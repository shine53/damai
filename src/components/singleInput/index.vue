<template lang="html">
	<div class="">
		<div class="input-group justify-content-center">
			<div class="input-group-prepend" :class="{'bg-white':inputData.white,'border-red':inputData.red}">
				<span :class="inputData.icon"></span>
			</div>
			<div class="form-group">
				<input :type='inputData.datatype' class="form-control" :class="{'border-red':inputData.red}" :placeholder='inputData.content'>
				<small class="form-text text-danger">{{inputData.small}}</small>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'singleInput',
	props:['inputData']
}
</script>

<style lang="css" scoped>
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
</style>
