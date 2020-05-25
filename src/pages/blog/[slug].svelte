<script>
    import data from "./blog.json";
    const posts = data.posts;
    import { url } from "@sveltech/routify";
    export let slug;
    export let title;
    export let content;
</script>


<h1>{title}</h1>
<p>Blog article: {slug}</p>
<p style="color:red;">{content}</p>

<a href={$url(`../${slug}/delete`)}>Delete</a>
{#each posts as i}

<p> {i.id} for {slug}</p>
{/each}