## Name:    ZhengYuanchun(Tandy)
## Date:    2015-09-27 10:12
## Note:    这是一个仿照Pinterest网站的简单实用的响应式网格瀑布流式布局JQuery插件。

	使用方式：
	1.<script src='js/juqery.min.js'></script>
	  <script src='js/jailswall.js></script>
	
	2.用<div>容器包裹需要部署的内容。
	  <div class="wall">
 	    <a class="wall-item" href="#">
              <img src="1.jpg">
              <h2>wall-item 1</h2>
 	    </a>
 
  	    <a class="wall-item" href="#">
    	      <img src="2.jpg">
              <h2>wall-item 2</h2>
            </a>
 
            <a class="wall-item" href="#">
              <img src="3.jpg">
              <h2>wall-item 3</h2>
            </a>
 
 		 ...
   
	  </div>      
		
	3.style样式
	  .article {
	  display: block;
	  margin: 0 0 30px 0;
	  padding: 12px;
	  background: white;
	  border-radius: 3px;
	  box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.05);
	  transition: all 220ms;
	  }
	.article:hover {
	  box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.1);
	  transform: translateY(-5px);
	  transition: all 220ms;
	  }	
	.article > img {
	  display: block;
	  width: 100%;
	  margin: 0 0 24px 0;
	  }
	.article h2 {
	  text-align: center;
	  font-size: 14px;
	  text-transform: uppercase;
	  margin: 0 0 12px 0;
	 }
 
	.wall {
	  display: block;
	  position: relative;
	  }
	.wall-column {
	  display: block;
	  position: relative;
	  width: 25%;
	  float: left;
	  padding: 0 12px;
	  box-sizing: border-box;
	  }
	@media (max-width: 640px) {
	  .wall-column {
	    width: 50%;
	  }
 	  }
	@media (max-width: 480px) {
	  .wall-column {
	    width: auto;
	    float: none;
	  }
	  }           
	其中.wall-column 的 width属性用于控制每行显示多少列。

	4.初始化插件
	$(function(){
	  $('.wall').jaliswall();
	});
