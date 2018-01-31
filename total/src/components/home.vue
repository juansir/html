<template>
	<div id="app">
		<header id="head">
			<div class="logo">
				<a href="#">协助科技<p>XIE ZHU TECHNOLOGY</p></a>
			</div>
	  		<ul class="ul">
		  		<li><a href="">首页</a><span>|</span></li>
		  		<li><a href="">酒店方案</a><span>|</span></li>
		  		<li><a href="">产品</a><span>|</span></li>
		  		<li><a href="">合作加盟</a><span>|</span></li>
		  		<li><a href="">新闻动态</a><span>|</span></li>
		  		<li><a href="">管理平台</a><span>|</span>
		  			<div class="guan">
		  				<a href="">酒店管家</a>
		  				<a href="">携住论坛</a>
		  			</div>
		  		</li>
		  		<li><a href="">我们</a></li>
		  	</ul>
	  	</header>
		<nav class="banner">
			<ul class="img">
			    <li><a href="#">
			    	<img src="../../images/banner1.jpg">
			    	<img class="font" src="../../images/banner1_fonts.png" />
			    </a></li>
			    <li><a href="#">
			    	<img src="../../images/banner2.jpg">
			    	<img class="font" src="../../images/banner2_fonts.png" />
			    </a></li>
			    <li><a href="#">
			    	<img src="../../images/banner1.jpg">
			    	<img class="font1" src="../../images/banner3_fonts.png" />
			    	<img class="font2" src="../../images/banner3_phone.png" />
			    </a></li>
			    <li><a href="#"><img src="../../images/banner4.png"></a></li>
			</ul>
			<ul class="num">
				<li></li>
				<li></li>
				<li></li>
				<li></li>
			</ul>
		</nav>
		<vv></vv>
		<ff></ff>
	</div>
	
</template>

<script>
	import v from  './Homeview'
	import f from  './Footer'
	export default {
	  components:{
	    'vv' : v,
	    'ff' : f,
	  }
	}
	
	$(function(){
		$('.ul li').eq(5).mouseover(function(){			
			$('#head').css('background-color','#fff')
			$('.logo a').css('color','#000')
			$('.ul li a').css('color','#000')
			$('.ul li .guan').css('display','block')
		})
		$('.ul li').eq(5).mouseleave(function(){			
			$('#head').css('background-color','')
			$('.logo a').css('color','#fff')
			$('.ul li a').css('color','#fff')
			$('.ul li .guan').css('display','')
		})
		
		console.log($('#head').offset().top)
		if($('#head').offset().top<0){
			$(this).css('background-color','#fff')
			$('.logo a').css('color','#000')
			$('.ul li a').css('color','#000')
		}
		
		var i=0;
		var clone=$(".banner .img li").first().clone();
		$(".banner .img").append(clone);	
		var size=$(".banner .img li").length;	
		$(".banner .num li").first().addClass("on");
		
	
		/*鼠标划入圆点*/
		$(".banner .num li").hover(function(){
			var index=$(this).index();
			i=index;
			$(".banner .img").stop().animate({left:-index*100+'vw'},500)	
			$(this).addClass("on").siblings().removeClass("on")		
		})
		/*自动轮播*/
		var t=setInterval(function(){
			i++;
			move()
		},2000)
		
		
		/*对banner定时器的操作*/
		$(".banner").hover(function(){
			clearInterval(t);
		},function(){
			t=setInterval(function(){
				i++;
				move()
			},2000)
		})
	
		function move(){
			if(i==size){
				$(".banner  .img").css({left:0})			
				i=1;
			}
			if(i==-1){
				$(".banner .img").css({left:-(size-1)*100 +'vw'})
				i=size-2;
			}
			$(".banner .img").stop().animate({left:-i*100 +'vw'},500)
			
			if(i==size-1){
				$(".banner .num li").eq(0).addClass("on").siblings().removeClass("on")	
			}else{		
				$(".banner .num li").eq(i).addClass("on").siblings().removeClass("on")	
			}
		}
		
	})
	
</script>

<style scoped>
	/*header*/
	#head{
		border-bottom: 1px solid #eee;
	    color: #fff;
	    position: fixed;
	    width: 100vw;
	    height: 6vw;
	    line-height: 6vw;
	    z-index:99;
	    top: 0;
	    font-size: 14px;
	}
	.logo{
		width:40%;
		float: left;
		padding-top: 1%;
	}
	.logo a{
		display:block;
		height:6vw;
		line-height:2.2vw;
		background: url(../../images/websit-logo.jpg) no-repeat 30% top;
		background-size:15% ;
		padding-left:40% ;
		font-size: 2.2em;
		color: #fff;
	}
	.logo p{
		font-size:0.1em;
	}
	.ul{
		width: 60%;
	    color: #fff;
	    vertical-align: middle;
	    display: inline-block;
	    float: right;
	    cursor: pointer;
	}
	.ul li{
		width: 14%;
	    text-align: center;
	    float: left;
	    position: relative;
	}
	.ul li a{
		display: block;
	    width: 100%;
	    height: 100%;
	    color: #fff;
	}
	.ul li span{
		position: absolute;
	    top:-2%;
	    right: 0;
	    width:0;
	    font-size: 1.2em;
	}
	.ul li .guan{
		background: #fff;
		border-radius: 2px;
		display: none;
	}
	.ul li .guan a{
		color:#000;
		line-height: 3vw;
	}
	.ul li .guan a:hover{
		color:orange;
	}
	/*nav*/
	.banner{
		width:100vw;
		height: 45vw;
    	position: relative;
    	overflow: hidden;
	}
	.img{
		width:500vw;
		position:absolute;
	}
	.img li{
		width:100vw;
		float: left;
		position: relative;
    	overflow: hidden;
	}
	.img img{
		max-width: 100%!important;
    	vertical-align: middle;
	}
	.font{
		width: 22%;
    	left: 39%;
    	top: 40%;
    	position:absolute;
	}
	.font1{
		width: 22%;
    	left: 30%;
    	top: 40%;
    	position:absolute;
	}
	.font2{
		width: 30%;
    	left: 53%;
    	top: 20%;
    	position:absolute;
	}
	.banner .num{ 
		position:absolute; 
		width:100vw;
		height: 0.5vw; 
		bottom:6vw; 
		left:0; 
		text-align:center; 
	}
	.banner .num li{ 
		width:3vw;
		height:0.5vw; 
		background:rgba(255,255,255,0.6); 
		border-radius:1em; 
		display:inline-block; 
		margin:0 4px; 
		cursor:pointer;
	}
	.banner .num li.on{background:#454545;}
</style>