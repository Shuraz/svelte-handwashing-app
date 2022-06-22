<script>
    export let progress=0;
</script>
<style>
    .progress-container{
        border: solid red 1px;
        margin: 20px 0;
    }
    .progress-bar{
        height: 30px;
        background-color: green;
    }
</style>
<div bp=grid>
    <div bp="offset-5@md 4@md 12@sm" class="progress-container">
        <div class="progress-bar" style="width:{progress}%"></div>
        <span class="sr-only">%{progress}</span>
    </div>

</div>