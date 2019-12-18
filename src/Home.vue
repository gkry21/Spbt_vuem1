<template>
	<div id="app">
	<layout>
		<template #header="header">
			<h1>{{header.title}}</h1>
		</template>
		<template #sidebar="sidebar">  <!-- 사이더바에 메뉴 만들기 -->
		<ul class="menu">
			<li v-for="i of sidebars" :key= "i.menu">
			<router-link :to="i.link">{{i.menu}}</router-link>
			</li>
		</ul>
		</template>
		<template #content="content">
			<h1>{{content.title}}</h1>
		</template>
		<template #footer="footer">
		<h1>{{footer.title}}</h1>
		</template>
	</layout>
	</div>
</template>
<script>
import Layout from '@/components/Layout.vue'
export default {
	name : "homeApp",
	components: {Layout},
	data(){
		return { 
			sidebars: [
				{menu: "Home", link: "#"},
				{menu: "About", link: "/app"},
				{menu: "Contact", link: "#"},
				{menu: "Subject", link: "#"},
				{menu: "cart", link: "/cart"},
				{menu: "calculator", link: "/calculator"},
				{menu: "seqsum", link: "/seqsum"},
				{menu: "acc", link: "/acc"},
				{menu: "todo", link: "/todo"}

			]
		}
	}
}
</script>
<style scoped>
ul.menu {
    position:relative;
    padding: 5px 5px 5px 5px;
    list-style: none;
    font-style: italic;
}
ul.menu a {
    text-decoration:none;
}
</style>