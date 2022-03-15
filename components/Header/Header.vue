<template>
  <div class="contenier">
    <div class="hearer_menu">
      <ul class="listUL" v-for="item in menu" :key="item">
        <NuxtLink to="/" class="links">{{item}}</NuxtLink> </ul>
      <span class="Contact">Contact</span>
    </div>

  </div>
</template>

<script>
const listmenu  = require('../../constant/constant')
  export default {
    data () {
      return {
        menu: listmenu.manuList
      }
    },
    mounted () {
      console.log(this.menu);
    }
    
  }
</script>

<style lang="css" scoped>
.links{
  list-style-type:none;
}
.listUL {
  list-style-type: none;
  display: flex;
  gap: 20px;
  padding: 15px;
font-family: 'Poppins';
font-style: normal;
font-weight: 500;
font-size: 16px;
line-height: 24px;
color: #fff;
display: flex;
justify-content:center;
}
.Contact {
  display: flex;
flex-direction: row;
justify-content: left;
align-items: center;
padding: 22px 40px;

position: absolute;
left: 78.12%;
right: 12.5%;
top: 3.23%;
bottom: 98.99%;

/* Green_01 */

background: #3DB079;
border-radius: 8px;
color: #fff;
}

</style>