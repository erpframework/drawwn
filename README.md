drawwn
(draw so easy, you'll yawn)

by Fraywing
======

Super easy javascript canvas drawing UI and tool with build with oCanvas, color picker, and easy slider.

TO USE:

Simple add (or dynamically load) the drawwn.js development file, or the drawwn.min.js minified file into your page; along with the drawwn.css file.

initialize the constructor with:

 var can = $('#yourElement').drawwn({
        "tools" : {  //add or remove tools
            "circle" : true,
            "arrow" : true,
            "line" : true,
            "text" : true,
            "selector" : true
        },
        "zoom" : true, //doesn't work
        "colors" : true, 
        "loadImage" : true,
        "exportImage" : function(image){ //optional exported image callback function, gets the image as base64
           var img = "<img src='"+image+"' />";
            $('body').append(img);
        },
        "background" : "#d3d3d3", //background for canvas
        "height" : "700px", //height
        "width" : "1000px" //width
        });
        
        EXTRA:
        
       can.waitTillReady(function(o){ //use to wait until ready to load an image into drawwn
          o.loadImage("/js/images/backFlips.png");
        });
