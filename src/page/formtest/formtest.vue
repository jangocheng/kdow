<template>
	<div>
		<span v-text="msg"></span>
		<div>
			<button class="testCss" @click="printSomething">输出点啥</button>
		</div>
		<div>
			<h2>测试kdowForm</h2>
			<kdow-form 
			:definition="form.definition"
			:objects="form.objects"
			@update:model="(model)=>{form.objects = model}"/>
			<button type="submit" @click="submitForm">提交表单</button>
		</div>
	</div>
</template>
<style type="text/css">
	@import './formtest.css';
</style>
<script>
   export default require('./formtestController.js')
</script>