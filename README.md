## Update
Does not work reliably. Bing treats links to the same result from different searches as different results.

## Bing userstyle for links

The Bing search engine has a usability issue that stems from broken presentational hints on links. All links are colored as purple,
giving no indication of which links are visited and which are not.

This seems to be an [old problem](https://www.bing.com/search?q=bing+all+links+purple), keeping this userstyle relevant.

This userstyle sets the color of unvisited links to blue and visited links to purple as per [standard guidelines](https://html.spec.whatwg.org/multipage/rendering.html#phrasing-content-3).

## Applying the userstyle in your browser

There are two ways of applying the userstyle:

- #### With uBlock Origin

  If you already use uBlock Origin and don't want to install Stylish, you can add these lines to your custom filters:
  ```
  www.bing.com#$#main #b_results > li a{color:#0000EE !important}
  www.bing.com#$#main a:visited, #b_results > li a:visited{color:#551A8B !important}
  ```

- #### With Stylish

  First, install Stylish: ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/stylish/), [Chrome](https://chrome.google.com/webstore/detail/stylish-custom-themes-for/fjnbnpbmkenffdnngjfgmeleoegfcffe))

  Then install this userstyle from https://userstyles.org/styles/263172/bing-link-color-fixer
