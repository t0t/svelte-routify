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
  .cssgrid {
    list-style: none;
    border: 1px solid blue;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: minmax(100px, auto);
    /* grid-auto-rows: 100px; */
    gap: 1em;
    justify-items: stretch;
    align-items: center;
    margin: 0;
  }
  .cssgrid * {
    border: 1px solid rgb(128, 0, 30);
  }
  .MainNav {
      padding-left: 0;
  }
  .MainNav li {
      display: flex;
  }
  .MainNav li a {
      padding: 1em;
  }
</style>
<ul class="cssgrid MainNav">
  {#each links as [path, name]}
  <li>
    <a href="{$url(path)}" class:selected="{$isActive(path)}">{name}</a>
  </li>
  {/each}
</ul>
