# Kievit3

<html class="no-js" lang="en-US">
<head>
  <meta name="viewport" content="width=device-width, height=device-height, initial-scale=1.0">
  <meta charset="UTF-8" /><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={licenseKey:"NRJS-7a0deee73b6de246708",applicationID:"41455697"};window.NREUM||(NREUM={}),__nr_require=function(e,t,n){function r(n){if(!t[n]){var i=t[n]={exports:{}};e[n][0].call(i.exports,function(t){var i=e[n][1][t];return r(i||t)},i,i.exports)}return t[n].exports}if("function"==typeof __nr_require)return __nr_require;for(var i=0;i<n.length;i++)r(n[i]);return r}({1:[function(e,t,n){function r(){}function i(e,t,n){return function(){return o(e,[u.now()].concat(c(arguments)),t?null:this,n),t?void 0:this}}var o=e("handle"),a=e(7),c=e(8),f=e("ee").get("tracer"),u=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var d=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],p="api-",l=p+"ixn-";a(d,function(e,t){s[t]=i(p+t,!0,"api")}),s.addPageAction=i(p+"addPageAction",!0),s.setCurrentRouteName=i(p+"routeName",!0),t.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,t){var n={},r=this,i="function"==typeof t;return o(l+"tracer",[u.now(),e,n],r),function(){if(f.emit((i?"":"no-")+"fn-start",[u.now(),r,i],n),i)try{return t.apply(this,arguments)}catch(e){throw f.emit("fn-err",[arguments,this,e],n),e}finally{f.emit("fn-end",[u.now()],n)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,t){m[t]=i(l+t)}),newrelic.noticeError=function(e,t){"string"==typeof e&&(e=new Error(e)),o("err",[e,u.now(),!1,t])}},{}],2:[function(e,t,n){function r(){return c.exists&&performance.now?Math.round(performance.now()):(o=Math.max((new Date).getTime(),o))-a}function i(){return o}var o=(new Date).getTime(),a=o,c=e(9);t.exports=r,t.exports.offset=a,t.exports.getLastTimestamp=i},{}],3:[function(e,t,n){function r(e){return!(!e||!e.protocol||"file:"===e.protocol)}t.exports=r},{}],4:[function(e,t,n){function r(e,t){var n=e.getEntries();n.forEach(function(e){"first-paint"===e.name?d("timing",["fp",Math.floor(e.startTime)]):"first-contentful-paint"===e.name&&d("timing",["fcp",Math.floor(e.startTime)])})}function i(e,t){var n=e.getEntries();n.length>0&&d("lcp",[n[n.length-1]])}function o(e){e.getEntries().forEach(function(e){e.hadRecentInput||d("cls",[e])})}function a(e){if(e instanceof m&&!g){var t=Math.round(e.timeStamp),n={type:e.type};t<=p.now()?n.fid=p.now()-t:t>p.offset&&t<=Date.now()?(t-=p.offset,n.fid=p.now()-t):t=p.now(),g=!0,d("timing",["fi",t,n])}}function c(e){d("pageHide",[p.now(),e])}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var f,u,s,d=e("handle"),p=e("loader"),l=e(6),m=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){f=new PerformanceObserver(r);try{f.observe({entryTypes:["paint"]})}catch(v){}u=new PerformanceObserver(i);try{u.observe({entryTypes:["largest-contentful-paint"]})}catch(v){}s=new PerformanceObserver(o);try{s.observe({type:"layout-shift",buffered:!0})}catch(v){}}if("addEventListener"in document){var g=!1,w=["click","keydown","mousedown","pointerdown","touchstart"];w.forEach(function(e){document.addEventListener(e,a,!1)})}l(c)}},{}],5:[function(e,t,n){function r(e,t){if(!i)return!1;if(e!==i)return!1;if(!t)return!0;if(!o)return!1;for(var n=o.split("."),r=t.split("."),a=0;a<r.length;a++)if(r[a]!==n[a])return!1;return!0}var i=null,o=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var c=navigator.userAgent,f=c.match(a);f&&c.indexOf("Chrome")===-1&&c.indexOf("Chromium")===-1&&(i="Safari",o=f[1])}t.exports={agent:i,version:o,match:r}},{}],6:[function(e,t,n){function r(e){function t(){e(a&&document[a]?document[a]:document[i]?"hidden":"visible")}"addEventListener"in document&&o&&document.addEventListener(o,t,!1)}t.exports=r;var i,o,a;"undefined"!=typeof document.hidden?(i="hidden",o="visibilitychange",a="visibilityState"):"undefined"!=typeof document.msHidden?(i="msHidden",o="msvisibilitychange"):"undefined"!=typeof document.webkitHidden&&(i="webkitHidden",o="webkitvisibilitychange",a="webkitVisibilityState")},{}],7:[function(e,t,n){function r(e,t){var n=[],r="",o=0;for(r in e)i.call(e,r)&&(n[o]=t(r,e[r]),o+=1);return n}var i=Object.prototype.hasOwnProperty;t.exports=r},{}],8:[function(e,t,n){function r(e,t,n){t||(t=0),"undefined"==typeof n&&(n=e?e.length:0);for(var r=-1,i=n-t||0,o=Array(i<0?0:i);++r<i;)o[r]=e[t+r];return o}t.exports=r},{}],9:[function(e,t,n){t.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,t,n){function r(){}function i(e){function t(e){return e&&e instanceof r?e:e?u(e,f,a):a()}function n(n,r,i,o,a){if(a!==!1&&(a=!0),!l.aborted||o){e&&a&&e(n,r,i);for(var c=t(i),f=v(n),u=f.length,s=0;s<u;s++)f[s].apply(c,r);var p=d[h[n]];return p&&p.push([b,n,r,c]),c}}function o(e,t){y[e]=v(e).concat(t)}function m(e,t){var n=y[e];if(n)for(var r=0;r<n.length;r++)n[r]===t&&n.splice(r,1)}function v(e){return y[e]||[]}function g(e){return p[e]=p[e]||i(n)}function w(e,t){s(e,function(e,n){t=t||"feature",h[n]=t,t in d||(d[t]=[])})}var y={},h={},b={on:o,addEventListener:o,removeEventListener:m,emit:n,get:g,listeners:v,context:t,buffer:w,abort:c,aborted:!1};return b}function o(e){return u(e,f,a)}function a(){return new r}function c(){(d.api||d.feature)&&(l.aborted=!0,d=l.backlog={})}var f="nr@context",u=e("gos"),s=e(7),d={},p={},l=t.exports=i();t.exports.getOrSetContext=o,l.backlog=d},{}],gos:[function(e,t,n){function r(e,t,n){if(i.call(e,t))return e[t];var r=n();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,t,{value:r,writable:!0,enumerable:!1}),r}catch(o){}return e[t]=r,r}var i=Object.prototype.hasOwnProperty;t.exports=r},{}],handle:[function(e,t,n){function r(e,t,n,r){i.buffer([e],r),i.emit(e,t,n)}var i=e("ee").get("handle");t.exports=r,r.ee=i},{}],id:[function(e,t,n){function r(e){var t=typeof e;return!e||"object"!==t&&"function"!==t?-1:e===window?0:a(e,o,function(){return i++})}var i=1,o="nr@id",a=e("gos");t.exports=r},{}],loader:[function(e,t,n){function r(){if(!E++){var e=x.info=NREUM.info,t=l.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&t))return u.abort();f(h,function(t,n){e[t]||(e[t]=n)});var n=a();c("mark",["onload",n+x.offset],null,"api"),c("timing",["load",n]);var r=l.createElement("script");r.src="https://"+e.agent,t.parentNode.insertBefore(r,t)}}function i(){"complete"===l.readyState&&o()}function o(){c("mark",["domContent",a()+x.offset],null,"api")}var a=e(2),c=e("handle"),f=e(7),u=e("ee"),s=e(5),d=e(3),p=window,l=p.document,m="addEventListener",v="attachEvent",g=p.XMLHttpRequest,w=g&&g.prototype;if(d(p.location)){NREUM.o={ST:setTimeout,SI:p.setImmediate,CT:clearTimeout,XHR:g,REQ:p.Request,EV:p.Event,PR:p.Promise,MO:p.MutationObserver};var y=""+location,h={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1208.min.js"},b=g&&w&&w[m]&&!/CriOS/.test(navigator.userAgent),x=t.exports={offset:a.getLastTimestamp(),now:a,origin:y,features:{},xhrWrappable:b,userAgent:s};e(1),e(4),l[m]?(l[m]("DOMContentLoaded",o,!1),p[m]("load",r,!1)):(l[v]("onreadystatechange",i),p[v]("onload",r)),c("mark",["firstbyte",a.getLastTimestamp()],null,"api");var E=0}},{}],"wrap-function":[function(e,t,n){function r(e,t){function n(t,n,r,f,u){function nrWrapper(){var o,a,s,p;try{a=this,o=d(arguments),s="function"==typeof r?r(o,a):r||{}}catch(l){i([l,"",[o,a,f],s],e)}c(n+"start",[o,a,f],s,u);try{return p=t.apply(a,o)}catch(m){throw c(n+"err",[o,a,m],s,u),m}finally{c(n+"end",[o,a,p],s,u)}}return a(t)?t:(n||(n=""),nrWrapper[p]=t,o(t,nrWrapper,e),nrWrapper)}function r(e,t,r,i,o){r||(r="");var c,f,u,s="-"===r.charAt(0);for(u=0;u<t.length;u++)f=t[u],c=e[f],a(c)||(e[f]=n(c,s?f+r:r,i,f,o))}function c(n,r,o,a){if(!m||t){var c=m;m=!0;try{e.emit(n,r,o,t,a)}catch(f){i([f,n,r,o],e)}m=c}}return e||(e=s),n.inPlace=r,n.flag=p,n}function i(e,t){t||(t=s);try{t.emit("internal-error",e)}catch(n){}}function o(e,t,n){if(Object.defineProperty&&Object.keys)try{var r=Object.keys(e);return r.forEach(function(n){Object.defineProperty(t,n,{get:function(){return e[n]},set:function(t){return e[n]=t,t}})}),t}catch(o){i([o],n)}for(var a in e)l.call(e,a)&&(t[a]=e[a]);return t}function a(e){return!(e&&e instanceof Function&&e.apply&&!e[p])}function c(e,t){var n=t(e);return n[p]=e,o(e,n,s),n}function f(e,t,n){var r=e[t];e[t]=c(r,n)}function u(){for(var e=arguments.length,t=new Array(e),n=0;n<e;++n)t[n]=arguments[n];return t}var s=e("ee"),d=e(8),p="nr@original",l=Object.prototype.hasOwnProperty,m=!1;t.exports=r,t.exports.wrapFunction=c,t.exports.wrapInPlace=f,t.exports.argsToArray=u},{}]},{},["loader"]);</script>

  <title>FrieslandCampina Ingredients</title>

  <link rel="apple-touch-icon" sizes="180x180" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/apple-touch-icon.png">
  <link rel="icon" type="image/png" sizes="32x32" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/favicon-32x32.png">
  <link rel="icon" type="image/png" sizes="16x16" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/favicon-16x16.png">
  <link rel="manifest" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/site.webmanifest">
  <link rel="mask-icon" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/safari-pinned-tab.svg" color="#5bbad5">
  <link rel="shortcut icon" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/favicon.ico">
  <meta name="msapplication-TileColor" content="#ffffff">
  <meta name="msapplication-config" content="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/favicons/browserconfig.xml">
  <meta name="theme-color" content="#ffffff">
  <meta name="apple-mobile-web-app-title" content="FrieslandCampina Ingredients" />

  <link rel="stylesheet" href="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/css/main.css?ver=1619431103" />

  
	<!-- This site is optimized with the Yoast SEO plugin v15.9.1 - https://yoast.com/wordpress/plugins/seo/ -->
	<meta name="robots" content="index, follow, max-snippet:-1, max-image-preview:large, max-video-preview:-1" />
	<meta property="og:locale" content="en_US" />
	<meta property="og:type" content="website" />
	<meta property="og:site_name" content="FrieslandCampina Ingredients" />
	<meta name="twitter:card" content="summary_large_image" />
	<script type="application/ld+json" class="yoast-schema-graph">{"@context":"https://schema.org","@graph":[{"@type":"WebSite","@id":"https://www.frieslandcampinaingredients.com/#website","url":"https://www.frieslandcampinaingredients.com/","name":"FrieslandCampina Ingredients","description":"Every day Royal FrieslandCampina provides millions of consumers all over the world with dairy products containing valuable nutrients.","potentialAction":[{"@type":"SearchAction","target":"https://www.frieslandcampinaingredients.com/?s={search_term_string}","query-input":"required name=search_term_string"}],"inLanguage":"en-US"},{"@type":"WebPage","@id":"#webpage","url":"","name":"","isPartOf":{"@id":"https://www.frieslandcampinaingredients.com/#website"},"breadcrumb":{"@id":"#breadcrumb"},"inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":[""]}]},{"@type":"BreadcrumbList","@id":"#breadcrumb","itemListElement":[{"@type":"ListItem","position":1,"item":{"@type":"WebPage","@id":"https://www.frieslandcampinaingredients.com/","url":"https://www.frieslandcampinaingredients.com/","name":"Home"}},{"@type":"ListItem","position":2,"item":{"@type":"WebPage","@id":"","url":"","name":""}}]}]}</script>
	<!-- / Yoast SEO plugin. -->


