<h1>Desktop</h1>

<script>
    import { count, filter } from "./store"

    $: numbers = Array.from({ length: $count }).map((_, i) => i)

    $: filters = $filter === "" ? "" : "&" + $filter
</script>

<div>
    {#each numbers as number}
        <img src={"https://picsum.photos/1900/1005?random=" + number + filters} alt="random photo">
    {/each}
</div>

<style>
    img {
        max-width: 100%;
        height: auto;
    }
</style>




