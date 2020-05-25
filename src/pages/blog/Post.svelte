<script>
  export let post;
  const { title, thumb, content } = post;
</script>

<div>
  <h3>{post.title}</h3>
  <img src="{post.thumb}" alt="Poster for {post.title}" />
  <p>{@html post.content}</p>
</div>
