<script>
    import ProgressBar from "./ProgressBar.svelte";
</script>
<style>
    h2{
        margin: 0;
    }
    .start{
        background-color: maroon;
        margin: 10px 0;
        width: 100%;
    }
</style>
<!-- <p>Timer</p> -->
<div bp="grid">
<h2  bp="offset-5@md 4@md 12@sm">Second Left:</h2>
</div>
<ProgressBar/>
<button class="start">Start</button>