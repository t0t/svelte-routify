<script>
    import data from "./products.json";
    import Product from "./Product.svelte";
    const products = data.products;
    
    import { url, isActive } from "@sveltech/routify";
</script>

<svelte:head>
	<title>TODH</title>
</svelte:head>

<style>
    .cssgrid {
        padding: 24px;
        border: 1px solid green;
        display: grid;
        grid-template-columns: repeat(2, 2fr);
        grid-template-rows: repeat(1, 2fr);
        /* grid-auto-rows: auto; */
        gap: 1em;
    }
</style>

<h1>Products</h1>

<section>
    {#each products as product}
        <Product {product} />
        <button class:selected={$isActive(product.slug)}>
            <a href="products/{$url(product.slug)}">{product.title}</a>
        </button>
    {/each}
</section>