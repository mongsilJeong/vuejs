<template>
  <div>
    <item-header :headerText="header.name">
        <div slot="content">
            <div>
                <label class="control-label">판매가</label>
                <input type="text"/>
            </div>
            <field-set headerText="할인" radioBtnId="enableDiscountPrice" radioBtnName="enableDiscountPrice">
                <div slot="form-sub-detail" class="form-sub-detail">
                    <label class="control-label">전체 할인</label>
                    <input type="text"/>
                </div>
            </field-set>
            <field-set headerText="판매기간" radioBtnId="enableSellDts" radioBtnName="enableSellDts">
                <div slot="form-sub-detail" class="form-sub-detail">
                    <label class="control-label">기간설정</label>
                    <input type="button" value="3일"/>
                </div>
            </field-set>
        </div>
    </item-header>
  </div>
</template>
<script>

import ItemHeader from '../uiComponent/header.vue';
import FieldSet from '../uiComponent/fieldset.vue';

export default {
  name: 'SellPrcInfoView' ,
  components : {ItemHeader, FieldSet} ,
  data : function() {
      return {
          header : {
              name : "가격정보"
          }
      }
  }
}
</script>
<style scoped>
.control-label { float: left; width: 180px; }
.form-sub-detail {background-color : rgb(226, 226, 226)}
</style>