<link rel='dns-prefetch' href='//s.w.org' />
		<script type="text/javascript">
			window._wpemojiSettings = {"baseUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.0.1\/72x72\/","ext":".png","svgUrl":"https:\/\/s.w.org\/images\/core\/emoji\/13.0.1\/svg\/","svgExt":".svg","source":{"concatemoji":"https:\/\/www.frieslandcampinaingredients.com\/wp\/wp-includes\/js\/wp-emoji-release.min.js?ver=5.6"}};
			!function(e,a,t){var r,n,o,i,p=a.createElement("canvas"),s=p.getContext&&p.getContext("2d");function c(e,t){var a=String.fromCharCode;s.clearRect(0,0,p.width,p.height),s.fillText(a.apply(this,e),0,0);var r=p.toDataURL();return s.clearRect(0,0,p.width,p.height),s.fillText(a.apply(this,t),0,0),r===p.toDataURL()}function l(e){if(!s||!s.fillText)return!1;switch(s.textBaseline="top",s.font="600 32px Arial",e){case"flag":return!c([127987,65039,8205,9895,65039],[127987,65039,8203,9895,65039])&&(!c([55356,56826,55356,56819],[55356,56826,8203,55356,56819])&&!c([55356,57332,56128,56423,56128,56418,56128,56421,56128,56430,56128,56423,56128,56447],[55356,57332,8203,56128,56423,8203,56128,56418,8203,56128,56421,8203,56128,56430,8203,56128,56423,8203,56128,56447]));case"emoji":return!c([55357,56424,8205,55356,57212],[55357,56424,8203,55356,57212])}return!1}function d(e){var t=a.createElement("script");t.src=e,t.defer=t.type="text/javascript",a.getElementsByTagName("head")[0].appendChild(t)}for(i=Array("flag","emoji"),t.supports={everything:!0,everythingExceptFlag:!0},o=0;o<i.length;o++)t.supports[i[o]]=l(i[o]),t.supports.everything=t.supports.everything&&t.supports[i[o]],"flag"!==i[o]&&(t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&t.supports[i[o]]);t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&!t.supports.flag,t.DOMReady=!1,t.readyCallback=function(){t.DOMReady=!0},t.supports.everything||(n=function(){t.readyCallback()},a.addEventListener?(a.addEventListener("DOMContentLoaded",n,!1),e.addEventListener("load",n,!1)):(e.attachEvent("onload",n),a.attachEvent("onreadystatechange",function(){"complete"===a.readyState&&t.readyCallback()})),(r=t.source||{}).concatemoji?d(r.concatemoji):r.wpemoji&&r.twemoji&&(d(r.twemoji),d(r.wpemoji)))}(window,document,window._wpemojiSettings);
		</script>
		<style type="text/css">
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 .07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
	<link rel='stylesheet' id='wp-block-library-css'  href='https://www.frieslandcampinaingredients.com/wp/wp-includes/css/dist/block-library/style.min.css?ver=5.6' type='text/css' media='all' />
