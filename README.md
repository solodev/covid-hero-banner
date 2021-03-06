# covid-hero-banner
Add custom messages, links, and images to your website

## Tutorial

For detailed instructions, view the [COVID Hero Banner](http://www.covidresponse19.com/free-website-tools/covid-hero-banner.stml) article.

## Demo

Check out a working example on [JSFiddle](https://jsfiddle.net/solodev/mxvy9p60/).

## HTML

The HTML is wrapped with a unique "covid-hero" class so that the CSS styles can target this element specifically without interferring with other elements. Swap the image for one specific to your business or industry with recommended dimensions of 1920px by 600px. Customize the content inside the "header-content" element to meet your needs.

```
<header class="covid-hero">
	<div class="hero">
	  <div class="hero-item">
			<img alt="Covid-19 Image" class="img-responsive cover" src="https://raw.githubusercontent.com/solodev/covid-hero-banner/master/covid_banners_1.jpg">
			<div class="header-container">
				<div class="header-content">
					<h1>COVID-19 Updates</h1> 
					<p>Get the latest news on the Coronavirus efforts from the city and county.</p>
					<a class="btn btn-primary" href="#">Learn More</a>
				</div>
			</div>
	  </div>
	</div>
</header>
```


## CSS

The CSS utilizes the object-fit property to make sure the image scales properly to the container and on mobile devices. Additionally, the "header-content" class has a background-color with a transparent opacity to ensure readibility but allow the image behind it to be visible.

```
.covid-hero {
	overflow: hidden;
	font-family: Inter, sans-serif;
}
.covid-hero .hero .hero-item img {
	width: 100%;
	height: 600px;
	object-fit: cover;
	object-position: top center;
}
.covid-hero .hero .hero-item .header-container {
    max-width: 1200px;
    margin: 0 auto;
}
.covid-hero .hero .hero-item .header-content {
	top: 20%;
	margin-left: 8rem;
	background-color: rgba(0, 0, 0, 0.7);
	max-width: 473px;
	width: 100%;
	padding: 2rem;
	position: absolute;
	color: #fff;
}
.covid-hero .hero .hero-item .header-content p {
	font-size: 18px;
}
.covid-hero .hero .hero-item .header-content .btn-primary {
  background-color: #579829;
	color: #fff;
	font-size: 18px;
	text-decoration: none;
	margin-top: 15px;
  padding: 15px;
	display: inline-block;
}
.covid-hero .hero .hero-item .header-content .btn-primary:hover {
    background-color: #366b11;
}

/* Media Queries */
@media (max-width: 768px) {
	.covid-hero .hero .hero-item .header-content {
		left: 50%;
		-webkit-transform: translateX(-50%);
		transform: translateX(-50%);
		margin: 0 auto;
	}
}
```

