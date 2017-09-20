---
layout: chess_post
title: Defensa Caro-kann
---

<head>
  <link rel="stylesheet" href="../chessWebsite/css/chessboard-0.3.0.css" />
</head>
<body>

  <script src="../chessWebsite/jquery/jquery-3.2.1.min.js"></script>
  <script src="../chessWebsite/js/chess.js"></script>
  <script src="../chessWebsite/js/chessboard.js"></script>
  <center><div id="myBoard" style="width: 200px"></div></center>

<script type="text/javascript">

      var init = function() {
            var board, game = new Chess();
            var makeRandomMove = function(move) {
                game.move(move);
                board.position(game.fen());
            };

            var cfg = {
              position: 'start'
            };
            board = new ChessBoard('#myBoard', cfg);
    
            setTimeout(function(){ makeRandomMove('e4'); }, 3000);
            setTimeout(function(){ makeRandomMove('e5'); }, 6000);
        };
        jQuery(document).ready(init);
  </script>