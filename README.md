<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chess Game</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f8f8f8;
        }
        .board {
            display: grid;
            grid-template-columns: repeat(8, 60px);
            grid-template-rows: repeat(8, 60px);
            border: 5px solid black;
        }
        .square {
            width: 60px;
            height: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 30px;
        }
        .dark { background-color: #769656; }
        .light { background-color: #eeeed2; }
    </style>
</head>
<body>
    <div class="board">
        <script>
            const board = document.querySelector(".board");
            const pieces = ["♖","♘","♗","♕","♔","♗","♘","♖"];
            const pawns = "♙";
            const blackPieces = pieces.map(p => p.replace("♖","♜").replace("♘","♞").replace("♗","♝").replace("♕","♛").replace("♔","♚"));
            const blackPawns = "♟";for (let row = 0; row < 8; row++) {
            for (let col = 0; col < 8; col++) {
                const square = document.createElement("div");
                square.className = square ${(row + col) % 2 === 0 ? "light" : "dark"};
                
                if (row === 0) square.textContent = blackPieces[col];
                if (row === 1) square.textContent = blackPawns;
                if (row === 6) square.textContent = pawns;
                if (row === 7) square.textContent = pieces[col];
                
                board.appendChild(square);
            }
        }
    </script>
</div>

</body>
</html># chess-game
