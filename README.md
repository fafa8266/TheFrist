# TheFrist
这是我的第一个仓库
准备在这里留下我第一段代码，留下一段ztree的代码吧！


<div class="panel-body">
    <div class="e-persons-search">
      <span class="e-persons-search-i" id="searchBtn"><i
        class="fa fa-search"></i></span> <input type="text"
        class="form-control e-persons-search-t" id="key"
        placeholder="<fmt:message key='bms.materiel.searchMateriel'/>">
    </div>
    <div class="e-persons-search-l">
      <ul id="treeDemo" class="ztree"></ul>
    </div>  
</div>


<script>
  var setting = {
		data: {
			key: {
				name: "materialId"
			},
			simpleData: {
				enable:true,
				idKey: "id",
				pIdKey: "materialParentId",
				rootPId: ""
			}
		},
		view: {
			showLine: true,
			selectedMulti: false,
			dblClickExpand: false,
			fontCss: setFontCss_ztree ,
			expandSpeed: ""
		},
		callback: {
			onClick: onClickFunc,
			onAsyncSuccess: selectedNodes,
       }
	};
  function onClickFunc(event,treeId,treeNode){
    //do something
  }
  function selectedNodes()(event,treeId,treeNode){
    //do something
  }
  
  //加载树形菜单
	$(document).ready(function(){
    $.fn.zTree.init($("#treeDemo"), setting,materialDatas);

  });
  
</script>
