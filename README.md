# Minesweeper
This is a project part of the CS50AI course. I have written the functions: in the sentence class :known_mines, known_safes, mark_mine, and mark_safe. In the MinesweeperAI class: add_knowledge, make_safe_move, and make_random_move.
Minesweeper is a puzzle game that consists of a grid of cells, where some of the cells contain hidden “mines.” Clicking on a cell that contains a mine detonates the mine, and causes the user to lose the game. 
Clicking on a “safe” cell (i.e., a cell that does not contain a mine) reveals a number that indicates
how many neighboring cells – where a neighbor is a cell that is one square to the left, right, up, down, or diagonal from the given cell – contain a mine.

The minesweeper.py file inculdes an AI that can play the game using a knowledge based approach.
The knowledge of the AI (knowledge based agent) is represtened using logical sentence.
Every logical sentence in this representation has two parts: a set of cells on the board that are involved in the sentence, and a number count, representing the count of how many of those cells are mines. 
For example: {A, B, C, D, E, F, G, H} = 1, This sentence means that one of the cells from A to H contains a mine. Add to it the sentence: {D, E, G} = 0, now the AI can infer that {A, B, C, F, H} = 1, and so on until a sentence length 
equal it's value meaning that all of it's cells are mines. 
For the AI to play a move, it eithers make a random move if it doesnt know any safe moves. Or it plays a move that it infered being safe such as one the cells from the previuos sentence: {D, E, G} = 0. 
