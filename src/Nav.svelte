<script>
    import { url, isActive } from "@sveltech/routify";

    const links = [
        ["./home", "home"],
        ["./about", "about"],
        ["./blog", "blog"],
        ["./products", "products"],
    ];
</script>
<style>
    .selected {
        color: red;
    }
</style>
<ul>
    {#each links as [path, name]}
    <li>
      <a href={$url(path)} class:selected={$isActive(path)}>{name}</a>
    </li>
    {/each}
</ul>