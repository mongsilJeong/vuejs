<template>
  <div>
    <h1>백화점</h1>
    <item-basic-info-view></item-basic-info-view>
  </div>
</template>
<script>
import ItemBasicInfoView from './cotentComponent/itemBasicInfo.vue';

export default {
  name: 'itemDptsView' ,
  components : {ItemBasicInfoView}
}
</script>
