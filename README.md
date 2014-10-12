custom-twitter-widget
=====================

A simple way to customize your iframe twitter widget.

Take the following simple steps

1. Copy and paste the anchor tag on your html code.
2. Instead of using the javascript twitter provides, use the one below

<script>
!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";js.setAttribute('onload', "twttr.events.bind('rendered',function(e) {customize()});");fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");

function customize(){
	jQuery("#twitter-widget-0").contents().find('head').append("<link rel='stylesheet' type='text/css' href='YOUR-CSS-URL'");
}

</script>

3. The only thing you will have to change is the href attribute on the customize function
4. WARNING : YOUR BROWSER MIGHT CACHE THE CSS FILE YOU ARE USING SO YOUR CHANGES MIGHT NOT BE VISIBLE RIGHT AWAY.
5. ENJOY !