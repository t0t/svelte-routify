<script>
  export let post;
  const { title, thumb, content } = post;
</script>

<style>
  .cssgrid {
    border: 1px dashed pink;
    display: grid;
    grid-template-columns: 25% 25% 50%;
    grid-template-rows: 50% 50%;
  }
</style>

<div class="cssgrid">
  <h3>{post.title}</h3>
  <img src="{post.thumb}" alt="Poster for {post.title}" />
  <p>{@html post.content}</p>
</div>
