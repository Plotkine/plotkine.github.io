---
title: /home
layout: homepages
permalink: /
---

<!-- <h1>Welcome to my blog!</h1> -->

<p>[this blog sucks on mobile]</p>

<h1>plotkine@blog:~$ whoami</h1>

<p>I am an information security engineer who studied mathematics, based in Brussels and interested in:
- Programming
- Penetration testing</p>

<style>
#background {
  width: 475px;
  height: 475px;
  position: relative;
  background: #000000;
  border-style: solid;
  border-color: #00ff00;
}
.animate {
  width: 5px;
  height: 5px;
  position: absolute;
  background-color: #00ff00;
}
</style>

<script>
function isIn(i,j,aList) { // aList is a list of 2-lists
  for (let k = 0; k < aList.length; k++) {
    if ((aList[k][0] === i) && (aList[k][1] === j)) {
      return true;
    }
  }
  return false;
}

function evolve(i,j,aList) { // game of life rules for the cell i,j
  // calculating number of alive neighbors
  aliveNeighbors=0;
  if (isIn((((i-1) % squaresDivision) + squaresDivision) % squaresDivision,(((j-1) % squaresDivision) + squaresDivision) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn((((i-1) % squaresDivision) + squaresDivision) % squaresDivision,j % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn((((i-1) % squaresDivision) + squaresDivision) % squaresDivision,(j+1) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn(i % squaresDivision,(((j-1) % squaresDivision) + squaresDivision) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn(i % squaresDivision,(j+1) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn((i+1) % squaresDivision,(((j-1) % squaresDivision) + squaresDivision) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn((i+1) % squaresDivision,j % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn((i+1) % squaresDivision,(j+1) % squaresDivision,aList)) {
    aliveNeighbors+=1;
  }
  if (isIn(i,j,aList)) { // if the cell (i,j) was alive
    if ((aliveNeighbors !== 2) && (aliveNeighbors !== 3)) {
      return "becomesDead";
    }
    else {
      return "staysAlive";
    }
  }
  else { // if the cell (i,j) was not alive
    if (aliveNeighbors === 3) { // the cell becomes alive
      return "becomesAlive";
    }
    else {
      return "staysDead";
    }
  }
}

function createInitialPattern() {
  return [[5,5],[6,5],[7,5],   [10,10],[10,11],[10,12],    [15,15],[16,16],[17,16],[17,15],[17,14]];
}

function draw() {
  //clearing previously drawn cells
  document.getElementById("background").innerHTML = "";
  //we draw the (alive) cells
  for (const aliveCell of aliveCells) {
    drawAliveCell(aliveCell[0], aliveCell[1]);
  }

  //we evolve the cells
  aliveCellsCopy=Array.from(aliveCells);
  for (let i = 0; i <= squaresDivision; i++) {
    for (let j = 0; j <= squaresDivision; j++) {
      willEvolve=evolve(i,j,aliveCellsCopy);
      if (willEvolve === "becomesDead") {
        for(var k = 0; k < aliveCells.length; k++) { //we remove the cell from the list
          if ((aliveCells[k][0] === i) && (aliveCells[k][1] === j)) {
            aliveCells.splice(k,1);
            break; //we know it can be there only once
          }
        }
      }
      else if (willEvolve === "becomesAlive") {
        aliveCells.push([i,j]);
      }
    }
  }
}

function drawAliveCell(i,j) {
  leftValue = (i * 5).toString() + "px"
  topValue  = (j * 5).toString() + "px"
  document.getElementById("background").innerHTML += "<div class=\"animate\" style=\"top:" + topValue + "; left:" + leftValue + ";\"></div>"
}
</script>
</head>

<body>

<div id="background"></div>

<script>
fps=30; // frames per second
squaresDivision=95; // number of squares per row/column
aliveCells = createInitialPattern();
setInterval(draw, 1000/fps);
</script>
