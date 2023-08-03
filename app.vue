<template>
  <div>
    <pre>productObj: dsfwesdo0kp{{ productObj }}</pre>
    <pre> rawObj:{{ rawObj }}</pre>
  </div>

</template>
<script setup>
const productObj = ref(null);
async function getFaceApi(){
  const data =await $fetch("https://fakestoreapi.com/products");
  productObj.value = data;
}
getFaceApi()
</script>