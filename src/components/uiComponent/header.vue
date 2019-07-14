<!-- 헤더 밑에 slot 이 있고, header 누르면 slot show/hide 가능-->
<template>
  <div class="container">
    <div class="header" @click="toggle()">{{headerText}}</div>
    <transition name="fade">
        <div class="content" v-if="isOpen">
            <slot name="content"></slot>
        </div>
    </transition>
  </div>
</template>

<script>
export default {
    name : 'ItemHeader' ,
    props : [ 'headerText' ] ,
    data : function (){
        return {
            isOpen : false
        }
    } ,
    methods : {
        toggle : function() {
            this.isOpen = !this.isOpen;
        }
    }
}
</script>

<style scoped>
.container { margin:10px; padding:2px;
    border:solid 1px gray; }
.header { padding:4px 20px 4px 20px; background-color : #A93226;
    color:white; text-align: left; font-weight: bold; font-size: 22px;}
.footer { padding:4px 20px 4px 20px; background-color: aqua; 
    text-align:left; }
.content { padding: 10px; height:auto; min-height: 40px;
    text-align:left; }
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>