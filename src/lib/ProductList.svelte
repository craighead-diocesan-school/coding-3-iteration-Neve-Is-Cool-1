<script>
  let students = ["Alice", "Barbie", "Charlie"]
  import ProductItem from "./ProductItem.svelte"
  const products = [
    { name: "Apple", price: 1.0, description: "A juicy red apple" },
    { name: "Banana", price: 0.5, description: "A ripe yellow banana" },
    { name: "Cherry", price: 2.0, description: "A sweet red cherry" },
    { name: "Date", price: 1.5, description: "A dried date fruit" },
    { name: "Elderberry", price: 2.5, description: "A small dark berry" },
  ]
</script>

<div class="box">
  <ul>
    {#each students as student, index}
      <li>{index + 1}. {student}</li>
    {/each}
  </ul>
</div>
<div class="box">
  <ul>
    {#each products as product}
      <ProductItem name={product.name} price={product.price} description={product.description} />
    {/each}
  </ul>
</div>
