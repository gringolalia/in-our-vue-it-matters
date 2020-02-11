<template lang="pug">
.home
	img(alt='Vue logo' src='../assets/anarchy.svg' width='125px')
	HelloWorld(msg='Good Morning, Midnight').
	.md-display-2.my-4 Ban the Bomb
	.md-display-1.mt-2.mb-4 Burn the Brassiere
	md-button.md-dense.md-raised.md-primary Pressed for Time
	md-button.md-dense.md-raised.md-accent Press Your Luck
		
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
	name: 'Home',
	components: {
		HelloWorld
	}
}
</script>

<style>
.home {
	min-height: 100vh;
}