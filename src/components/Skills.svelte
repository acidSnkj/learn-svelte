<script>
    let skills = [
        {id: 1, name: 'HTML', value: 80},
        {id: 2, name: 'CSS', value: 70},
        {id: 3, name: 'JavaScript', value: 60},
    ]
</script>
<style>
    .Skills {
        display: flex;
        justify-content: center;
    }
    ul {
        margin: 0;
        padding: 0;
        list-style: none;
    }
    li {
        display: inline;
        margin: 0 0 0 0.4em;
    }
</style>
<div class="Skills">
    <strong>Habilidades</strong>
    <ul>
        {#each skills as {name, value}, i}
        <li>
            {name} - {value}%
        </li>
        {/each}
    </ul>
</div>