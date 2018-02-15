<!--suppress ALL -->
<template lang="pug">
	#app
		v-app(dark)
			v-navigation-drawer(app)
				v-toolbar(flat)
					v-list
						v-list-tile
							v-list-tile-title.title Application
				v-divider
				v-list.pt-0(dense)
					v-list-tile(v-for="item in items" v-bind:key="item.title" @click="$router.push(item.link)" ripple)
						v-list-tile-action
							v-icon {{ item.icon }}
						v-list-tile-content
							v-list-tile-title {{ item.title }}
			v-toolbar(app)
			v-content
				v-alert(type="success" dismissible  v-bind:value="succAlert" v-model="alert" transition="scale-transition") This is a success alert.
				router-view
		v-footer(dark)
			v-card.text-xs-center(flat tile)
				v-cart-text.white--text
					| &copy;2018 —
					strong VentumIT
</template>

<script lang="ts">
	import { Component, Vue } from 'vue-property-decorator';

	@Component
	export default class App extends Vue {
		data () {
			return {
				alert: true,

				items: [
					{ title: 'Home', icon: 'dashboard', link: '/' },
					{ title: 'About', icon: 'question_answer', link: '/about' }
				],
			}
		}
	}
</script>


<style lang="stylus">
	@import '~vuetify/src/stylus/main'

	.footer
		@extend .application .theme--dark.toolbar

	.alert
		@extend .mx-2, .my-2

	#app
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;

	#nav
		padding: 30px;

	#nav a
		font-weight: bold;

	#nav a.router-link-exact-active
		color: #42b983;
</style>
