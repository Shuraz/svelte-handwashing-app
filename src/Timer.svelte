<script>
    import ProgressBar from "./ProgressBar.svelte";
    let totalSecond=20;
    let secondLeft=totalSecond;
    let isRunning=false;
    //calculate in percent
    $: progress = ((totalSecond-secondLeft)/totalSecond)*100;
    const handleStart=()=>{
        isRunning=true;
        let timer =setInterval(() => {
            secondLeft -=1;
            if(secondLeft==0){
                clearInterval(timer)
                secondLeft=totalSecond;
                isRunning=false;
            }
        }, 1000);

    }
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
    .start[disabled]{
background-color: gray;
cursor: not-allowed;
    }
</style>
<!-- <p>Timer</p> -->
<div bp="grid">
<h2  bp="offset-5@md 4@md 12@sm">Second Left: {secondLeft}</h2>
</div>
<ProgressBar progress={progress}/>
<div bp="grid">

 <button disabled={isRunning}  bp="offset-5@md 4@md 12@sm" class="start" on:click={handleStart}>Start</button>

</div>