<link rel='stylesheet' id='addtoany-css'  href='https://www.frieslandcampinaingredients.com/app/plugins/add-to-any/addtoany.min.css?ver=1.15' type='text/css' media='all' />
<script type='text/javascript' src='https://www.frieslandcampinaingredients.com/wp/wp-includes/js/jquery/jquery.min.js?ver=3.5.1' id='jquery-core-js'></script>
<script type='text/javascript' src='https://www.frieslandcampinaingredients.com/wp/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2' id='jquery-migrate-js'></script>
<script type='text/javascript' src='https://www.frieslandcampinaingredients.com/app/plugins/add-to-any/addtoany.min.js?ver=1.1' id='addtoany-js'></script>
<link rel="https://api.w.org/" href="https://www.frieslandcampinaingredients.com/wp-json/" />

<script data-cfasync="false">
window.a2a_config=window.a2a_config||{};a2a_config.callbacks=[];a2a_config.overlays=[];a2a_config.templates={};
(function(d,s,a,b){a=d.createElement(s);b=d.getElementsByTagName(s)[0];a.async=1;a.src="https://static.addtoany.com/menu/page.js";b.parentNode.insertBefore(a,b);})(document,"script");
</script>
</head>

  <body class="theme-trends"  data-pagetype="treats_recipe" data-id=4721 data-template="base.twig">


 <div class="c-modal c-modal-form__modal" id="modal-download-recipe" data-modal-auto-focus="true" data-modal-no-body-class="false"js-hook-modal>

        <div class="modal__container">

            <div class="modal__content" role="dialog">

                
                            <div class="c-modal-form">
            <div class="c-modal-form__header">
                <h2 class="c-modal-form__title"></h2>
                            </div>

            <div class="c-modal-form__content">

                	<form class="c-form" id="form-download-recipe" action="#" method="post" js-hook-form-submit novalidate handler>
		<div class="signup-recording">
			<h2 id="recipe-download-title" class="title">
				Excellent choice!
			</h2>
			<div id="recipe-download-text" class="intro">
				Please fill in the fields below in order to download this recipe.
			</div>
			
    <div class="c-input form__item input--text">

        <div class="input__wrapper">
            <label class="input__label" for="input-first-name">
                First name*
            </label>
            <input class="input__input"
                type="text"
                name="firstName"
                value=""
                id="input-first-name" required placeholder="First name*">
        </div></div>



			
    <div class="c-input form__item input--text">

        <div class="input__wrapper">
            <label class="input__label" for="input-last-name">
                Last name*
            </label>
            <input class="input__input"
                type="text"
                name="lastName"
                value=""
                id="input-last-name" required placeholder="Last name*">
        </div></div>



			
    <div class="c-input form__item input--email">

        <div class="input__wrapper">
            <label class="input__label" for="input-mail">
                E-mail address*
            </label>
            <input class="input__input"
                type="email"
                name="email"
                value=""
                id="input-mail" required placeholder="E-mail address*">
        </div></div>



			
    <div class="c-input form__item input--text">

        <div class="input__wrapper">
            <label class="input__label" for="input-company">
                Company*
            </label>
            <input class="input__input"
                type="text"
                name="company"
                value=""
                id="input-company" required placeholder="Company*">
        </div></div>


			
    <div class="c-input form__item input--number">

        <div class="input__wrapper">
            <label class="input__label" for="input-phone">
                Phone Number*
            </label>
            <input class="input__input"
                type="number"
                name="phoneNumber"
                value=""
                id="input-phone" required placeholder="Phone Number*">
        </div></div>


			
    <div class="c-input form__item input--text">

        <div class="input__wrapper">
            <label class="input__label" for="input-country">
                Country*
            </label>
            <input class="input__input"
                type="text"
                name="country"
                value=""
                id="input-country" required placeholder="Country*">
        </div></div>


			
    <div class="c-select form__item">

        <div class="select__wrapper">
            <label class="select__label" for="regionReport">
                
            </label>
            <select class="select__input"
                name="region"
                id="regionReport" required>

                                    <option
                        disabled                        selected="selected"                                                value=""

                        >
                        Region*
                    </option>
                                    <option
                                                                                                value="EMEA"

                        >
                        EMEA
                    </option>
                                    <option
                                                                                                value="North America"

                        >
                        North America
                    </option>
                                    <option
                                                                                                value="Latin America"

                        >
                        Latin America
                    </option>
                                    <option
                                                                                                value="SEAP"

                        >
                        SEAP
                    </option>
                                    <option
                                                                                                value="Greater China"

                        >
                        Greater China
                    </option>
                
            </select>
        </div></div>


			
    <div class="c-select form__item">

        <div class="select__wrapper">
            <label class="select__label" for="trendingApplications">
                
            </label>
            <select class="select__input"
                name="trendingApplications"
                id="trendingApplications" required>

                                    <option
                        disabled                        selected="selected"                                                value=""

                        >
                        Application Area*
                    </option>
                                    <option
                                                                                                value="Instant Sachets"

                        >
                        Instant Sachets
                    </option>
                                    <option
                                                                                                value="Capsules & Pads"

                        >
                        Capsules & Pads
                    </option>
                                    <option
                                                                                                value="Foodservice Drinks"

                        >
                        Foodservice Drinks
                    </option>
                                    <option
                                                                                                value="Food"

                        >
                        Food
                    </option>
                                    <option
                                                                                                value="All applications"

                        >
                        All applications
                    </option>
                
            </select>
        </div></div>


			<p class="disclaimer">
				FrieslandCampina processes your data in line with our
				<a target="_blank" href="https://privacy.frieslandcampina.com/english/frieslandcampina-privacy-policy/">privacy statement</a>. 
												By submitting your data, you agree to share your data with our carefully selected distributor in your country and segment.
			</p>
			
    <div class="c-checkbox form__item checkbox--horizontal">

        <div class="checkbox__wrapper">
                    <div class="checkbox__content">
                <input class="checkbox__input u-sr-only"
                    type="checkbox"
                    name="dirMarketingOptIn"
                    value="accepted"
                    id="accept-terms-webinar">
                <label class="checkbox__label" for="accept-terms-webinar">
                    <div class="checkbox__label-text">
                        I agree to receive information and commercial offers from FrieslandCampina.
                    </div>
                </label>
            </div>
                </div></div>



			<div style="position:absolute; left:-9999px; top: -9999px;">
                <label for="pardot_extra_field">Comments</label>
                <input type="text" id="pardot_extra_field" name="pardot_extra_field">
            </div>

			<button id="recipe-download-btn" class="c-button--primary" type="submit">
				<span class="button__label">Download recipe</span>
			</button>
		</div>
	</form>
	
	</div>
        </div>
    

                
                                    
    <a class="c-close-button modal__button-close" js-hook-button-modal-close aria-label="Close modalbox">

        <svg class="svg--icons-close" width="24" height="24" xmlns="http://www.w3.org/2000/svg"><path d="M6.657 17.263L17.263 6.657m-10.606 0l10.606 10.606" stroke-width="2" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"/></svg>

        <span class="c-close-button__label">Close</span>

    </a>


                
            </div>

            <div class="modal__outside-click" js-hook-button-modal-close></div>

        </div>

        <div class="modal__background" js-hook-button-modal-close></div>
    </div>





	    
    <div class="c-modal" id="modal-iframe"js-hook-modal>

        <div class="modal__container">

            <div class="modal__content" role="dialog">

                
                                    
    <a class="c-close-button modal__button-close" js-hook-button-modal-close aria-label="Close modalbox">

        <svg class="svg--icons-close" width="24" height="24" xmlns="http://www.w3.org/2000/svg"><path d="M6.657 17.263L17.263 6.657m-10.606 0l10.606 10.606" stroke-width="2" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"/></svg>

        <span class="c-close-button__label">Close</span>

    </a>


                
            </div>

            <div class="modal__outside-click" js-hook-button-modal-close></div>

        </div>

        <div class="modal__background" js-hook-button-modal-close></div>
    </div>




				    
    
        
    <div class="c-modal c-modal-form__modal" id="modal-thank-download" data-modal-auto-focus="true" data-modal-no-body-class="false"js-hook-modal>

        <div class="modal__container">

            <div class="modal__content" role="dialog">

                
                            <div class="c-modal-form">
            <div class="c-modal-form__header">
                <h2 class="c-modal-form__title"></h2>
                            </div>

            <div class="c-modal-form__content">

                <div class="thank-you-content">
	<div class="image-wrapper">
		<img src="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/images/modal-down.jpg">
	</div>
	<div class="text-wrapper">
		<h2 class="title">
							Thank you
					</h2>
		<div class="text">
							Your file download will start in an instant. You can check out some on-trend, ready-to-go recipes <a id='openRecipe' href='/food-beverages/trends/'>here</a>.
					</div>
		<a id="thank-down" href="/food-beverages/trends/" class="c-button--primary">
			<span class="">Continue</span>
		</a>
						
			</div>
