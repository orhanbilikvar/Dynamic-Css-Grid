# Dynamic Css Grid

Dynamic Css Grid

https://codepen.io/orhanblv/pen/wbBGRO

JS

var parent = document.getElementById("main");

var countClass = parent.getElementsByClassName("cols-1");

console.log(countClass.length);

var CountA = countClass.length;

var CountB = CountA / 3;

CountB = Math.floor(CountB);

CountC=CountA - (CountB*3);

CountD=3-CountC;

if (CountA>3) {

    if ( CountD == 1 ) {
        var element = document.getElementById("blog");
        element.classList.add("oneSpace");

    }
    if (CountD == 2) {
        var element = document.getElementById("blog");
        element.classList.add("twoSpace");
    }
}


CSS

.blog .blogic.oneSpace > div:nth-child(1) {
    grid-row: 1/3;
}

.blog .blogic.twoSpace > div:nth-child(1) {
    grid-row: 1/3;
}

.blog .blogic.twoSpace > div:nth-child(2) {
    grid-row: 1/3;
}

HTML

<div id="main">

<div class="blog">
    
    <div class="blogic" id="blog">
    
          <div class="cols-1"></div>
          
          <div class="cols-1"></div>
          
          <div class="cols-1"></div>
          
          <div class="cols-1"></div>
          
      </div>
      
 </div>

</div>

![Dynamic Css Grid](https://github.com/obilikvar/Dynamic-Grid/blob/master/taslak_r2_c1.jpg)
