<template>
	<div class="container full">
		<div class="top">
		</div>
		<h1 class="is-size-1 title has-text-centered">musicApp</h1>
		<hr>
		<div class="is-centered-middle">
			<button class="button login facebook" style="font-weight: bold;"><img :src="require('@/assets/images/facebook.svg')" style="height:100%; padding-right: 2rem;">Facebook</button>
		</div>
		<div class="is-centered-middle">
			<button class="button login google" style="font-weight: bold;"><img :src="require('@/assets/images/google.svg')" style="height:100%; padding-right: 2rem;">Google</button>
		</div>
		<div class="separator " style="color:#C0F9FA; font-weight: bold;">OR</div>
		<div class="form is-centered-middle" style="min-width:100%;">
			<div class="field">
			<label class="label title">Email</label>
				<div class="control">
					<input class="input " type="text" placeholder="example@example.com">
				</div>
			</div>
		</div>
		<div class="form is-centered-middle pt-3" style="min-width:100%;">
			<div class="field">
			<label class="label title">Password</label>
				<div class="control">
					<input class="input " type="text" placeholder="password123">
				</div>
			</div>
		</div>
		<div class="is-centered-middle pt-2">
			<div style="min-width: 30vw;">
				<span style="color:#C0F9FA;font-weight: bold;min-width:50%;float:left;"><input type="checkbox" style="margin-right:0.5rem;">Remember me</span>
				<a href="#" style="color:#C0F9FA; text-decoration: underline;min-width:50%;float:left;">Forgot your password?</a>
			</div>
		</div>
		<div class="is-centered-middle">
			<button class="button login boss" style="font-weight: bold;" @click="handleClick('dashboard')"><i class="fa-fa-login"/>Login</button>
		</div>
		<hr>
		<div class="is-centered-middle">
			<p class="title label" style="font-weight: bold;">Don't have an account?</p>
		</div>
		<div class="is-centered-middle pt-1">
			<button class="button login google" style="font-weight: bold;" @click="handleClick('signup')">Sign up</button>
		</div>


	</div>

	</template>

	<script>

		export default {
			name: "Login",
			emits: ['handleClick'],
			methods: {
				handleClick(value) {
					console.log(value);
					this.$emit('handleClick', value)
				}
			}
		}

	</script>

	<style type="text/css" scoped>

.facebook{
	background-color: #898F9C;
	border-color: #898F9C;
	color: #fff;
}
.login {
	border-radius: 500px;
	min-width: 30vw;
	margin-top: 5px;
	margin-bottom: 5px;
}
.boss{
	background-color: #64E987;
	border-color: #64E987;
}
.title {
	color: #C0F9FA;
}
hr {
	border: none;
	height: 1px;
	color: #333; /* old IE */
	background-color: #333; /* Modern Browsers */
}
.full {
	height: 100%;
	padding-bottom: 10vh;
}
.top {
	padding-top: 10vh;
}
.is-centered-middle {
	display: flex;
	justify-content: center;
	align-items: center;
}
.is-flex-column {
	flex-direction: column;
}
.is-flex-row {
	flex-direction: row;
}
.separator {
	display: flex;
	align-items: center;
	text-align: center;
}

.separator::before,
.separator::after {
	content: '';
	flex: 1;
	border-bottom: 1px solid #333;
	margin-top: 30px;
	margin-bottom: 30px;
	color: #C0F9FA;
}

.separator:not(:empty)::before {
	margin-right: .25em;
}

.separator:not(:empty)::after {
	margin-left: .25em;
}

.input{
	min-width: 30vw;
	background-color: #ffffcc;
}
</style>