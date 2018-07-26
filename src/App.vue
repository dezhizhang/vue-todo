<template>
  <div class='container'>
    <form role='form'>
       <div class='form-group'>
         <label from='username'>用户名</label>
         <input type='text' class='form-control'/>
       </div>
    </form>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>

</style>
