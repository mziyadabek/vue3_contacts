<template>
    <div class="contact">
        <h1> {{ name }} <span v-if="isFavorite == true" >(Best Friend)</span> </h1>
        <div class="btns">
            <MyButton @click="toggleShowDet" >  Show Datails </MyButton>
            <MyButton @click="toggleFavorite" > Best Friend  </MyButton>
        </div>
         <ul v-if="isVis == true" >
            <li><strong>Phone:</strong> {{ phoneNumber }}</li>
            <li><strong>Email:</strong> {{ emailAddress }} </li>
        </ul>
    </div>
</template>

<script>
    import MyButton from './MyButton.vue';
    export default{
      data(){
        return{
          isFavorite: false 
          ,
  
          isVis: false
        }
      }
    ,
    components: {
            MyButton
        },
    props: {
    id: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    phoneNumber: {
      type: String,
      required: true,
    },
    emailAddress: {
      type: String,
      required: true,
    },
    
  },

  methods : {
     toggleShowDet(){
       this.isVis  = !this.isVis
     }, toggleFavorite() {
      this.isFavorite = !this.isFavorite
    },
  }

    }
</script>

<style scoped>
    .contact{
        display: flex;
        flex-direction: column;
        width: 500px;
       
        border-radius: 12px;
        align-items: center;
        box-shadow: 0px 0px 10px lightslategray;
    }
    .contact h1{
        border-bottom: 2px solid gray;
        width: 80%;
        text-align: center;
        color: rgb(122, 24, 122);
     }

    .btns{
        display: flex;
        gap: 10px;
        padding-bottom: 10px;
    }

     ul {
  margin: 0;
  padding: 0;
  list-style: none;
  width: 400px;
  
}

li {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 90%;
  max-width: 40rem;
}
</style>
