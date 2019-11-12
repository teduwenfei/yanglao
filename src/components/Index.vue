<template>
  <el-container style=" border: 1px solid #eee">
    <el-aside width="15%" style="background-color: rgb(238, 241, 246)">
      <img src="../assets/logo.png" alt="">
      <el-menu >
        <el-submenu index="1">
          <template slot="title">
            <div @click="xuanzhong(1)">
              <i class="el-icon-message"></i>
              系统账号
            </div>
          </template>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <div @click="xuanzhong(2)">
              <i class="el-icon-menu"></i>
              设备管理
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(3)">
              <i class="el-icon-setting"></i>
              长者管理
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(4)">
              <i class="el-icon-setting"></i>
              护理员管理
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(5)">
              <i class="el-icon-setting"></i>
              访客管理
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(6)">
              <i class="el-icon-setting"></i>
              数据记录
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(7)">
              <i class="el-icon-setting"></i>
              数据分析
            </div>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <div @click="xuanzhong(8)">
              <i class="el-icon-setting"></i>
              系统设置
            </div>
          </template>
        </el-submenu>
        
      </el-menu>
    </el-aside>
    
    <el-container>
      <el-header style="font-size: 25px">
        <my-header style="width:100%" ></my-header>
      </el-header>
      
      
      <el-main>
        <Body v-show="xuan===1">
          
        </Body>
      </el-main>
    </el-container>
  </el-container>
</template>
<script>

  export default {
    data() {
      return {
        xuan:1
      }
    },
    methods:{
      xuanzhong(i){
        this.xuan=i
      }
    }
  };
</script>
<style scoped>
  .el-header {
    color: #333;
    line-height: 60px;
    display:flex;
    justify-content: space-between;
  }
  .el-aside {
    color: #333;
  } 
</style>