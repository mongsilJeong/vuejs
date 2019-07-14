<template>
  <div>
    <h1>온라인</h1>
    <item-basic-info-view></item-basic-info-view>
    <sell-prc-info-view></sell-prc-info-view>
  </div>
</template>
<script>

import ItemBasicInfoView from './cotentComponent/itemBasicInfo.vue';
import SellPrcInfoView from './cotentComponent/sellPrcInfo';
export default {
  name: 'itemOnlineView' ,
  components : {ItemBasicInfoView, SellPrcInfoView}
}
</script>