---
layout: Home
title: Home｜TSAI's Blog
description: my blog
sitemap:
    priority: 1.0
    lastmod: 2020-02-18
    changefreq: weekly
---
<html>
	<head>
    {% include head.html %}


	</head>
	<body class="is-loading">

		<!-- Wrapper -->
			<div id="wrapper" class="fade-in">

				<!-- Intro -->
					<div id="intro">
            <h1>{{site.title}}</h1>
						<h2>{{site.bio}}</h2>
						<p>分享生活、旅遊記事，把握現在的日子留做以後懷念。</p>
						<ul class="actions">
							<li><a href="#header" class="button icon solo fa-arrow-down scrolly">Continue</a></li>
						</ul>
					</div>

				<!-- Header -->
					<header id="header">
						<a href="{{ "/" | absolute_url }}" class="logo">{{site.title}}</a>
					</header>

				<!-- Nav -->
					<nav id="nav">

            {% include nav.html %}

					</nav>

				<!-- Main -->
					<div id="main">
						<!-- Featured Post -->
							<article class="post featured">
								<header class="major">
									<h2><a href="#">Travel</a></h2>
									<p></p>
								</header>
								<a href="#" class="image main"><img src="{{ "/images/travel.jpg" | absolute_url }}" alt="" /></a>
                <p><font face="微軟正黑體">我會在主頁這裡分享出去旅遊的心得，
					裡面包含一些去之前所預排的行程表、一趟旅途的花費，
					這些都是花了很多時間去安排的~ 想去的人如果可以參考一下我會很開心❤️
					不過大部分旅記內文就是給自己留作未來紀念，
					有點害羞、有點多廢話，希望各位不介意了!<br>而我也分享除了旅遊以外的生活大小事，有興趣可以點進blog裡面看全部~</font></p>
							</article>
						<!-- Posts -->
							<section class="posts">
                {% for post in site.posts limit:4 %}
                {% assign mod3 = forloop.index | modulo: 4 %}
  								<article>
  									<header>
  										<span class="date">{{ post.date | date_to_string }}</span>
  										<h2><a href="{{ post.url | absolute_url }}">{{ post.title }}</a></h2>
  									</header>
  									<a href="{{ post.url | absolute_url }}" class="image fit"><img src="{{ post.image | absolute_url }}" alt="" /></a>
  									<p>{{ post.excerpt }}</p>
  									<ul class="actions">
  										<li><a href="{{ post.url | absolute_url }}" class="button">Full Story</a></li>
  									</ul>
  								</article>
                  {% if mod3 == 0 %}
                  {% endif %}
                {% endfor %}

							</section>

						<!-- Footer -->
							<footer>
                <ul class="actions">
                  <li><a href="{{ "/blog/" | absolute_url }}" class="button">My Blog</a></li>
                </ul>
							</footer>

					</div>

				<!-- Footer -->
        {% include foot.html %}

			</div>

		<!-- Scripts -->
		{% include scripts-main.html %}
    {% include tracking.html %}

	</body>
</html>
