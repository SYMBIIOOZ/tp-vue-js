<template>
    <div>
        <div>
        <img :src="photo.url">{{photos.title}}<img>
        
        </div>
       
    </div>
</template>
<script>

    export default {
        
        name: "PhotoView",
        props: {
            photos: Object,
            
        },
        
        data() {

            return {

            }
        },
        
        methods: {
            
        },
    }
</script>

<style>
.ok {
    color:rgb(7, 255, 7);
}
.nok {
    color:red;
}
</style>