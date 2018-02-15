<!--suppress ALL -->
<template lang="pug">
	#app
		v-app(dark)
			v-navigation-drawer(app)
			v-toolbar(app)
			v-content
				v-alert(type="success" dismissible  v-bind:value="true") This is a success alert.
				router-view
		v-footer
</template>

<style lang="stylus">
	@import '~vuetify/src/stylus/main'


	#app
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;

	#nav
		padding: 30px;

	#nav a
		font-weight: bold;
		color: #2c3e50;

	#nav a.router-link-exact-active
		color: #42b983;
</style>
