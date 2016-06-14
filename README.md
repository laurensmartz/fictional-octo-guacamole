关于onmouseover（onmouseout）和onmouseenter（onmouseleave）的不同
1.onmouseover会被目标元素内的子元素捕获，而onmouseenter不会被目标元素内的子元素捕获。
例如：\<li\>
        <a href="\"></a>
      </li>
      假设给上面这个li（父元素）添加了onmouseover和onmouseout事件，那么当鼠标从li元素移动到a元素内的时候就会触发li元素的onmouseout事件，同时触发a元素的onmouseover事件（因为a元素被li元素的onmouseover和onmouseout事件捕获了，所以a元素也就同时具有了onmouseover和onmouseout事件属性）。由此可以推导出当鼠标从a元素移动到li元素里时，首先触发了a元素的onmouseout事件，紧接着触发了li元素的onmouseover事件。同样的例子如果换成onmouseenter和onmouseleave事件则li元素内的a元素不会被捕获，所有就算从li元素移入a元素或者从a元素移入li元素也不会发生任何事情。
