<div class="container" id="jigsaw-puzzle">
  <p class="lead">Drag the pieces into the grid to complete the puzzle and see what the detective found.</p>
  <div class="row">
    <div class="col-md-6">
      <div class="row" id="puzzle-pieces-area">
      </div>
      <div class="row" id="jigsaw-complete-video">
        <div class="embed-responsive embed-responsive-16by9">
          <iframe src="https://www.youtube-nocookie.com/embed/dQw4w9WgXcQ?modestbranding=1&rel=0" frameborder="0" allow="encrypted-media; picture-in-picture" allowfullscreen="" class="embed-responsive-item"></iframe>
        </div>
      </div>
    </div>
    <div class="col-md-6">
      <div id="puzzle-working-area">
        <div class="row">
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="0"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="1"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="2"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="3"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
        </div>
        <div class="row">
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="4"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="5"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="6"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="7"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
        </div>
        <div class="row">
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="8"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="9"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="10"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
          <div class="col-3 jigsaw-space jigsaw-drop-space" data-piece="11"><img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" class="jigsaw-space-holder" /></div>
        </div>
      </div>
      <div id="jigsaw-complete">
        <img src="https://awmb.uk/codepenassets/jigsaw/complete-puzzle.png" alt="" class="w-100"/>
      </div>
    </div>
  </div>
</div>
body {
  background-color: #282828;
  color: #f9f9f9;
}

.container {
  padding-top: 15px;
}

.jigsaw-piece {
  padding: 0.5px;
  width: 100%;
  z-index: 500;
}

.jigsaw-piece.ui-draggable-dragging {
  box-shadow: 0 0 20px rgba(0, 0, 0, .8);
  transition: box-shadow .2s;
  z-index: 1000;
}

#puzzle-working-area .row .col-md-3 {
  border: 1px solid #f9f9f9;
}

.jigsaw-space {
  padding: 0;
}

.jigsaw-drop-space {
  border: 0.5px solid #f3f3f3;
}

.jigsaw-space-holder {
  width: 100%;
  margin: 0;
  padding: 0;
  visibility: hidden;
}

#jigsaw-complete, #jigsaw-complete-video {
  display: none;
}
// Images for each piece
var pieces = [
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_001.jpg" alt="" data-piece="0" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_002.jpg" alt="" data-piece="1" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_003.jpg" alt="" data-piece="2" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_004.jpg" alt="" data-piece="3" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_005.jpg" alt="" data-piece="4" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_006.jpg" alt="" data-piece="5" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_007.jpg" alt="" data-piece="6" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_008.jpg" alt="" data-piece="7" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_009.jpg" alt="" data-piece="8" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_010.jpg" alt="" data-piece="9" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_011.jpg" alt="" data-piece="10" class="jigsaw-piece"/>',
  '<img src="https://awmb.uk/codepenassets/jigsaw/image_part_012.jpg" alt="" data-piece="11" class="jigsaw-piece"/>'
];

// Function to shuffle array
function shuffle(a) {
  var j, x, i;
  for (i = a.length - 1; i > 0; i--) {
    j = Math.floor(Math.random() * (i + 1));
    x = a[i];
    a[i] = a[j];
    a[j] = x;
  }
  return a;
}

// Function to print a puzzle piece in its div
function printPiece(item, index) {
  document.getElementById("puzzle-pieces-area").innerHTML += '<div class="col-3 jigsaw-space">' + item + '</div>';
}

// Function to use when the jigsaw is complete
function jigsawComplete() {
  $("#puzzle-pieces-area").slideUp();
  $("#jigsaw-complete-video").slideDown();
  $("#puzzle-working-area").hide();
  $("#jigsaw-complete").show();
}

// Shuffle the pieces
shuffle(pieces);
// Print the pieces
pieces.forEach(printPiece);

// Jigsaw puzzle status - true if the piece is in the correct place, false otherwise
var jigsawStatus = Array(pieces.length).fill(false);

$( document ).ready(function() {
  // Make pieces draggable
  $(".jigsaw-piece").draggable({
    // Snap to the puzzle grid
    snap: ".jigsaw-space-holder",
    snapMode: "inner",
    // When a piece starts to move, mark it as in the wrong place
    start: function( event, ui ) {
      jigsawStatus[$(this).data("piece")] = false;
    }
  });
  
  // Make the puzzle grid droppable
  $(".jigsaw-drop-space").droppable({
    // When something is dropped in a grid square
    drop: function(event, ui) {
      // Check if this is the right place for the piece or not, and update the array
      if ($(this).data("piece") == ui.draggable.data("piece")) {
         jigsawStatus[$(this).data("piece")] = true;
       } else {
         jigsawStatus[$(this).data("piece")] = false;
       }
      
      // If every item in the puzzle is in the correct place, the jigsaw is complete!
      if (jigsawStatus.every(function (value) { return value; })) {
        jigsawComplete();
      }
    }
  });
});
