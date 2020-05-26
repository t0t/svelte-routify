<script>
    import { url } from "@sveltech/routify";
    export let slug;
    import data from "./products.json";
    const products = data.products;
</script>

<style>
  .cssgrid {
    padding: 24px;
    border: 1px solid rgb(128, 0, 30);
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    /* grid-auto-rows: auto; */
    gap: 1em;
  }
  .cssgrid * {
    border: 1px solid rgb(128, 0, 30);
  }
</style>

<div class="cssgrid">
    {#each products as product}
    {#if (product.slug === slug)}
        <h1>{product.title}</h1>
        <img src="/{product.imagen}" alt="{product.title}">
        <p>{@html product.content}</p>
    {/if}
{/each}
</div>

<a href={$url(`${slug}/delete`)}>Delete</a>
