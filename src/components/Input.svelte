<script>
    export let name = "Default"
</script>
<style>
    input {
        margin-top: 20px;
    }
</style>

<div class="Input">
    <input type="text" bind:value={name} />
    <p>Hello {name} !</p>
</div>