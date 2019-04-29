<template>
  <div class="register">
    <Common :title="navTitle">
    	<div class="register-form w-100 justify-content-center">
			<MyForm :formData='formData'/>
    	</div>
    </Common>
  </div>
</template>

<script>
// @ is an alias to /src
import Common from '@/components/common'
import MyForm from '@/components/myForm'

export default {
  name: 'register',
  data() {
	return {
		navTitle: '账户注册',
		formData: {
			phone: true,
			password: true,
			passwordAgain: true,
			securityCode: true,
			small: true
		}
	}
  },
  components: {
   Common,
    MyForm
  }
}
</script>
<style lang="scss">
	.register-form {
		padding: 80px;
	}
</style>
