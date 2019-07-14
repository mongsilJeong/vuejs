<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="header">
      <h1 class="headerText">SSG 상품 상세</h1>
      <nav>
        <ul>
          <li>
            <a href="#" @click="changeMenu('itemOnlineView')">온라인</a>
          </li>
          <li>
            <a href="#" @click="changeMenu('itemDptsView')">백화점</a>
          </li>
          <!--
          <li>
            <a href="#" @click="changeMenu('contact')">Contact</a>
          </li> -->
        </ul>
      </nav>
    </div>
    <div class="container">
      <keep-alive include="itemOnlineView,itemDptsView">
        <component v-bind:is="currentView"></component>
      </keep-alive>
    </div>
  </div>
</template>

<script>

import itemOnlineView from './components/ItemOnlineView.vue';
import itemDptsView from './components/ItemDptsView.vue';

export default {
  name: 'app',
  components : {itemOnlineView, itemDptsView} ,
  data(){
    return{currentView : 'itemOnlineView'}
  } ,
  methods : {
    changeMenu(view) {
      this.currentView = view;
    }
  }
}
</script>

<style scoped>
.header { background-color:rgb(169, 216, 255); padding: 10px 0px 0px 0px; }
.headerText { padding: 0px 20px 0px 20px; } 
ul { list-style-type: none; margin: 0; padding: 0;
    overflow: hidden; background-color: purple;  }
li { float: left; }
li a { display: block; color: yellow; text-align: center;
    padding: 14px 16px; text-decoration: none;  }
li a:hover { background-color: aqua; color:black; }
</style>
