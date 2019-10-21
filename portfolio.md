---
layout: default
title: Portfolio
---
<a href="/" style="float:right;"><img src="/assets/images/logo-only.png" height="80" /></a>

<style>
/* Portfolio */

.portfolio-set {

}

.website .client-title {
	display: block;
	margin-bottom: 4px;
}

.website {
	margin-right: 10px;
	max-width: 175px;
	display: inline-block;
	vertical-align: top;
}

.website:last-child {
	margin-right: 0;
}

.website img {
	height: 120px;
	width: 175px;
	margin-bottom: 10px;
}

/** LIGHTBOX MARKUP **/

.s-lightbox {
	/** Default lightbox to hidden */
	display: none;
	/** Position and style */
	position: fixed !important;
	z-index: 999;
	width: 100%;
	height: 100%;
	text-align: center;
	top: 0;
	left: 0;
	background: rgba(0, 0, 0, 0.8) !important;
}

.s-lightbox img {
	/** Pad the lightbox image */
	max-width: 90%;
	max-height: 80%;
	margin-top: 2%;
}

.s-lightbox strong, .s-lightbox p, .s-lightbox small {
	color: #ffffff;
}

.s-lightbox:target {
	/** Remove default browser outline */
	outline: none;
	/** Unhide lightbox **/
	display: block;
}

a.s-lightbox {
	text-decoration: none !important;
}

.s-lightbox span {
	display: block;
	color: #FFFFFF !important;
}
</style>

# Portfolio

## Projects

[**Bulk User Management**](https://github.com/colettesnowmedia/bulk-user-management)

WordPress plugin to allow bulk importing, editing, and deleting of users via the use of CSV files.

[**Simple Cache for CodeIgniter**](https://github.com/colettesnow/Simple-Cache-for-CodeIgniter)

Simple Cache for CodeIgniter is an open source file based fragment caching library released under the GNU General Public License. It was designed to be simple to use and easily adaptable to use alternate backends if this was needed in the future. Also compatible with non-CodeIgniter applications.

**Muse’s Success** \([website](https://muses-success.info) \| [source](https://github.com/colettesnow/muses-success)\)

Muse’s Success is a structured wiki and community that is similar to Goodreads but exclusively for web fiction.

## WordPress
{% assign wordpress = site.portfolio | where: "type","wordpress" %}
<div class="portfolio-set">
{% for website in wordpress limit: 4 %}<span class="website"><a href="#{{ website.slug }}"><img src="{{ website.thumbnail }}" title="{{ website.title }}" /></a><strong class="client-title">{{ website.title }}</strong><small>{{ website.caption }}</small></span>{% endfor %}
</div>

## Websites (non-WordPress)
{% assign websites = site.portfolio | where: "type","websites" %}
<div class="portfolio-set">
{% for website2 in websites limit: 4 %}<span class="website"><a href="#{{ website2.slug }}"><img src="{{ website2.thumbnail }}" title="{{ website2.title }}" /></a><strong class="client-title">{{ website2.title }}</strong><small>{{ website2.caption }}</small></span>{% endfor %}
</div>

<br /><br />

{% for sites in site.portfolio %}<p><a class="s-lightbox" href="#_" id="{{ sites.slug }}"><img src="{{ sites.screenshot }}" /><br /><strong>{{ sites.title }}</strong><br /><small>{{ sites.caption }}</small></a></p>{% endfor %}
