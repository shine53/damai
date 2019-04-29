<template lang="html">
	<div class="login">
      <Common :title="navTitle">
		  <div class="login-section">
		  	<div class="row">
		  		<div class="col-6">
		  			<img src="./img/login.png" alt="">
		  		</div>
				<div class="col-6 right-section bg-white">
					<ul class="nav nav-tabs">
						<li class="nav-item" @click='bol=!bol'>
							<a class="nav-link" :class="{'active':bol}" href="#">账户登陆</a>
						</li>
						<li class="nav-item" @click='bol=!bol'>
							<a class="nav-link" :class="{'active':!bol}" href="#">短信登陆</a>
						</li>
					</ul>
					<div class="tab-content">
						<div class="login-form w-100 justify-content-center" v-show='bol'>
				  			<MyForm :formData='formData1'/>
							<div class="">
								<ul class="d-flex justify-content-around">
									<li><input type="checkbox" name="" value="">下次自动登陆</li>
									<li>
										<ul class="d-flex">
											<li>忘记密码？</li>
											<li class="color-danger">立即注册</li>
										</ul>
									</li>
								</ul>
								<p class="ml-5">其他登陆：<span class="icon-wechat"></span></p>
							</div>
				      	</div>
						<div class="login-form w-100 justify-content-center" v-show='!bol'>
				  			<MyForm :formData='formData2'/>
							<div class="">
								<ul class="d-flex justify-content-around">
									<li><input type="checkbox" name="" value="">下次自动登陆</li>
									<li>
										<ul class="d-flex">
											<li><a href="#">忘记密码？</a></li>
											<li><a class="color-red" href="#">立即注册</a></li>
										</ul>
									</li>
								</ul>
								<p class="ml-5">其他登陆：<span class="icon-wechat"></span></p>
							</div>
				      	</div>
					</div>
				</div>
		  	</div>
		  </div>
      </Common>
    </div>
</template>

<script>
import Common from '@/components/common'
import MyForm from '@/components/myForm'

export default {
	name: 'login',
	data() {
	  return {
		  navTitle: '欢迎登陆',
		  bol: true,
		  formData1: {
			  phone: true,
			  password: true,
			  passwordAgain: false,
			  securityCode: false,
			  small: false
		  },
		  formData2: {
			  phone: true,
			  password: false,
			  passwordAgain: false,
			  securityCode: true,
			  small: false
		  }
	  }
	},
	components: {
	 Common,
	  MyForm
	}
}
</script>

<style lang="css" scoped>
.login-section {
	padding: 80px 50px;
}
img {
	display: block;
	width: 100%;
	height: 100%;
}
>>>.form-list {
	padding: 80px 20px 20px;
}
.color-red {color: red;}
.login-form {
	padding: 5px;
}
</style>
