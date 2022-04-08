<template>
    <h1>Liste des Photos</h1>
    <div class="col">


        <Photo v-for="image of images" :key="image.id" :image="image.thumbnailUrl" :title="image.title" />


        
    </div>
</template>
<script>



import Photo from "../components/PictureComponent.vue"
    export default {
        components: {
           Photo
        },
        
        data() {
            return {
                images:[]
            }

        },
        async mounted() {

           await fetch('https://jsonplaceholder.typicode.com/photos')
              .then(response => response.json())
              .then(json => this.images = json)



        },

        
        method() {
            
        }
    }

</script>

<style>

    .col {
      width: 100%;
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      flex-direction: row;
      justify-content: center;
      align-items: center;
      margin: 10px;
    }
</style>