<template>
	<div id="app">
		<header id="nav">
			<img src="/img/logo.svg" />
			<h1 class="title">mindy</h1>
		</header>
		<div class="separator" />
		<div class="content">
			<router-view/>
		</div>
	</div>
</template>

<script lang="ts">
	import Vue from 'vue';
	import Button from '@/components/Button.vue';
	import TextField from '@/components/TextField.vue';

	export default Vue.extend({
		components: {
			Button,
			TextField,
		},
		data() {
			return {
				text: '',
			};
		},
	});
</script>

<style lang="scss">
#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #262840;
}
#nav {
	padding: 8px 64px;
	display: flex;
	align-items: center;
	.title {
		padding-left: 14px;
		font-family: "Lobster Two";
		font-style: normal;
		font-weight: normal;
		font-size: 32px;
		line-height: 40px;
		color: #EA8A8C;
		margin: 0;
	}
}
.separator {
	width: 100%;
	height: 1.5px;
	background: linear-gradient(90deg, #D3EBAD 0%, #B3E5D9 100%);
}
.content {
	margin: 4em;
}
</style>

<style>
body {
	margin: 0;
}
</style>
