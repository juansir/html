<template>
	<div id="app">
		<section>
			<div class="view"> 
				<a href="#">
					<div class='div'>
						<img src="../../images/home1.png" />
					</div>
				</a>
				<a href="#">
					<div class='div'>
						<img src="../../images/home2.png" />
					</div>
				</a>
				<a href="#">
					<div class='div'>
						<img src="../../images/home3.png" />
					</div>
				</a>
			</div>
			<!--news新闻-->
			<div class="news">
				<p>新闻<span>动态</span></p>
				<div class="newsp">
					<div class="left"><h2>相信·看见2018携住科技新品发布暨感恩答谢会圆满结束！</h2>2018.1.18<br />
						<p>2018年1月16日，相信·看见2018携住科技新品发布暨感恩答谢会，在苏州日航酒店盛大召开。本次盛会不仅是携住科技自己人的年度盛典更是酒店人的共同盛会！来自全国各地的酒店行业代表齐聚日航，原锦江集团高级副总裁张兴国先生、国际饭店业职业经理人协会副秘书长张经邦先生、同程旅游酒店事业部CEO叶俊等嘉宾重磅亮相，共同见证大会盛况。</p>
					</div>
					<ul class="center">
						<li><p>参会流程 | 欢迎参加2018相信·看见携住科技新品发布暨感恩答谢会！</p>2018.1.14</li>
						<li><p>共话未来酒店 | 金陵集团携旗下三十余家酒店高管赴携住总部观摩</p>2018.1.3</li>
						<li><p>智慧标杆 | 贵阳市各级领导参观体验携住智慧酒店</p>2017.12.25</li>
						<li><p>酒店业：这是一个智能时代</p>2017.12.19</li>
					</ul>
					<div class="right">
						<img src="../../images/home4.png" />
					</div>
				</div>
			</div>
			<!--更多按钮-->
			<div class='more'>
				<a href="">了解更多&nbsp;&nbsp;&nbsp;→</a>
			</div>
			<div class='zhannue'>
				<p>战略<span>合作</span></p>
				<div class='company'>
					<div><img src="../../images/keda.jpg" /></div>
					<div><img src="../../images/dianxin.jpg" /></div>
					<div><img src="../../images/aliyun.jpg" /></div>
					<div><img src="../../images/meadin.jpg" /></div>
					<div><img src="../../images/liantong.png" /></div>
					<div><img src="../../images/texas.jpg" /></div>
					<div><img src="../../images/lvyun.jpg" /></div>
					<div><img src="../../images/clear.jpg"/></div>
				</div>
			</div>
			<div class='hotel'>
				<p>部分合作<span>酒店</span></p>
				<div class='foot'>
					<div><img src="../../images/baolong.png" /></div>
					<div><img src="../../images/boyue.png" /></div>
					<div><img src="../../images/gelan.png" /></div>
					<div><img src="../../images/haiwaihai.png" /></div>
					<div><img src="../../images/jinling.png" /></div>
					<div><img src="../../images/kaiyuan.png" /></div>
					<div><img src="../../images/shanshui.png" /></div>
					<div><img src="../../images/shuxiang.png" /></div>
					<div><img src="../../images/tujia.png" /></div>
					<div><img src="../../images/wanxin.png" /></div>
					<div><img src="../../images/yaduo.png" /></div>
					<div><img src="../../images/yinju.png" /></div>
				</div>
			</div>
		</section>
	</div>
	
</template>

<script>
	$(function(){
		//1.
		$('.company div img').mouseover(function(){
			$(this).animate({width:'100%'},'slow')
		});
		$('.company div img').mouseleave(function(){
			$(this).animate({width:'90%'},'slow')
		});
		//2.
		$('.foot img').mouseover(function(){
			$(this).animate({top:'-10%'},'fast')
		});
		$('.foot img').mouseleave(function(){
			$(this).animate({top:''},'fast')
		});
	})
</script>

<style scoped>
	.view{
		width: 100%;
		overflow: hidden;
	}
	.view a{
		position: relative;
	    float: left;
	    display: inline-block;
	    width: 33%;
	    height: 100%;
	}
	.view a:nth-child(2){
		margin-left:0.5%;
		margin-right: 0.5%;
	}
	.view .div{
		width: 100%;
		height: 100%;
		overflow: hidden;
	    position: relative;
	}
	.view .div img{
		width:100%;
	}
	/*news*/
	section{
		width: 100vw;
	}
	.news{
		width: 100%;
    	overflow: hidden;
	}
	.news p{
		font-size: 2em;
		text-align: center;
    	margin: 3em 0;
	}
	.news span{
		color: #c5a47e;
	}
	.left{
		width:30%;
		float: left;
	}
	.center{
		width:30%;
		float: left;
		margin-left: 5%;
		margin-right: 5%;
	}
	.right{
		width:30%;
		float: left;
	}
	.more{
		width: 100%;
		margin: 0 auto;
	}
	.more a{
		width:20%;
		height:3vw;
		line-height:3vw;
		display:block;
    	margin: 6vw auto 10vw;
    	border-radius: 1vw;
    	background-color: #C5A47E;
    	color: #fff;
    	letter-spacing: 0.3em;
    	text-align: center;
	}
	.zhannue{
		width: 100%;
		text-align: center;
    	overflow: hidden;
    	background-color: rgb(39, 39, 39);
	}
	.zhannue p{
		font-size: 2em;
		color: #fff;
		text-align: center;
    	margin: 3em 0;
	}
	.zhannue span{
		color: #c5a47e;
	}
	.company{
		width: 70%;
		margin:0 auto;
	}
	.company div{
		width: 25%;
		height: 10vw;
		float: left;
		text-align: center;
		margin-bottom:3%;
	}
	.company div img{
    	width: 90%;	
	}
	.hotel{
		width: 100%;
		margin:2vw;
		text-align: center;
    	overflow: hidden;
	}
	.hotel p{
		font-size: 2em;
		text-align: center;
    	margin: 3em 0;
	}
	.hotel span{
		color: #c5a47e;
	}
	.foot{
		width: 100%;
	}
	.foot div{
		float: left;
		width: 16%;
		height: 15vw;
		text-align: center;
		margin-bottom:3%;
		position:relative;
		left: 0;
	}
	.foot img{
		width: 100%;
		position:absolute;
		left: 0;
	}
	.newsp{
		width: 90%;
		margin: 0 auto;
	}
	.left{
		font-size: 0.9em;
		cursor: pointer;
	}
	.left h2{
		font-size: 1.3em;
		font-weight: normal;
	}
	.left p{
		font-size: 0.9em;
    	margin-top: 2em;
    	line-height: 1.6em;
    	text-align: left;
	}
	.center>li{
		font-size:0.9em;
		margin-bottom:2vw;
		position:relative;
		cursor: pointer;
	}
	.center>li>p{
		font-size:0.9em;
		margin:0;
		text-align: left;
	}
	.center>li>p:hover{
		transition:0.5s;
		font-size:1.1em;
		color:#c5a47e;
	}
</style>