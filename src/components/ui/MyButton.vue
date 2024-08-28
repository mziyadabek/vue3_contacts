<template>
    <button class="btn">
        <slot>
          
        </slot>
    </button>
</template>

<script>
  export default{
    name: 'my-btn',
  }
</script>

<style scoped>
.btn {
  margin-top: 15px;
  padding: 10px 15px;
  border-radius: 12px;
  color: white;
  border: none;
  background-color: rgb(241, 71, 99);

}
</style>