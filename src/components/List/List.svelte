<script>
    import { slide, fade } from 'svelte/transition'

    let contactList

    export { contactList }
</script>

<div>
    {#if contactList.length > 0}
        {#each contactList as { name, number }, i}
            <div class="card" transition:fade>
                <p transition:slide|local>{i + 1}. {name} &middot; {number}</p>
            </div>
        {/each}
    {:else}
        <p>No Data</p>
    {/if}
</div>

<style>
    .card {
        width: 100%;

        text-align: left;
    }
</style>
