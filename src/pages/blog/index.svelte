<script>
    import data from "./blog.json";
    import Post from "./Post.svelte";
    const posts = data.posts;
    
    import { url, isActive } from "@sveltech/routify";
</script>
<style>
    .cssgrid {
        padding: 24px;
        border: 1px solid green;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        /* grid-auto-rows: auto; */
        gap: 1em;
    }
</style>
<h1>Blog page</h1>
<section class="cssgrid">
    {#each posts as post}
        <Post {post} />
        <button class:selected={$isActive(post.slug)}>
            <a href="blog/{$url(post.slug)}">{post.title}</a>
        </button>
    {/each}
</section>