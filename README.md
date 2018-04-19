# bootstrap-Table
### bootstrap table中实现可拖动的表格列

说明：引用文件colResizable-1.6.js和bootstrap-table-resizable.js

---

使用：

项目中初始化

```
<script type="text/javascript">
	$(function() {
		$("table").colResizable();
	})
</script>
```

### colResizable-1.6.js API使用：

_resizeMode：[type：string] [default：’fit’] [version：1.6] [values：’fit’，’flex’，’overflow’]_

‘fit’：这是默认的调整大小模型，其中调整列的大小不会改变表宽度，这意味着当列扩展时，下一个缩放。 
‘flex’：在此模式下，如果父容器中有足够的空间，表可以更改其宽度，每列可以独立缩小或扩展。如果没有足够的空间，列将会调整其宽度。表不会比其父母大得多。 
‘overflow’：允许使用父容器溢出来调整列的大小。

_disable：[type：boolean] [default：false] [version：1.0]_

当设置为true时，它旨在将所有以前添加的增强功能（如事件和此插件分配的其他DOM元素）删除到单个或集合的表中。在使用JavaScript从文档对象树中删除之前，还需要先将colResized表禁用到已经colResized表的任何DOM操作之前，例如添加列，行等。

_disabledColumns：[type：int of int] [default：[]] [version：1.6]_

要排除的列索引数组，因此无法手动拖动。

_liveDrag：[type：boolean] [default：false] [version：1.0]_ 

当设置为true时，将在拖动列锚点时更新表格布局。启用liveDrag的CPU耗费更多，因此不推荐用于较慢的计算机，特别是在处理巨大或非常复杂的表时。

_postbackSafe：[type：boolean] [default：false] [version：1.3]_

此属性可用于指定在回发或浏览器刷新后，手动选择的列宽度必须保持不变。此功能主要面向使用服务器端逻辑（codebehind）创建的页面，例如PHP或.NET，它仅与具有sessionStorage支持的浏览器（所有现代浏览器）兼容。但是，如果您定位较早的浏览器（如IE7和IE8），则仍可以使用sessionStorage.js来模拟sessionStorage。请注意，有些浏览器（IE和FF）在直接从本地文件系统运行网站时不启用sessionStorage对象，因此如果要测试此功能，建议您通过Web服务器查看网站或使用Chrome或Opera等不受此限制的浏览器。不要担心兼容性问题，

_partialRefresh：[type：boolean] [default：false] [version：1.5]_

如果表位于updatePanel内部或使用ajax进行的任何其他类型的部分页面刷新，则此属性应设置为true。表的ID在部分部分刷新之前和之后应该相同。

_innerGripHtml：[type：string] [default：empty string] [version：1.0]_

其目的是通过定义要在列中使用的HTML来提供一些视觉反馈来允许列锚定制。它可以以广泛的方式用于获得非常不同的输出，并且可以通过将其与draggingClass属性相结合来增加其灵活性。

_draggingClass：[type：string] [default：internal css class] [version：1.0]_ 

该属性被用作被拖动时分配给列锚的css类。它可以用于视觉反馈目的。

_minWidth：[type：number] [default：15] [version：1.1]_ 

该值指定列允许的最小宽度（以像素为单位）。

_headerOnly：[type：boolean] [default：false] [version：1.2]_

此属性可用于防止柱锚的垂直展开以适应桌面高度。如果设置为true，列处理程序的大小将被绑定到第一行的垂直大小。

_hoverCursor：[type：string] [default：“e-resize”] [version：1.3]_ 

此属性可用于自定义当用户位于列锚上时将显示的游标。

_dragCursor：[type：string] [default：“e-resize”] [version：1.3]_

定义用户调整列大小时将使用的游标。
