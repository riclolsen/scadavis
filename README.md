<a href="https://scadavis.io/">
    <img src="https://github.com/riclolsen/scadavis/raw/master/src/images/scadavis.svg" alt="SCADAvis.io Logo" title="SCADAvis.io" align="right" height="60" />
</a>

[SCADAvis.io](https://scadavis.io/)
============

HTML5 Synoptic Graphics Toolkit. SCADA-like realtime visualization tools for the web.

![](https://img.shields.io/badge/license-GPL-green "License GPL")

## Mission Statement

To provide a powerful toolkit for the producing of SCADA-like SVG displays for modern web browser platforms.

## Major features

* Pure HTML5/Javascript/SVG runtime.
* Use a custom Inkscape SVG Editor to create displays.
* Link tagged realtime data to SVG animations at runtime.
* Mobile friendly, framework agnostic.
* No special server requirements needed.

## Example Javascript code

    scadavis({
        container: "div1",
        iframeparams: 'frameborder="0" height="490" width="555"',
        svgurl: "https://raw.githubusercontent.com/riclolsen/displayfiles/master/office.svg"
    }).then( function (sv) {
        setInterval(function () {
            sv.storeValue("TAG1", Math.random() * 100);
            sv.storeValue("TAG2", 100 + Math.random() * 80);
            sv.storeValue("TAG3", 120 + Math.random() * 60);
            sv.storeValue("TAG4", 150 + Math.random() * 60);
            sv.storeValue("TAG5", 110 + Math.random() * 30);
            sv.storeValue("TAG6", 200 + Math.random() * 100);
            sv.storeValue("TAG7", 130 + Math.random() * 40);
            sv.updateValues();
        }, 2500);
        sv.zoomTo(0.65);  
    })

## Substation Simulation Example

https://codepen.io/ricardolo/pen/MWXmPpB




