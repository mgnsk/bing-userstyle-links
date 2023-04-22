## Bing userstyle for links

The Bing search engine has a usability issue that stems from missing presentational hints on links. All links are colored as purple,
giving no indication of which links are visited and which are not.

This userstyle sets the color of unvisited links to blue and visited links to purple as per standard guidelines: https://html.spec.whatwg.org/multipage/rendering.html#phrasing-content-3.

## Applying the userstyle in your browser

For userstyles, I recommend Stylish ([Firefox](https://addons.mozilla.org/en-US/firefox/addon/stylish/), [Chrome](https://chrome.google.com/webstore/detail/stylish-custom-themes-for/fjnbnpbmkenffdnngjfgmeleoegfcffe))



### Update as of April 2023
At first glance it looks like they have fixed the styles on Firefox where the colors for unvisited and visited links are different:

- Links:
  ```css
  #b_results > li a {
      color: #1a0dab;
  }
  a:visited, #b_results > li a:visited {
      color: #4a148c;
  }
  ```
  
But after some usage, Firefox also breaks as Bing starts serving the wrong CSS for no reason (even in tabs that had correct colors earlier, have wrong colors after a refresh):
- Links:
  ```css
  #b_results>li a {
      color: #4007a2;
  }
  a:visited, #b_results > li a:visited {
      color: #4007a2;
  }
  ```

Some chromium-based browsers are still clearly broken as unvisited and visited links share the same color:

- Links:
  ```css
  #b_results>li a {
      color: #4007a2;
  }
  a:visited, #b_results>li a:visited {
      color: #4007a2;
  }
  ```

This seems to be an [old problem](https://www.bing.com/search?q=bing+all+links+purple), keeping this userstyle relevant.
