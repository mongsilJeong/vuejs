<template>
  <div>
    <item-header :headerText="header.name">
        <div slot="content">
            <div>
                <label class="control-label">상품명</label>
                <input type="text"/>
            </div>
            <div>
                <label class="control-label">다국어명</label>
                <input type="text"/>
            </div>
        </div>
    </item-header>
  </div>
</template>
<script>

import ItemHeader from '../uiComponent/header.vue';

export default {
  name: 'ItemBasicInfoView' ,
  components : {ItemHeader} ,
  data : function() {
      return {
          header : {
              name : "상품정보"
          }
      }
  } ,
  methods : {
      toggle : function(){

      }
  }
}
</script>
<style scoped>
.control-label { float: left; width: 180px; }
</style>