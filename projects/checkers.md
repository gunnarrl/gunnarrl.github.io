---
layout: project
type: project
image: img/checkers.jpg
title: "Checkers vs. AI"
date: 2024
published: true
labels:
  - Machine Learning
  - Games
  - Python
summary: "Created an app where you can play checkers against a friend or varying levels of AI"
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

This is a checkers app that I made using pygame in python. You can either play against your friends on the same machine or against 3 levels of AI. The AI was made using the minimax algorithm with varying levels
of depth depending on the difficulty. This works well because checkers is not a very complex game so it is reasonable to check all possible move sequences. The project taught me a lot about object-oriented design
and how to implement it.

The hardest part was turning the minimax algorithm into code, here is the minimax code:
```
def minimax(self, board, depth, alpha, beta, maximizing_player):
        if depth == 0 or board.is_game_over():
            return self.evaluate_board(board), None

        best_move = None
        if maximizing_player:
            max_eval = float('-inf')
            for move in self.get_all_moves(board, self.color):
                board_copy = board.copy()
                board_copy.move_piece(move[0], move[1])
                eval, _ = self.minimax(board_copy, depth - 1, alpha, beta, False)
                if eval > max_eval:
                    max_eval = eval
                    best_move = move
                alpha = max(alpha, eval)
                if beta <= alpha:
                    break
            return max_eval, best_move
        else:
            min_eval = float('inf')
            for move in self.get_all_moves(board, -self.color):
                board_copy = board.copy()
                board_copy.move_piece(move[0], move[1])
                eval, _ = self.minimax(board_copy, depth - 1, alpha, beta, True)
                if eval < min_eval:
                    min_eval = eval
                    best_move = move
                beta = min(beta, eval)
                if beta <= alpha:
                    break
            return min_eval, best_move
```

The project is on my github at https://github.com/gunnarrl/checkers-vs-AI
