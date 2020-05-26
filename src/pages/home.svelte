<h1>Esta es la HOME</h1>

<div class="cssgrid">
  <div>lorem</div>
  <div>lorem</div>
  <div>lorem</div>
  <div>lorem</div>
  <div>lorem</div>
</div>

<style lang="scss">
  .cssgrid {
    border: 1px solid blue;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-auto-rows: 10em;
    gap: 1em;
    padding: 1em;
  }
  .cssgrid > div {
    border: 1px solid red;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
