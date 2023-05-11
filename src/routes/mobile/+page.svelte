<h1>Mobile</h1>

<script>
    import { count, filter } from "./store"

    $: numbers = Array.from({ length: $count }).map((_, i) => i)

    $: filters = $filter === "" ? "" : "&" + $filter
</script>

<div>
    {#each numbers as number}
        <img class ="grid" src={"https://picsum.photos/320/640?random=" + number + filters} alt="random photo">
    {/each}
</div>

<style>
    img {
        max-width: 100%;
        height: auto;
    }
</style>
