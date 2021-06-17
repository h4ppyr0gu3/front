<template>
	<div class="hero is-fullheight">
		<div class="hero-body is-centered-middle">
			<div class="columns p-5 m-5">
				<div class="column m-5 p-5">
					<p class="title is-size-1">musicApp</p>
				</div>
				<div class="column m-5 p-5">
					<div class="is-centered-middle" style="flex-direction: column;">
						<p class="has-text-centered text"> All your music where you want it!!</p>
						<div class="p-1">
						</div>
						<button class="button" @click="handleClick('signup')"> Sign up Now!</button>
						<div class="p-1">
						</div>
						<a @click="handleClick('login')">Log in</a>
					</div>
				</div>
			</div>
		</div>
	</div>

		<div class="columns my-3">
			<div class="column is-6">
				<p class="has-text-centered is-size-4 p-5"> Exciting new Features to look forward to:</p>
				<div class="is-centered-middle">
					<ol class="p-2">
						<li> improved error handling</li>
						<li>API only rails app, with js frontend, and improved design</li> 
						<li>better integration with music databases</li> 
						<li>one button to download all the songs on your device</li> 
						<li>device tracking for multi download to stop duplicates</li>
						<li>mp3 cutting</li>
						<li>Progressive web app to not have to download at all</li>
						<li>improved automatic renaming</li>
						<li>in browser player accross tabs</li>
						<li>lazy load from database</li>
						<li>equalizer</li>
						<li>Visualizer</li>
					</ol>
				</div>
			</div>
			<div class="column is-6">
				<p class="has-text-centered is-size-4 p-5"> Current Features:</p>
				<div class="is-centered-middle">
					<ol class="p-2">
						<li> Oauth 2.0</li>
						<li>Follow your friends and see what they are listeneng to</li>
						<li>Discuss music with friends with shared playlists</li>
						<li>mp3 header tag change and album art for download</li>
						<li>search database</li>
					</ol>
				</div>
			</div>
	</div>
	

</template>

<script type="text/javascript">
	export default {
		name: 'Landing',
		emits: ['handleClick'],
		methods: {
			handleClick(value) {
				console.log(value);
				this.$emit('handleClick', value)
			}
		}
	}
</script>

<style scoped type="text/css">


p.title {
	color: #C0F9FA;
	width: 15rem;
}

.text {
	color: #C0F9FA;
}

.button {
	border-radius: 2rem;
	padding-right: 2rem;
	padding-left: 2rem;
	background-color: #92F294;
	font-size: 20px;
	padding-top: 0px;
	padding-bottom: 0px;
}

.is-centered-middle {
  display: flex;
  justify-content: center;
  align-items: center;
}

a {
	text-decoration: underline;
	color: #C0F9FA;
}
</style>