---
layout: default
title: Portfolio
permalink: /portfolio
---
<a href="/" class="logo"><img src="/assets/images/logo-only.png" height="80" /></a>

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
{% for website in wordpress limit: 4 %}<span class="website"><a href="#{{ website.slug }}"><img src="{{ website.thumbnail }}" title="{{ website.title }}" alt="Thumbnail of {{ website.title }}" /></a><strong class="client-title">{{ website.title }}</strong><small>{{ website.caption }}</small></span>{% endfor %}
</div>

## Websites (non-WordPress)
{% assign websites = site.portfolio | where: "type","websites" %}
<div class="portfolio-set">
{% for website2 in websites limit: 4 %}<span class="website"><a href="#{{ website2.slug }}"><img src="{{ website2.thumbnail }}" title="{{ website2.title }}" alt="Thumbnail of {{ website2.title }}" /></a><strong class="client-title">{{ website2.title }}</strong><small>{{ website2.caption }}</small></span>{% endfor %}
</div>

<br /><br />

{% for sites in site.portfolio %}<p><a class="s-lightbox" href="#_" id="{{ sites.slug }}"><img src="{{ sites.screenshot }}" alt="Screenshot of {{ sites.title }}" /><br /><strong>{{ sites.title }}</strong><br /><small>{{ sites.caption }}</small></a></p>{% endfor %}
