<script>
    import { url } from "@sveltech/routify";
    export let slug;
    import data from "./products.json";
    const products = data.products;
</script>

{#each products as product}
    {#if (product.slug === slug)}
        <h1>{product.title}</h1>
        <img src="/{product.imagen}" alt="{product.title}">
        <p>{@html product.content}</p>
    {/if}
{/each}

<a href={$url(`${slug}/delete`)}>Delete</a>
