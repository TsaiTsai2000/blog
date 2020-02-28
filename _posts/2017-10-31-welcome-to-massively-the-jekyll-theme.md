---
layout: post
title:  "Welcome to Massively: The Jekyll Theme!"
date:   2017-10-31
excerpt: "Huge thanks to HTML5 UP for making this awesome template! Let's see what it can do"
image: "/images/pic02.jpg"
---
<style type='text/css'>

.slider_container {
    margin: 30px auto;
    width: 400px;
    height: 280px;
    position: relative;
    border: 20px solid;    
    border-color: #fff;
    border-bottom-width: 100px;
    background-color: #f5f5f5;
    box-shadow: #666 0 0 5px;
}

.slider_container div {
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    filter: alpha(opacity=0);
}
.slider_container div {
    -webkit-animation: round 25s linear infinite;
            animation: round 25s linear infinite;
}

@-webkit-keyframes round {
    4% {
        opacity: 1;
        filter: alpha(opacity=100);
        /* 0 - 1秒 淡入*/
    }
    20% {
        opacity: 1;
        filter: alpha(opacity=100);
        /* 1- 5秒靜止*/
    }
    24% {
        opacity: 0;
        filter: alpha(opacity=0);
        /* 5-6秒淡出*/
    }
}
@keyframes round {
    4% {
        opacity: 1;
        filter: alpha(opacity=100);
        /* 0 - 1秒 淡入*/
    }
    20% {
        opacity: 1;
        filter: alpha(opacity=100);
        /* 1- 5秒靜止*/
    }
    24% {
        opacity: 0;
        filter: alpha(opacity=0);
        /* 5-6秒淡出*/
    }
}
.slider_container div:nth-child(5) {
    -webkit-animation-delay: 0s;
            animation-delay: 0s;
}

.slider_container div:nth-child(4) {
    -webkit-animation-delay: 5s;
            animation-delay: 5s;
}

.slider_container div:nth-child(3) {
    -webkit-animation-delay: 10s;
            animation-delay: 10s;
}

.slider_container div:nth-child(2) {
    -webkit-animation-delay: 15s;
            animation-delay: 15s;
}

.slider_container div:nth-child(1) {
    -webkit-animation-delay: 20s;
            animation-delay: 20s;
}
.slider_container span {    
    color: #000;
    background: #fff;
    position: absolute;
    left: 0%;
    top: 280px;
    width: 400px;
    height: 100px;
    font-size: 30px;
    text-align: center;
    line-height: 100px;
    -webkit-transform:scaleY(0);
        -ms-transform:scaleY(0);
            transform:scaleY(0);
    -webkit-transition: all 0.5s ease-in-out;
            transition: all 0.5s ease-in-out;
}

.slider_container:hover span {
    width: 100%;
    -webkit-transform:scaleY(1);
        -ms-transform:scaleY(1);
            transform:scaleY(1);
}
.slider_container:hover div {
    -webkit-animation-play-state: paused;
            animation-play-state: paused;
}
</style>

<div class="slider_container">
	<div>
		<img src="https://tsaitsai2000.github.io/blog/images/Cebu/1-2.JPG" alt="pure css3 slider" />
		
<span class="info">Image Description 1</span>
</div>
	<div>
	<img src="https://tsaitsai2000.github.io/blog/images/Cebu/6.JPG" alt="pure css3 slider" / position: fixed; z-index: -1>
	<span class="info">Image Description 2</span>
	</div>
	<div>
		<img src="https://tsaitsai2000.github.io/blog/images/Cebu/3.JPG" alt="pure css3 slider" / position: fixed; z-index: -1>
	<span class="info">Image Description 3</span>
	</div>
	<div>
	<img src="https://tsaitsai2000.github.io/blog/images/Cebu/1.JPG" alt="pure css3 slider" / position: fixed; z-index: -1>
	<span class="info">Image Description 4</span>
	</div>
	<div>
		<img src="https://tsaitsai2000.github.io/blog/images/Cebu/2.JPG" alt="pure css3 slider" / position: fixed; z-index: -1>
	<span class="info">Image Description 5</span>
	</div>
</div>
## How to Use This Theme
Just go ahead and read up on [how to install Jekyll](https://jekyllrb.com/). It's not too hard I promise!

Download this repository [here](https://github.com/iwiedenm/jekyll-theme-massively) and save it to any folder you want.

Open a terminal window or a command line and ```cd``` to that location.

Then enter: ```bundle exec jekyll serve```. You can now access your new Jekyll site from [http://127.0.0.1:4000/](http://127.0.0.1:4000/). Have fun exploring your new site!

## Features
### Auto-Generating Sitemap
The sitemap is auto generated! Just simply change the front matter of each site. It looks like so...
```
sitemap:
    priority: 0.7
    lastmod: 2017-11-02
    changefreq: weekly
```
### Formspring integration
The contact form below each page on the footer actually collects information! Just change your email address in the ```_config.yml``` file!
