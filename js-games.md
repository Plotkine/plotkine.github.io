---
title: /js-games
layout: games
permalink: /js-games
---

# Games I made with <a href="https://p5js.org/" target="_blank" rel="noopener noreferrer">p5.js</a>

## Snake

<iframe src="https://editor.p5js.org/Plotkine/present/wt0UfN_ce" width="500px" height="575px" frameBorder="0" title="snake"></iframe>

## Freddie game

<iframe src="https://editor.p5js.org/Plotkine/present/_6t0LDFnp" width="750px" height="750px" frameBorder="0" title="freddieGame"></iframe>

<!-- disable scrolling with arrows -->
<script> 
  var el_up = document.getElementById("GFG_UP"); 
  var el_down = document.getElementById("GFG_DOWN"); 
  el_up.innerHTML = "Click on the button to disable" 
                  + " scrolling through arrow keys."; 
          
  function gfg_Run() { 
    window.addEventListener("keydown", function(e) { 
      if([32, 37, 38, 39, 40].indexOf(e.keyCode) > -1){ 
        e.preventDefault(); 
      } 
    }, false); 
              
    el_down.innerHTML = "Scrolling from arrow keys is disabled."; 
  }
  gfg_Run();          
</script>
