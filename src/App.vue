<script>
import MyButton from './components/ui/MyButton.vue';
import MainContactDiv from './components/ui/MainContactDiv.vue';

export default {
  data() { 
    return {
      friends: [
        {
          id: "michael",
          name: "Michael Jackson",
          phone: "123 45678 90",
          email: "michael@localhost.com",
          
        },
        {
          id: "aulie",
          name: "Aulie Dulat ",
          phone: "123 44328 90",
          email: "julie@localhost.com",
          
        },
        {
          id: "arch",
          name: "Arrrrrchynbek",
          phone: "123 44328 90",
          email: "julie@localhost.com",
          
        },
        {
          id: "saksh",
          name: "Sakshbek",
          phone: "123 44328 90",
          email: "julie@localhost.com",
          
        },
      ],
    };
  },
  components: {
    MyButton,
    MainContactDiv
  },
  methods: {
    
  }
}
</script>

<template>
  <div class="app">

    <div class="navbar">
       <h1>My Contacts</h1>
    </div>

    <MainContactDiv
    v-for="friend in friends"
      :id="friend.id"
      :name="friend.name"
      :phoneNumber="friend.phone"
      :emailAddress="friend.email"
      :isFavorite="friend.isFavorite"
      @click="toggleFavoriteStatus"
    />


  </div>
  
</template>

<style scoped>
  .app{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    gap: 30px;
  }
  .navbar{
    display: flex;
    height: 150px;
    width: 500px;
    border-radius: 12px;
    background-color: rgb(122, 24, 122);
    justify-content: center;
    align-items: center;
    box-shadow: 0px 0px 10px lightslategray;
  }
  .navbar h1{
    color: white;
  }

  
</style>
