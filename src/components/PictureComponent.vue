<template>
    <div>
        <div class ='row'>
          <img :src="image" :alt="title" >

        </div>

    </div>
</template>
<script>

    export default {

        name: "PhotoView",
        props: {
          image: String,
          title: String,


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


.row{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin: 10px;
}
.ok {
    color:rgb(7, 255, 7);
}
.nok {
    color:red;
}
</style>