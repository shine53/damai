<template lang="html">
	<div class="">
		<form class="form-list bg-white" action="index.html" method="post">
			<div class="input-group justify-content-center" v-show='formData.phone'>
				<div class="input-group-prepend bg-white border-red">
					<span class="icon-user"></span>
				</div>
				<div class="form-group">
					<input type="number" class="form-control border-red" placeholder="请输入手机号">
					<small class="form-text text-danger" v-show='formData.small'>请填写手机号</small>
				</div>
			</div>
			<div class="input-group justify-content-center" v-show='formData.password'>
				<div class="input-group-prepend bg-white border-red">
					<span class="icon-lock-closed"></span>
				</div>
				<div class="form-group">
					<input type="password" class="form-control border-red" placeholder="请输入密码">
					<small class="form-text text-danger" v-show='formData.small'>请填写密码</small>
				</div>
			</div>
			<div class="input-group justify-content-center" v-show='formData.passwordAgain'>
				<div class="input-group-prepend bg-white border-red">
					<span class="icon-lock-closed"></span>
				</div>
				<div class="form-group">
					<input type="password" class="form-control border-red" placeholder="请确认密码">
					<small class="form-text text-danger" v-show='formData.small'>请确认密码</small>
				</div>
			</div>
			<div class="form-half" v-show='formData.securityCode'>
				<div class="row">
					<div class="col-6 offset-sm-1">
						<div class="input-group">
							<div class="input-group-prepend bg-white border-secondary">
								<span class="icon-message"></span>
							</div>
							<div class="form-group">
								<input type="password" class="form-control border-secondary" placeholder="请输入验证码">
							</div>
						</div>
					</div>
					<div class="col-3">
						<button class="btn btn-outline-secondary" type="button" name="button">获取验证码</button>
					</div>
				</div>
			</div>
			<input class="form-submit bg-danger" type="submit" value="提交">
		</form>
	</div>

</template>

<script>
export default {
	name: 'myForm',
	props: ['formData']
}
</script>

<style lang="css" scoped>
.form-list {
	padding: 50px 100px;
}
.input-group-prepend {
	display: inline-block;
	padding: 8px;
	height: 38px;
	border-radius: 5px 0 0 5px;
}
.border-red {
	border: 1px solid red !important;
}
.border-secondary{
	border: 1px solid #6c757d;
}
.form-group {
	width: 85%;
}
.form-control {
	border-radius: 0 5px 5px 0 !important;
}
.form-submit {
	border-radius: 5px;
	width: 90%;
	margin: 6%;
	padding: .5em;
	color: #fff;
}
</style>
