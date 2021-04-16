<script>
    let contactList

    export { contactList }
</script>

<div>
    {#each contactList as { name, number }, i}
        <p>{name}</p>
    {/each}
</div>
