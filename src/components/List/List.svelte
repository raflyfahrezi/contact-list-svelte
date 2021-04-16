<script>
    let contactList

    export { contactList }
</script>

<div>
    {#each contactList as { name, number }, i}
        <div class="card">
            <p>{i + 1}. {name} &middot; {number}</p>
        </div>
    {/each}
</div>

<style>
    .card {
        width: 100%;

        text-align: left;
    }
</style>
