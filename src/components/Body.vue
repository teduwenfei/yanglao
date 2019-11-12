<template>
    <div>
        <el-form ref="form" :model="form" label-width="100px">
          <div id="parent">
            <el-form-item label="养老院名称:" style="width:35%; font-weight:bold">
                <el-input v-model="form.name"></el-input>
            </el-form-item>
            <el-form-item label="账户名:" style="width:35%; font-weight:bold">
                <img src="../assets/logo.png" alt="" style="width:5%">
            </el-form-item>
            <el-form-item label="账户名:" style="width:35%; font-weight:bold">
                <el-input v-model="form.uname"></el-input>
            </el-form-item>
            <el-form-item label="密码:" style="width:35%; font-weight:bold">
                <el-input v-model="form.pwd"></el-input>
            </el-form-item>  
            <el-form-item label="报警手机号:" style="width:35%; font-weight:bold">
                <el-input v-model="form.phone"></el-input>
            </el-form-item> 
          </div>
          <div class="parent">
            <el-form-item label="活动性质:" prop="type" style="font-weight:bold;">
              <el-checkbox-group v-model="ruleForm.type">
                <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>
                <el-checkbox label="地推活动" name="type"></el-checkbox>
                <el-checkbox label="线下主题活动" name="type"></el-checkbox>
                <el-checkbox label="单纯品牌曝光" name="type"></el-checkbox>
              </el-checkbox-group>
            </el-form-item>
            <el-form-item label="后台模块选择:" prop="type" style="font-weight:bold">
              <el-checkbox-group v-model="ruleForm.type">
                <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>
                <el-checkbox label="地推活动" name="type"></el-checkbox>
                <el-checkbox label="线下主题活动" name="type"></el-checkbox>
                <el-checkbox label="单纯品牌曝光" name="type"></el-checkbox>
              </el-checkbox-group>
            </el-form-item>
          </div>
        </el-form>
    </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          name: '',
          uname:'',
          phone:'',
          pwd:'',
        },
        ruleForm: {
          type: []
        },
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
  }
</script>
<style scoped>
  #parent{
    width:60%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
  .el-checkbox-group{
    width:100%;  
  }
  .el-checkbox{
    width:100%;
    text-align:center;
    border:1px solid #ccc;
  }
  .parent{
    width:100%;
    display: flex;
    justify-content: space-between;
  }
  .el-form-item:nth-child(1){
    width:20.7%;
  }
  .el-checkbox-group{
    margin-top:20px;
  }
</style>