</div>



            </div>
        </div>
    

                
                                    
    <a class="c-close-button modal__button-close" js-hook-button-modal-close aria-label="Close modalbox">

        <svg class="svg--icons-close" width="24" height="24" xmlns="http://www.w3.org/2000/svg"><path d="M6.657 17.263L17.263 6.657m-10.606 0l10.606 10.606" stroke-width="2" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"/></svg>

        <span class="c-close-button__label">Close</span>

    </a>


                
            </div>

            <div class="modal__outside-click" js-hook-button-modal-close></div>

        </div>

        <div class="modal__background" js-hook-button-modal-close></div>
    </div>
    
        <script type='text/javascript' id='ajax_script-js-extra'>
/* <![CDATA[ */
var myAjax = {"ajax_url":"https:\/\/www.frieslandcampinaingredients.com\/wp\/wp-admin\/admin-ajax.php"};
/* ]]> */
</script>
<script type='text/javascript' src='https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/scripts/ajax.js?ver=1' id='ajax_script-js'></script>
<script type='text/javascript' id='region_script-js-extra'>
/* <![CDATA[ */
var myAjax = {"ajax_url":"https:\/\/www.frieslandcampinaingredients.com\/wp\/wp-admin\/admin-ajax.php"};
/* ]]> */
</script>
<script type='text/javascript' src='https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/scripts/recipesFilter.js?ver=1619431103' id='region_script-js'></script>


    
        <script src="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/js/main.js?ver=1619431103"></script>
      <!-- <script type="module" src="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/js/main-es.js"></script>
      <script nomodule src="https://www.frieslandcampinaingredients.com/app/themes/frieslandcampina/assets/js/main.js"></script> -->
      <script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.eu01.nr-data.net","licenseKey":"NRJS-7a0deee73b6de246708","applicationID":"41455697","transactionName":"MhBSZQoZWkYDBhBYXQtaZUMRV11bBgAcH0INBQ==","queueTime":0,"applicationTime":9075,"atts":"HldRE0IDSUg=","errorBeacon":"bam.eu01.nr-data.net","agent":""}</script></body>

</html>
