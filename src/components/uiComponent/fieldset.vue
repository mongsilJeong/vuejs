<!-- 헤더 밑에 slot 이 있고, header 누르면 slot show/hide 가능-->
<template>
  <div id="form-sub-wrap">
    <table>
        <tr>
            <td class="control-label">{{headerText}}</td>
            <td>
                <input type="radio" :id="radioBtnId" :name="radioBtnName" @click="isEnable = true"/><label>설정함</label>
                <input type="radio" :id="radioBtnId" :name="radioBtnName" @click="isEnable = false"/><label>설정안함</label>
            </td>
        </tr>
    </table>
    <slot name="form-sub-detail" v-if="isEnable" ></slot>
  </div>
</template>

<script>
export default {
    name : 'FieldSet' ,
    props : [ 'headerText', 'radioBtnId', 'radioBtnName' ] ,
    data : function (){
        return {
            isEnable : false ,
            radioBtnId : this.radioBtnId ,
            radioBtnName : this.radioBtnName
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
.control-label { float: left; width: 180px; }
</style>