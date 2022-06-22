<script>
	import HowTo from "./HowTo.svelte"
	import Timer from "./Timer.svelte"
	let audio;
	const timerEnd=(e)=>{
console.log(e.detail);
audio.play();

	}
</script>
<style>
	h1,h3{
		text-align: center;
	}
</style>
<h1>Handwashing App</h1>
<Timer on:endwash={timerEnd}/>
<HowTo/>

<h3>
	<a href="#">Picture Source</a>
	<a href="#">Sound Source</a>
</h3>
<audio bind:this={audio} src="public_sound.wav"></audio>