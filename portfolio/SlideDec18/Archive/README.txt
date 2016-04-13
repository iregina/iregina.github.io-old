A Pen created at CodePen.io. You can find this one at http://codepen.io/anon/pen/gPrRJW.

 Goal: create a nicely styled cross-browser 1 element slider. Tested & works in Firefox 36, 39 (nightly), Chrome 41, 43 (canary)/ Opera 28, IE 11 on Windows 8. CSS-only in Firefox & IE/ not much JS needed for Chrome/ Opera. 

Has a couple of nice extras in Chrome/ Opera - displaying a nice tooltip above the thumb. This is achieved by using pseudo elements on the thumb. This is something that didn't work until recently, so I'm also using `/deep/` - careful, experimental stuff, only supported in Blink, [the spec has already changed](http://dev.w3.org/csswg/css-scoping-1/#deep-combinator), no future really, already not working anymore in canary - see ([link #1](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/hRw781MV3mE/pQHWrsKhmj0J), [link #2](https://code.google.com/p/chromium/issues/detail?id=433977)). 

I can also get a tooltip with the current value in IE via [`::-ms-tooltip`](https://msdn.microsoft.com/en-us/library/windows/apps/hh465805.aspx), but I cannot style that asshole. 

Fallback for no JS in Chrome/ Opera: same background both before and after the thumb and no tooltip. 

**Disclaimer because some people got the wrong idea: I did NOT design these sliders.** Whoever knows me is probably aware of the fact that I'm 100% technical and 0% artistic. Me trying to design something would result in visual vomit. I just googled "slider design" and tried to reproduce (as well as I could) the images that search found. Inspiration for this demo: 

![image](http://i.imgur.com/ECXZwyY.jpg) 

From [here](http://slayerd1.deviantart.com/art/Slider-Progress-Bar-265703323). 

You can see the rest of my 1 range input sliders in [this collection](http://codepen.io/collection/DgYaMj/).  

Forked from [Ana Tudor](http://codepen.io/thebabydino/)'s Pen [prettify `<input type=range>` #93](http://codepen.io/thebabydino/pen/PwxKjm/).