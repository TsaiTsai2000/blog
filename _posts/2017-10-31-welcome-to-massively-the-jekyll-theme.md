---
layout: post
title:  "Welcome to Massively: The Jekyll Theme!"
date:   2017-10-31
excerpt: "Huge thanks to HTML5 UP for making this awesome template! Let's see what it can do"
image: "/images/pic02.jpg"
---
/*

All grid code is placed in a 'supports' rule (feature query) at the bottom of the CSS (Line 77). 
        
The 'supports' rule will only run if your browser supports CSS grid.

Flexbox is used as a fallback so that browsers which don't support grid will still recieve an identical layout.

*/

@import url(https://fonts.googleapis.com/css?family=Montserrat:500);

:root {
	/* Base font size */
	font-size: 10px;
}

*,
*::before,
*::after {
	box-sizing: border-box;
}

body {
	min-height: 100vh;
	background-color: #fafafa;
}

.container {
	max-width: 100rem;
	margin: 0 auto;
	padding: 0 2rem 2rem;
}

.heading {
	font-family: "Montserrat", Arial, sans-serif;
	font-size: 4rem;
	font-weight: 500;
	line-height: 1.5;
	text-align: center;
	padding: 3.5rem 0;
	color: #1a1a1a;
}

.heading span {
	display: block;
}

.gallery {
	display: flex;
	flex-wrap: wrap;
	/* Compensate for excess margin on outer gallery flex items */
	margin: -1rem -1rem;
}

.gallery-item {
	/* Minimum width of 24rem and grow to fit available space */
	flex: 1 0 24rem;
	/* Margin value should be half of grid-gap value as margins on flex items don't collapse */
	margin: 1rem;
	box-shadow: 0.3rem 0.4rem 0.4rem rgba(0, 0, 0, 0.4);
	overflow: hidden;
}

.gallery-image {
	display: block;
	width: 100%;
	height: 100%;
	object-fit: cover;
	transition: transform 400ms ease-out;
}

.gallery-image:hover {
	transform: scale(1.15);
}

/*

The following rule will only run if your browser supports CSS grid.

Remove or comment-out the code block below to see how the browser will fall-back to flexbox styling. 

*/

@supports (display: grid) {
	.gallery {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(24rem, 1fr));
		grid-gap: 2rem;
	}

	.gallery,
	.gallery-item {
		margin: 0;
	}
}

<div class="container">

<h1 class="heading">Image Gallery with CSS Grid <span>& Flexbox Fallback</span></h1>

<div class="gallery">

<div class="gallery-item">
		<img class="gallery-image" src="https://tsaitsai2000.github.io/blog/images/Cebu/cover.jpg" alt="person writing in a notebook beside by an iPad, laptop, printed photos, spectacles, and a cup of coffee on a saucer">
		</div>

<div class="gallery-item">
		<img class="gallery-image" src="https://images.u
		nsplash.com/photo-1515260268569-9271009adfdb?w=500&h=500&fit=crop" alt="sunset behind San Francisco city skyline">
		</div>

<div class="gallery-item">
		<img class="gallery-image" src="https://images.unsplash.com/photo-1506045412240-22980140a405?w=500&h=500&fit=crop" alt="people holding umbrellas on a busy street at night lit by street lights and illuminated signs in Tokyo, Japan">
		</div>

<div class="gallery-item">
		<img class="gallery-image" src="https://images.unsplash.com/photo-1514041181368-bca62cceffcd?w=500&h=500&fit=crop" alt="car interior from central back seat position showing driver and blurred view through windscreen of a busy road at night">
		</div>

<div class="gallery-item">
			<img class="gallery-image" src="https://images.unsplash.com/photo-1445810694374-0a94739e4a03?w=500&h=500&fit=crop" alt="back view of woman wearing a backpack and beanie waiting to cross the road on a busy street at night in New York City, USA">
	</div>

<div class="gallery-item">
		<img class="gallery-image" src="https://images.unsplash.com/photo-1486334803289-1623f249dd1e?w=500&h=500&fit=crop" alt="man wearing a black jacket, white shirt, blue jeans, and brown boots, playing a white electric guitar while sitting on an amp">
		</div>

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
