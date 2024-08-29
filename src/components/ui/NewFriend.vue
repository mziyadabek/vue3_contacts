<template>
    <form @submit.prevent="submitData" >
        <label for="Name"><strong>Name</strong></label>
        <input type="text" v-model="enteredName" >
        <label for=""  ><strong>Phone</strong></label>
        <input type="text" v-model="enterdPhone">
        <label for=""  ><strong>Email</strong></label>
        <input type="text" v-model="enteredEmail">

        <button >Submit</button>
    </form>
</template>

<script>
    export default {
        data() {
            return {
                enteredName: '',
                enterdPhone: '',
                enteredEmail: ''
            }
        },
        methods: {
            submitData(){
                this.$emit('add-contact', this.enteredName,this.enterdPhone,this.enteredEmail)
            }
        }
    }
</script>

<style>
    form {
        display: flex;
        flex-direction: column;
         box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
         margin: 1rem auto;
         border-radius: 10px;
         padding: 1rem;
         text-align: center;
         width: 90%;
         max-width: 40rem;
    }
</style>