<template>
  <div class="login_container">
    <div class="login_box">
    	<div class="avatar_box">
    		<img src="../assets/logo.png"/>
    	</div>

    	<!--表单区域-->
    	<el-form ref="loginFormRef" :model="loginForm" class="login_form" label-width="0">
    		<el-form-item>
    			<el-input v-model="loginForm.username" prefix-icon="iconfont icon-user"></el-input>
    		</el-form-item>

    		<el-form-item>
    			<el-input v-model="loginForm.password" prefix-icon="iconfont icon-lock"></el-input>
    		</el-form-item>

    		<el-form-item class="btns">
    			<el-button type="primary">提交</el-button>
    			<el-button type="info">重置</el-button>
    		</el-form-item>
    	</el-form>
    </div>
  </div>
</template>

<script>
export default {
	data(){
		return {
			loginForm:{
				username:"username",
				password:"password"
			}
		}
	}
}
</script>

<style lang="less" scoped>
.login_container{
	background-color:#2b4b6b;
	height:100%;
}

.login_box{
    width:450px;
    height:300px;
    background-color:#fff;
    border-radius:3px;
    position:absolute;
    left:50%;
    top:50%;
    transform:translate(-50%,-50%);
    .avatar_box{
        width:130px;
        height:130px;
        border:1px solid #eee;
        border-radius:50%;
        padding:5px;
        box-shadow:0 0 2px #ddd;
        position:absolute;
        left:50%;
        transform:translate(-50%,-50%);
        background-color:#0ee;
        img{
            width:100%;
            height:100%;
            border-radius:50%;
            background-color:#eee;
        }
    }
}

.btns{
    display:flex;
    justify-content:flex-end;
}
.login_form{
    position:absolute;
    bottom:0%;
    width:100%;
    padding:0 10px;
    box-sizing:border-box;
}
</style>
