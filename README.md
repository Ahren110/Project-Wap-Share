# Project-Wap-Share

>移动Wap端分享组件，集合了分享到新浪微博，QQ空间，以及生成二维码的功能


##如何使用

项目依赖于jQuery或者Zepto（移动端，后者使用居多），因此要先引入它们

	<script src='js/zepto.min.js'></script>
	<script src='js/SFE.mShare.js'></script>

然后，调用init方法


	<script type="text/javascript">
	    share.init({
	        title:"分享到",   //可选，默认为"分享到"
	        maskLayer:true,    //可选，遮罩层，默认为true
	        needCancel:true,  //可选，取消按钮，默认为true
	        shareTo:{
	            wb:{    //可选
	                type:"新浪微博",
	                description:"这里是分享出去的内容",
	                url:"分享的链接",
	                imgUrl:"分享的图片地址"
	            },
	            kj:{   //可选
	                type:"QQ空间",
	                title:"QQ有可选的分享标题",
	                description:"这里是分享出去的内容",
	                url:"分享的链接",
	                imgUrl:"分享的图片地址"
	            },
	            wm:{   //可选
	                type:"生成二维码",
	                url:"要生成二维码的链接"
	            }
	        }
	    });

	    //触发
	    btn.ontouchstart = function(e){
	            share.open();      //打开分享按钮
	    };
	</script>
