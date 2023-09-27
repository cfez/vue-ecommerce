<script setup>
    import HeadItem from './components/HeadItem.vue'
    import BodyItem from './components/BodyItem.vue'
    import { ref } from 'vue'

    const storeItem = ref([])

    
            

    async function getData() {
    const res = await fetch('https://fakestoreapi.com/products');
    const finalRes = await res.json();
    storeItem.value = finalRes;
  }

    getData()
    
    console.log(storeItem)

</script>


<template>
     <HeadItem/> 
     <div id="bodydata">
        <BodyItem v-for="item in storeItem" 
             :key="item.id" 
             :title="item.title" 
             :category="item.category"
             :image="item.image"
             :price="item.price"
             :description="item.description"/>
     </div>
</template>
