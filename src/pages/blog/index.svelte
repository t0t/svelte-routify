<script>
    import data from "./blog.json";
    const posts = data.posts;
    
    import { url, isActive } from "@sveltech/routify";
    const links = [
        ["blog/foo", "Foo"],
        ["blog/bar", "Bar"],
        ["blog/lum", "lum"],
    ];
</script>

<h1>Blog page</h1>

<ul>
    {#each posts as post}
    <li>
        <img src="{post.thumb}" alt="">
        <button><a href=blog/{$url(post.slug)}>{post.title}</a></button>
      <p>{post.excerpt}</p>
    </li>
    {/each}
</ul>
<ul>
    {#each links as [path, name]}
    <li>
      <a href={$url(path)} class:selected={$isActive(path)}>{name}</a>
    </li>
    {/each}
</ul>