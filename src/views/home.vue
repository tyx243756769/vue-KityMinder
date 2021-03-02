<template>
<div>
    <h1 style="text-align: center;">测试</h1>
    <div style="height: 89.5vh;background: #e1e1e1;">
    	<kityminder-editor on-init="initEditor(editor, minder)"></kityminder-editor>
    	<!--<div id='vue-KityMinder' @on-init="initEditor(editor, minder)" style="width: 100%;height: 100%;"></div>-->
    </div>
</div>
</template>

<!-- bower:js -->
<!--<script src="bower_components/jquery/dist/jquery.js"></script>
<script src="bower_components/bootstrap/dist/js/bootstrap.js"></script>-->
<script src="../../bower_components/angular/angular.js"></script>
<script src="../../bower_components/angular-bootstrap/ui-bootstrap-tpls.js"></script>
<!--<script src="bower_components/codemirror/lib/codemirror.js"></script>
<script src="bower_components/codemirror/mode/xml/xml.js"></script>
<script src="bower_components/codemirror/mode/javascript/javascript.js"></script>
<script src="bower_components/codemirror/mode/css/css.js"></script>
<script src="bower_components/codemirror/mode/htmlmixed/htmlmixed.js"></script>
<script src="bower_components/codemirror/mode/markdown/markdown.js"></script>
<script src="bower_components/codemirror/addon/mode/overlay.js"></script>
<script src="bower_components/codemirror/mode/gfm/gfm.js"></script>-->
<script src="../../bower_components/angular-ui-codemirror/ui-codemirror.js"></script>
<!--<script src="bower_components/marked/lib/marked.js"></script>-->
<script src="../../node_modules/kity/dist/kity.js"></script>
<script src="../../bower_components/hotbox/hotbox.js"></script>
<!--<script src="bower_components/json-diff/json-diff.js"></script>-->
<script src="../../node_modules/kityminder-core/dist/kityminder.core.js"></script>
<script src="../../bower_components/color-picker/dist/color-picker.js"></script>
<script src="../../bower_components/seajs/dist/sea.js"></script>

<script src="../../ui/kityminder.app.js"></script>
<script src="../../ui/service/commandBinder.service.js"></script>
<script src="../../ui/service/config.service.js"></script>
<script src="../../ui/service/memory.service.js"></script>
<script src="../../ui/service/lang.zh-cn.service.js"></script>
<script src="../../ui/service/valueTransfer.service.js"></script>
<script src="../../ui/service/minder.service.js"></script>
<script src="../../ui/service/resource.service.js"></script>
<script src="../../ui/service/revokeDialog.service.js"></script>
<script src="../../ui/service/server.service.js"></script>
<script src="../../ui/filter/lang.filter.js"></script>
<script src="../../ui/dialog/hyperlink/hyperlink.ctrl.js"></script>
<script src="../../ui/dialog/image/image.ctrl.js"></script>
<script src="../../ui/dialog/imExportNode/imExportNode.ctrl.js"></script>
<script src="../../ui/directive/topTab/topTab.directive.js"></script>
<script src="../../ui/directive/undoRedo/undoRedo.directive.js"></script>
<script src="../../ui/directive/appendNode/appendNode.directive.js"></script>
<script src="../../ui/directive/arrange/arrange.directive.js"></script>
<script src="../../ui/directive/operation/operation.directive.js"></script>
<script src="../../ui/directive/hyperLink/hyperLink.directive.js"></script>
<script src="../../ui/directive/imageBtn/imageBtn.directive.js"></script>
<script src="../../ui/directive/noteBtn/noteBtn.directive.js"></script>
<script src="../../ui/directive/resourceEditor/resourceEditor.directive.js"></script>
<script src="../../ui/directive/priorityEditor/priorityEditor.directive.js"></script>
<script src="../../ui/directive/progressEditor/progressEditor.directive.js"></script>
<script src="../../ui/directive/noteEditor/noteEditor.directive.js"></script>
<script src="../../ui/directive/notePreviewer/notePreviewer.directive.js"></script>
<script src="../../ui/directive/kityminderEditor/kityminderEditor.directive.js"></script>
<script src="../../ui/directive/templateList/templateList.directive.js"></script>
<script src="../../ui/directive/themeList/themeList.directive.js"></script>
<script src="../../ui/directive/layout/layout.directive.js"></script>
<script src="../../ui/directive/styleOperator/styleOperator.directive.js"></script>
<script src="../../ui/directive/fontOperator/fontOperator.directive.js"></script>
<script src="../../ui/directive/expandLevel/expandLevel.directive.js"></script>
<script src="../../ui/directive/selectAll/selectAll.directive.js"></script>
<script src="../../ui/directive/colorPanel/colorPanel.directive.js"></script>
<script src="../../ui/directive/navigator/navigator.directive.js"></script>
<script src="../../ui/directive/searchBox/searchBox.directive.js"></script>
<script src="../../ui/directive/searchBtn/searchBtn.directive.js"></script>
<script>
import Vue from 'vue';
import 'vue';
export default{
    data: ()=> {
        return {
        	km:null
        };
    },
    components: {
    },
    created () {
    	var km = window.km = new kityminder.Minder();
	    km.setup('#vue-KityMinder');
//	    km.disable();
//	    km.execCommand('hand');
//	    
//  	var minder = new kityminder.Minder({
//				renderTo: '#vue-KityMinder'
//			});
//			console.log(minder)
			km.importJson({
			  "root": {
			    "data": {
			      "text": "test111"
			    },
			    "children": [
			      { "data": { "text": "新闻\nsrc/module/node.j"}},
			      { "data": { "text": "网页"} },
			      { "data": { "text": "贴吧"} },
			      { "data": { "text": "知道"} },
			      { "data": { "text": "音乐" } },
			      { "data": { "text": "图片"} },
			      { "data": { "text": "视频"} },
			      { "data": { "text": "地图" } },
			      { "data": { "text": "百科","expandState":"collapse"}}
			    ]
			  },
			  "template":"default"
			});
    },
    mounted () {
    },
    computed: {},
    methods: {
    	initEditor(editor, minder) {
    		console.log(1111111)
					window.editor = editor;
					window.minder = minder;
			}
    },
}
</script>
<style>
</style>