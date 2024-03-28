# Project 4


- [1 - Introduction](#1---introduction)
- [2 - Matomo implementation](#2---matomo-implementation)
- [3 - How to add widgets to the dashboard?](#3---how-to-add-widgets-to-the-dashboard)
- [4 - How to create a dashboard for each tracked page?](#4---how-to-create-a-dashboard-for-each-tracked-page)
- [5 - Free tools descriptions](#5---free-tools-descriptions)
- [6 - Home-made process and Hotjar alternatives](#6---Home-made-process-and-Hotjar-alternatives)
- [7 - Reference](#7---reference)

## 1 - Introduction 

This document takes place in the context of matomo implementation to track the mosaic web pages and replace the home-made process and Hotjar. It summarizes how to use the Matomo analytics platform and proposes alternative indicators that are similar to those used both in the home-made tool and with Hotjar.

The database used to store visitor’s data was created with the DataBase Management System MariaDB. The tracked mosaic pages are the following: bioacc, growth, ssd-faq, guts-predict, tkdb. 

For reasons of confidentiality, identifiers and passwords to access the matomo page with the data on the visits of mosaic pages are not provided in this document. Nevertheless, they can be requested by sending a mail to mosaic@univ-lyon1.fr.

## 2 - Matomo implementation

 

To implement matomo, insert the following JavaScript code (tracking code) in the <head> tags of the html code corresponding to pages that you want to track:

~~~~javascript
<!-- Matomo -->

<script>
 var _paq = window._paq = window._paq || [];
 /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
 _paq.push(['trackPageView']);
 _paq.push(['enableLinkTracking']);
 (function() {
  var u="//lbbe-analytics.univ-lyon1.fr/";
  _paq.push(['setTrackerUrl', u+'matomo.php']);
  _paq.push(['setSiteId', '4']);
  var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
  g.async=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
 })();
</script>
<!-- End Matomo Code -->
~~~~

## 3 - How to add widgets to the dashboard?

*Dashboard* → *Dashboard* (down arrow) → *Select the widget of interest*

## 4 - How to create a dashboard for each tracked page? 

*All visits* (top tab) → *add new segment → Actions In Visit → Behaviour → Page URL → Is → Value* : select the url corresponding to the page of interest → *Save & Apply* (after giving a name for the new dashboard)

## 5 - Free tools descriptions

### 5.1 Visitors

It presents insights through graphs, a map and tables about the **number of visits** in addition to insights about **visitors** such as their IP, their locations, the operating system used, the average duration of their visits, etc. The period can be modified and the visitors can be tracked in real time. 

### 5.2 Behaviour

It presents tables containing **statistics about tracked pages** (views, first or last seen by the visitors) and visitor actions (search keywords used, the downloaded contents …). Furthermore, it is possible to **define events to measure specific user interactions** **with the pages** and know whether visits correspond to **new ones or returning visits** through the *Events* and *Engagement* tabs. 

### 5.3 Acquisition

It presents **channels that lead visitors to the websites**. The different channel types are the following:

- Direct Entry: visitors have directly entered the web page URL in web browsers. 

- Search Engines: visitors were referred to the web page through searching in the web browser (insights about the web browsers and the key words used).
- Websites: visitors were redirected by a link leading to the web page of interest (insights about the sites / social media that refer to the tracked page).
- Marketing campaign: visitors were redirected to the web page through e-mails or advertisements…

Moreover, a graph to visualize the different channel types used over time is provided. 

### 5.4 Goals

It allows the user to **define objectives** based on:

- visits (the page can be specified with an url or the page title)
- downloads 
- links redirecting to another web site
- time spent on a page

It provides a graph to visualize the objective fulfilled over time. 

## 6 - Home-made process and Hotjar alternatives

### 6.1 Home-made process alternatives

- ![#ea9898](https://placehold.co/15x15/ea9898/ea9898.png) `Home-made tools`
____________________



<img src="./Project 4.assets/image-20240327170940686.png" alt="image-20240327170940686" style="zoom: 80%;" />

→ Behaviour → Pages : the table can be exported in different formats such as tsv. 

<img src="./Project 4.assets/z6-C3KWujpUvBdjHwQreJF97XuflR2WiI28VN3gk0mNZcG5iq2nCPkosp1imfo628qjEJgMWWkUMGsRzxWVVmFIWp2YTVuqr2KSiIm72Pgbk7j5rjPbZ6Wmdv3yzodRFH6u3_AeUGXAPZPGyKB47KH8.png" alt="img" style="zoom: 67%;" />

_________________________



<img src="./Project 4.assets/image-20240327171013863.png" alt="image-20240327171013863" style="zoom:80%;" />

Visitors → Location 

<img src="./Project 4.assets/bXxHoTXSfdDgDO4-pq1zthk91DBccpSxuoiKlbMd2H-WEjTo9ZcjX_Nd0XKXQdH78L5GI6U2sJtoQ1J4obq5__YufgYonPqO2LuXOICcqRrbF2JBbd5xtfrwvtJCqnwcL_xeV_c4Oal7XW3YEE6_UC8.png" alt="img" style="zoom: 50%;" />

________________________



<img src="./Project 4.assets/image-20240327171030343.png" alt="image-20240327171030343">

Visitors → Visits Log

​				<img src="./Project 4.assets/Y_DqKGxsX3xl4pW3H00irTzobIxfa6CMrDtPHwyX-x5D6dk0v3OVriApEpwFsebhaD2OR_MLGhRWjHMCwAarfETb8zqMLcAqYXwUjGLdpofMdj7vsdZeF3rwvhhDcsbCPkHhmXt9HGKGJHrvIzDw-cE.png" alt="img" style="zoom: 67%;" />

__________________________________



### 6.2 <span style="color:green">Hotjar</span>  alternatives

- ![#93c47d](https://placehold.co/15x15/93c47d/93c47d.png) `Hotjar tools`
_________________________



<img src="./Project 4.assets/image-20240327171058771.png" alt="image-20240327171058771" style="zoom: 80%;" />

<img src="./Project 4.assets/image-20240327171119378.png" alt="image-20240327171119378" style="zoom:80%;" />

→ Behaviour → Pages: the table can be exported in different formats such as tsv. 



<img src="./Project 4.assets/9n3WHEqWbjcJPH-yX6X1OSL0Rtp55rz-Z_3z2nSrnKkW3y7Po8MkAB2WR4uBvGHKfZ9KPH8pK9J0wd3f8H0V6TeQZPTacbDGBzJwc3iNmsb2o90N0ZZSfgdeeIhiR-Aeh18lJNRkedy8oGQS1Q59dZI.png" alt="img" style="zoom:80%;" />



_________________



<img src="./Project 4.assets/image-20240327171134992.png" alt="image-20240327171134992" style="zoom: 80%;" />

 → Behaviour → Downloads (top clicked button can be defined in Goal) 

<img src="./Project 4.assets/ygtZjn11j6I6kv1baDApU3WL0pb8aYMXYNUv33x1q8hxoH7dzmbW3WnCDjVU1IGeUJ1H-nxa0AuRAfjiCYGf_aMNDtUticjp-wrLvFXvNmqfQESpaplXf7bmP9ewLl-YNF8WjOjSROhxvowOYopxK3Y.png" alt="img" style="zoom: 80%;" />

_____________________



<img src="./Project 4.assets/image-20240327171153486.png" alt="image-20240327171153486" style="zoom:67%;" />

Behaviour → Engagement 

​					**<img src="./Project 4.assets/oZNL55kn5-VUA7oNNWfB_7eejNjDAe08z6JbrpgQMbI7ChiAtx4G0-MtUhTPRDMQw4IINissg0uYoMx1lAyW9FK7j4d_yfub57d9G3WKj2sEzqDntpheL1L9vQLjusj03lZyiWVOoqdFOV-X1V1WU9k.png" alt="img" style="zoom: 80%;" />**

____



<img src="./Project 4.assets/image-20240327171209591.png" alt="image-20240327171209591" style="zoom:80%;" />

Visitors → Devices → Device type → change visualization → vertical bar graph

​								**<img src="./Project 4.assets/QKPXDKjFFGYlo-G4gsBC0gSKCyrHYxOpBC6VjiuZablcVe4GQ3sOUV-0W7DVxOHyrq4zcgkDaaHv0uastbqvRUz0FethRaf0Om4Av5GdbC4LFu8gvMKPBj_CltES7BN86VA7x1eOt4RTdi_2MoqcKN0.png" alt="img"  />**

_____________



<img src="./Project 4.assets/image-20240327171225565.png" alt="image-20240327171225565" style="zoom:50%;" />

Visitors→ Location → Country → Change visualization → Pie chart 

​							<img src="./Project 4.assets/_s-ZcZczkzAlzi5IgMm7wHEQUl5Q4xsv91oFntzjWPPlH29yMxrjOK3-gWCx95xv69g4EgQYvoyawpWmDc0Mze4Hjp4a_RDyfCyD821zBnqw1P5ePuLQFYTVxzK6vW_-vmBNOmMFFFHgVgrF_lo7TiU.png" alt="img" style="zoom:67%;" />

 

**Recordings**

_____________



<img src="./Project 4.assets/PixPin_2024-03-28_13-58-16.png" alt="image-20240327171304121" style="zoom:67%;" />

→ Session Recordings (paying service)

__________________



**Heatmaps**

____________________



<img src="./Project 4.assets/image-20240327171324117.png" alt="image-20240327171324117" style="zoom:67%;" />

**→** Heatmaps (paying service)

___________________



## 7 - Reference

[1]- Matomo: a powerful web analysis platform that gives you ownership of 100% of the data. https://fr.matomo.org/, 2018 (accessed June 13, 2023).
