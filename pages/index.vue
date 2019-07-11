<template>
	<div class="container">
		<mt-header title="long long long long title" style="width:100%">
			<router-link to="/" slot="left">
				<mt-button icon="back">back</mt-button>
			</router-link>
			<mt-button icon="more" slot="right"></mt-button>
		</mt-header>
		{{content}}
		<mt-button type="primary" @click="open">弹框</mt-button>
	</div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import { Toast } from 'mint-ui'

export default {
	components: {
		Logo
	},
	data() {
		return {
			selected: '1',
			content: '内容'
		}
	},
	methods: {
		open() {
			Toast({
				message: 'operation success'
			})
		}
	}
}
</script>

<style>
.container {
	/* margin: 0 auto;
	min-height: 100vh; */
	/* display: flex;
	justify-content: center;
	align-items: center;
	text-align: center; */
}
/*
.title {
	font-family: 'Quicksand', 'Source Sans Pro', -apple-system,
		BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial,
		sans-serif;
	display: block;
	font-weight: 300;
	font-size: 100px;
	color: #35495e;
	letter-spacing: 1px;
}

.subtitle {
	font-weight: 300;
	font-size: 42px;
	color: #526488;
	word-spacing: 5px;
	padding-bottom: 15px;
}

.links {
	padding-top: 15px;
} */
</style>
