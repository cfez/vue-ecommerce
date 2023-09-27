<script setup>
   defineProps(['title', 'description', 'image', 'price', 'ratings', 'category'])
   
</script>

<template>
    <div id="datacover">
        <div id="datacoverimg">
           <img :src="image" />
        </div>
        <p>
            {{ title }}
        </p>
        <p>
            {{ description }}
        </p>
    </div>
</template>


<style>
   img{
      max-width: 200px;
      height: 200px;
      display: block;
      margin: auto;
   }
   #datacover{
      width: 23%;
      
   }
   #datacoverimg{
    background-color: #f5f6f6;
   }
</style>