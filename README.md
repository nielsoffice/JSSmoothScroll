# JSSmoothScroll
JavaScript smooth scroll effect

```HTML
<!-- HTML MENU LINK -->
<div id="div_block-42-384" class="hp-tab-menu-items">
  <a id="text_block-43-384" class="hp-blog-submenu" href="#HPLatest">Latest</a>
  <a id="text_block-44-384" class="hp-blog-submenu" href="#HPBranding">Branding</a>
  <a id="text_block-45-384" class="hp-blog-submenu" href="#HPDigital">Digital</a><
</div>
  
 <!-- HTML CONTENT LINKED ON -->
  <div id="div_block-2308-389" class="ct-div-block"><h2 id="HPPrint" class="ct-headline">Print</h2></div>
  <div id="div_block-2308-389" class="ct-div-block"><h2 id="HPBranding" class="ct-headline">Branding</h2></div>
  <div id="div_block-2308-389" class="ct-div-block"><h2 id="HPDigital" class="ct-headline">Digital</h2></div>
```

```CSS
 #div_block-2308-389 { margin-bottom: 750px; }
```

```JS
(function() {
	
 let eTarget = document.querySelectorAll('.hp-blog-submenu');

     eTarget.forEach(function( v, k ) {

	  
	 let cID = v.id;
	 let _id = document.querySelector('#'+cID);	
		
	 _id.addEventListener('click', function( __event ) { __event.preventDefault();
		
		 document.querySelector(this.getAttribute('href')).scrollIntoView({ 
			
			behavior: "smooth" 
		 
		 });														
	  });	
	}); 
			
})();
```

<br />Reference: 
<br />https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView#examples
