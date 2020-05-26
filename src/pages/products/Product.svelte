<script>
  export let product;
  const { title, thumb, content } = product;
</script>

<style>
  .cssgrid {
    border: 1px dashed pink;
    display: grid;
    grid-template-columns: 25% 25% 50%;
    grid-template-rows: repeat(1, 2fr);
  }
</style>

<div class="cssgrid">
  <h3>{product.title}</h3>
  <p>{@html product.content}</p>
  <img src="{product.thumb}" alt="product {product.title}" />
</div>
