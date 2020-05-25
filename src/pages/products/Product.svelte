<script>
  export let product;
  const { title, thumb, content } = product;
</script>

<div>
  <h3>{product.title}</h3>
  <img src="{product.thumb}" alt="product {product.title}" />
  <p>{@html product.content}</p>
</div>
