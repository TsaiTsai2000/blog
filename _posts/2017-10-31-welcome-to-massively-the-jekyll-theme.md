---
layout: post
title:  "Welcome to Massively: The Jekyll Theme!"
date:   2017-10-31
excerpt: "Huge thanks to HTML5 UP for making this awesome template! Let's see what it can do"
image: "/images/pic02.jpg"
---
  <title> 飛天網事--純CSS程式碼實現圖片輪播 </title>
  <meta charset="utf-8" />
  <meta name="description" content="飛天網事，WEB前端開發，純css3程式碼圖片輪播，HTML5+CSS3精彩案例" />
  <meta name="keywords" content="飛天網事，WEB前端開發，HTML5，CSS3，jQuery，" />
	<meta name="author" content="R.tian @eduppp.cn 2015">
	<link rel="shortcut icon"  href="http://eduppp.cn/images/logo4.gif" />
	<link rel="apple-touch-icon" href="http://eduppp.cn/images/logo.gif" />
  <style type="text/css">
		#frame {/*----------圖片輪播相框容器----------*/
			position: absolute; /*--絕對定位，方便子元素的定位*/
			width: 300px;
			height: 200px;
			overflow: hidden;/*--相框作用，只顯示一個圖片---*/
			border-radius:5px;
		}
		#dis {/*--絕對定位方便li圖片簡介的自動分佈定位---*/
			position: absolute;
			left: -50px;
			top: -10px;
			opacity: 0.5;
		}
		#dis li {
			display: inline-block;
			width: 200px;
			height: 20px;
			margin: 0 50px;
			float: left;
			text-align: center;
			color: #fff;
			border-radius: 10px;
			background: #000;
		}
		#photos img {
			float: left;
			width:300px;
			height:200px;
		}
		#photos {/*---設定總的圖片寬度--通過位移來達到輪播效果----*/
			position: absolute;z-index:9px;
			width: calc(300px * 5);/*---修改圖片數量的話需要修改下面的動畫引數*/
		}
		.play{
			animation: ma 20s ease-out infinite alternate;/**/
		}
		@keyframes ma {/*---每圖片切換有兩個階段：位移切換和靜置。中間的效果可以任意定製----*/
			0%,20% {		margin-left: 0px;		}
			25%,40% {		margin-left: -300px;	}
			45%,60% {		margin-left: -600px;	}
			65%,80% {		margin-left: -900px;	}
			85%,100% {		margin-left: -1200px;	}
		}
		.num{
			position:absolute;z-index:10;
			display:inline-block;
			right:10px;top:165px;
			border-radius:100%;
			background:#f00;
			width:25px;height:25px;
			line-height:25px;
			cursor:pointer;
			color:#fff;
			text-align:center;
			opacity:0.8;
		}
		.num:hover{background:#00f;}
		.num:hover,#photos:hover{animation-play-state:paused;}
		.num:nth-child(2){margin-right:30px}
		.num:nth-child(3){margin-right:60px}
		.num:nth-child(4){margin-right:90px}
		.num:nth-child(5){margin-right:120px}
		#a1:hover ~ #photos{animation: ma1 .5s ease-out forwards;}
		#a2:hover ~ #photos{animation: ma2 .5s ease-out forwards;}
		#a3:hover ~ #photos{animation: ma3 .5s ease-out forwards;}
		#a4:hover ~ #photos{animation: ma4 .5s ease-out forwards;}
		#a5:hover ~ #photos {animation: ma5 .5s ease-out forwards;}
		@keyframes ma1 {0%{margin-left:-1200px;}100%{margin-left:-0px;}	}
		@keyframes ma2 {0%{margin-left:-1200px;}100%{margin-left:-300px;}	}
		@keyframes ma3 {100%{margin-left:-600px;}	}
		@keyframes ma4 {100%{margin-left:-900px;}	}
		@keyframes ma5 {100%{margin-left:-1200px;}	}
  </style>

 <div id="frame" >
	<a id="a1" class="num">1</a>
	<a id="a2" class="num">2</a>
	<a id="a3" class="num">3</a>
	<a id="a4" class="num">4</a>
	<a id="a5" class="num">5</a>
	<div id="photos" class="play">
		<img src="http://eduppp.cn/images/0/1.jpg" >
		  <img src="http://eduppp.cn/images/0/3.jpg" >
		<img src="http://eduppp.cn/images/0/4.jpg" >
		<img src="http://eduppp.cn/images/0/5.jpg" >
		<img src="http://eduppp.cn/images/0/2.jpg" >
		<ul id="dis">
			<li>中國標誌性建築：天安門</li>
			<li>中國標誌性建築：東方明珠</li>
			<li>中國標誌性建築：布達拉宮</li>
			<li>中國標誌性建築：長城</li>
			<li>中國標誌性建築：天壇</li>
			</ul>
	</div>
</div>
