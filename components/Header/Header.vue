<template>
  <div> 
      <header>
      <img class="logo" :src="img" alt="this img yet">
     <nav>
        <ul class="nav_ul" >
          <span v-for="item in menu" :key="item">
            <NuxtLink class="nuxt_link" :to="item.link">{{item.name}}</NuxtLink>
          </span>
          
        </ul>
     </nav>
      <a><button class="button_contact">Contact</button></a>
      </header>

  </div>
</template>

<script>
import imgLogo from '../../images/Group.svg'
const listmenu  = require('../../constant/constant')
  export default {
    data () {
      return {
        menu: listmenu.manuList,
        img: imgLogo
      }
    },
    mounted () {
      console.log(this.menu);
    }
    
  }
</script>

<style lang="scss" scoped>
header {
  display:flex;
  justify-content: space-around;
  align-items: center;
}
.nuxt_link {
  text-decoration: none;
  display: flex;

}
.nuxt_link:hover {
  border-bottom: 2px solid #fff;
}
.nav_ul {
  display: flex;
  gap: 20px;
}
.button_contact{
  display: flex;
flex-direction: row;
justify-content: center;
align-items: center;
padding: 22px 40px;

position: absolute;
left: 78.12%;
right: 12.5%;
top: 1.23%;
bottom: 98.99%;

/* Green_01 */
border: none;

background: #3DB079;
border-radius: 8px;
}
.button_contact:hover{
  color: blue;
  margin-top: 2px;
}
.logo {
  // margin-right: -30px;
}
</style>