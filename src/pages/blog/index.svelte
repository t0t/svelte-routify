<script>
    import data from "./blog.json";
    import Post from "./Post.svelte";
    const posts = data.posts;
    
    import { url, isActive } from "@sveltech/routify";
</script>

<h1>Blog page</h1>
<ul>
    {#each posts as post}
        <Post {post} />
        <button class:selected={$isActive(post.slug)}>
            <a href="blog/{$url(post.slug)}">{post.title}</a>
        </button>
    {/each}
</ul>