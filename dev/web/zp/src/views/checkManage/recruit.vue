/*
 * @Author: liuyr 
 * 招聘审核页面
 * @Date: 2019-12-23 17:11:53 
 * @Last Modified by: lijunkun
 * @Last Modified time: 2019-12-25 16:48:13
 */
<template>
  <div id="recruitCheck">
    <div class="serchDiv">
      <el-select v-model="value" placeholder="职位类型">
    <el-option
      v-for="item in jobData"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
    </div>
    <div class="tableDiv">
       <el-table
    ref="multipleTable"
    :data="tableData"
    tooltip-effect="dark"
    style="width: 100%"
    @selection-change="handleSelectionChange">
    <el-table-column
      type="selection"
      width="55">
    </el-table-column>
    <el-table-column
      label="招聘标题"
      width="200">
      <template slot-scope="scope">{{ scope.row.date }}</template>
    </el-table-column>
    <el-table-column
      prop="name"
      label="发布人"
      width="120">
    </el-table-column>
    <el-table-column
      prop="address"
      label="联系方式"
      show-overflow-tooltip>
    </el-table-column>
     <el-table-column
      prop="address"
      label="职位"
      show-overflow-tooltip>
    </el-table-column>
    <el-table-column
      prop="address"
      label="发布时间"
      show-overflow-tooltip>
    </el-table-column>
    <el-table-column align="center" label="详细信息">
          <template slot-scope="scope">
            <el-button @click="toSee(scope.row)" type="text" size="small">查看</el-button>
          </template>
        </el-table-column>
    
    <el-table-column align="center" label="状态" width="100">
          <template slot-scope="scope">
            <el-button type="text" @click="toEdit(scope.row)" size="small">通过</el-button>
            <el-button type="text" size="small" @click="toDelete(scope.row.id)">拒绝</el-button>
          </template>
        </el-table-column>
  </el-table>
    </div>
  </div>
</template>

<script>
import {recruit} from '@/api/recruit.js';
import config from "@/utils/config.js";


export default {
  data() {
    return {
      recruitL:"",
      recruitData:[],
    };
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {}
};
</script>
<style scoped>
</style>