<script>
    import data from "./products.json";
    import Product from "./Product.svelte";
    const products = data.products;
    
    import { url, isActive } from "@sveltech/routify";
</script>

<h1>Products</h1>
<ul>
    {#each products as product}
        <Product {product} />
        <button class:selected={$isActive(product.slug)}>
            <a href="products/{$url(product.slug)}">{product.title}</a>
        </button>
    {/each}
</ul>