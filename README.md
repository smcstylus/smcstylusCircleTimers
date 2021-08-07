# smcstylusCircleTimers
jQuery SMCstylus Circle Timers is a jQuery plugin that provides beautiful animated countdowns in circle shapes.

Features: You can fill the center of circles, the past time lines and the left time lines with solid or gradient colors. There is also the possibility to change the cap style of animated line. Add separate shadow (color and diffuse) for main timer and left time lines and more...

Down bellow is the implementation of this plugin in an Wordpress Elementor Addon
<a href="https://github.com/smcstylus/smcstylus-Addons-for-Elementor" title="SMCstylus Addons for Elementor">
  <img src="smcstylusCircleTimers.jpg" alt="smcstylusCircleTimers">
</a>

Plugin options:
<pre>
circleTimerArgs = {
  animation: string, // "smooth"
  direction: string, // "Booth"
  labelSize: float, // (10 / 100)
  numberSize:float, // (28 / 100)
  innerFill: boolean, // false
  innerUseGradient: boolean, // false
  innerBackgroundColors: array, // ["#ffcc00"]
  innerCenterSize: integer, // 5
  innerShadowBlur: integer, // 0
  innerShadowColor: string, // "#00000000"
  pastTimeLineShow: boolean, // true
  pastTimeLineWith: float, // 0.15
  pastTimeLineUseGradient: boolean,  // true
  pastTimeLineColors: array, // ["#FFF602", "#447A47"]
  pastTimeLineGradPoints: array, // [5, 101, 0, 0]
  pastTimeLineShadowBlur: integer // 0
  pastTimeLineShadowColor: string, // "#000000"
  pastTimeLineShadowCoordinates:array, // [0, 0]
  leftTimeLineWidth: float, // 0.08
  leftTimeLineCap: string, // "round" 
  leftTimeLineUseGradient: boolean, // true
  leftTimeLineColors: array, // ["#72B96F","#B9B76F"]
  leftTimeLineIndividualColors:boolean, // false
  leftTimeLineShadowBlur: integer, // 3
  leftTimeLineShadowColor: string, // "#262F2F"
  leftTimeLineShadowCoordinates: array, // [3, 4]
  leftTimeLineUIEffect: integer, // 0
  time: {
  Days: {
    show: boolean,
    text: string, // "Zile"
    color: string, // ["#f6008b"]
    gradient: boolean,
  },
  Hours: {
    show: boolean,
    text: string,
    color: string,
    gradient: boolean,
  },
  Minutes: {
    show: boolean,
    text: string,
    color: string,
    gradient: boolean,
  },
  Seconds: {
    show: boolean,
    text: string,
    color: string,
    gradient: boolean,
  },
};

$(el)
.smcstylusCircleTimers(circleTimerArgs);         
</pre>  
  Rebuild on resize
<pre>
$(window).resize(() => {
  $(el).smcstylusCircleTimers().rebuild();
});
</pre>
  Add listener
<pre>
$(el)
.smcstylusCircleTimers(circleTimerArgs)
.addListener(countdownCompleteListener);       
</pre>
 Action on document load
<pre>
$(document).ready(() => {
  if ($(el).data("tc-act") === "ended") {
    let el = $(el).smcstylusCircleTimers(circleTimerArgs);
    // Call your function
    countdownComplete(el.elements[0]);
  }
});
</pre>
            
