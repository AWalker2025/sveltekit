
<script>
    const numberOfImages = 20

    const numbers = Array.from({ length: numberOfImages }).map((_, i) => i)

    let width = 300
    let height = 300
</script>

<div>
    {#each numbers as number}
        <img class ="grid" alt="random photo" src={"https://picsum.photos/" + width + "/" + height + "?random=" + number }>
    {/each}
</div>