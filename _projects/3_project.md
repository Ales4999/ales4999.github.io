---
layout: page
title: Tic-Tac-Toe Game on STM32 Board
description: STM32 Tic-Tac-Toe Game with HAL, Interrupts, and Timers
img: assets/img/emd_board.jpg
importance: 3
category: work
---

This project features a fully implemented Tic-Tac-Toe game on an STM32F429i Discovery Board, focusing on integrating peripherals via the HAL, handling external interrupts for user input, and using timers to manage game timing. An AI opponent was created using RNG for single-player mode.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emb_codeHier.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/emb_board2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This was my final project for ECEN 2370 - Embedded Systems. It is an implementation of the known and loved game of Tic-Tac-Toe using a STM32F429i Discovery Board. This project relies on the effective use of the HAL (Hardware Abstraction Layer) in order to correctly access and manipulate the peripherals from the board in order to implement the game functionality.  The game allows for 2 playing modes, single player and multiplayer respectively, as well as accurate tracking of playing time and total record of wins. 
</div>

<div class="project-scope mt-4">
  <h3>Project Scope</h3>
  <p>This project scope covered virtually all the topics learned throughout the course. The breakdown is as follows:</p>
  
  <ul>
    <li><strong>Utilized Peripherals:</strong>
      <ul>
        <li><strong>RNG (Random Number Generator):</strong> Used for random moves in the game.</li>
        <li><strong>Timers:</strong> Used for timing game events.</li>
        <li><strong>Interrupts:</strong> Used for handling user input and game reset logic.</li>
        <li><strong>LCD Screen:</strong> Displayed the intro screen, game board, and game result screen.</li>
      </ul>
    </li>
    
    <li> <strong>Tic-Tac-Toe Game:</strong>
      <ul>
        <li>Standard 3x3 game board.</li>
        <li>User selects either single player or multiplayer mode.</li>
        <li>Implemented X’s and O’s.</li>
        <li>Game ends when someone gets 3 in a row or if there is a stalemate.</li>
      </ul>
    </li>
    
    <li><strong>Additional Requirements Implemented:</strong>
      <ul>
        <li>Created two screens besides the game board screen:
          <ul>
            <li>One for selecting the game mode.</li>
            <li>One for displaying game results, time elapsed, and current record (W-L-Ties).</li>
          </ul>
        </li>
        <li>Implemented AI logic for 1 player using the RNG (brute force possibilities).</li>
      </ul>
    </li>
  </ul>
</div>

<div class="key-features mt-4"> 
    <h3>Key Features</h3> 
    <ul> 
    <li>Designed a <strong>user-friendly interface</strong> on the LCD screen for game mode selection, gameplay, and result display.</li>
    <li>Created <strong>AI opponent</strong> using RNG-based logic for dynamic single-player mode.</li>
    <li>Utilized <strong>HAL</strong> for peripheral control, including the LCD, timers, and RNG.</li>
    <li>Implemented <strong>external interrupts</strong> for user input and game resets.</li>
    </ul> 
</div>

<div class="project-pdf mt-4">
  <h3>Project Documentation</h3>
    <iframe src="/assets/pdf/emb_doc.pdf" width="100%" height="800px"></iframe>
</div>