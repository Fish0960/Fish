/*
 * @Author: liuyr 
 * 权限列表页面
 * @Date: 2019-12-23 17:11:53 
 * @Last Modified by: liuyr
 * @Last Modified time: 2019-12-23 21:28:33
 */
<template>
  <div id="limitList">权限列表页面
  
  <div>
    
  <el-form-item label="活动名称">
    <el-input v-model="form.name"></el-input>
  </el-form-item>

     <el-form-item label="活动区域">
    <el-select v-model="form.region" placeholder="请选择活动区域">
      <el-option label="区域一" value="shanghai"></el-option>
      <el-option label="区域二" value="beijing"></el-option>
    </el-select>
  </el-form-item>
  </div>
</div>
</template>

<script>
import axios from "axios";
import qs from "qs";
//设置基础路径
axios.defaults.baseURL = "http://127.0.0.1:8899";

export default {
  data() {
    return {};
  },
  computed: {},
  methods: {},
  created() {},
  mounted() {}
};
</script>
<style scoped>
</style>