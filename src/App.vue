<template>
  <h1>cooking-vue-start</h1>
  <p>A vue project.</p>
  <dialog :title="dialog.title" :content="dialog.content" :btntype="dialog.btntype" :showstatus.sync="dialog.showstatus"></dialog>
  <a href="javascript:void(0)" @click="onShow">显示</a>
</template>

<script>
  import dialog from 'vue-dialog_xiaomingming/src/dialog.vue'	
  export default {
    name: 'app',
	components: {
       dialog
    },
    data(){
    	return {
    		dialog:{
    			title:"这是标题",
    			content:"这是内容",
    			modalId:1,
    			btntype:2,
    			showstatus:false
    		}
    		
    	}
    },
    methods:{
    	onShow(){
    		this.dialog.showstatus = true;
    	}
    },
    events:{
    	OK_EVENT(){
    		alert(this.dialog.modalId)
    	}
    }
  };
</script>
