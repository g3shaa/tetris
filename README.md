<h1>Tetris Code Documentation</h1>

<h2>1. Overview of the Code</h2>

<h3>1.1. Description</h3>
<p>
    The provided code is an implementation of the Tetris game in Python using the Pygame library. The game consists
    of two main components: blocks (<code>Block</code>) and tetrominoes (<code>Tetromino</code>). Additionally, the
    code includes classes for rendering text (<code>Text</code>) and managing the game process (<code>Tetris</code>).
</p>

<h3>1.2. Project Structure</h3>
<p>
    - <code>settings.py</code>: File containing constants and game settings.<br>
    - <code>tetromino.py</code>: Implementation of the <code>Block</code> and <code>Tetromino</code> classes.<br>
    - <code>main.py</code>: Main application file containing the <code>App</code> class, which initializes the
    game and runs the game loop.
</p>

<h2>2. Settings Module (<code>settings.py</code>)</h2>

<h3>2.1. Constants</h3>
<p>
    - <code>FPS</code>: Frames per second for the game loop.<br>
    - <code>FIELD_COLOR</code>, <code>BG_COLOR</code>: Colors used for the game field and background.<br>
    - <code>SPRITE_DIR_PATH</code>, <code>FONT_PATH</code>: Paths to directories containing sprites and fonts.<br>
    - <code>ANIM_TIME_INTERVAL</code>, <code>FAST_ANIM_TIME_INTERVAL</code>: Animation time intervals.<br>
    - <code>TILE_SIZE</code>: Size of individual tiles.<br>
    - <code>FIELD_SIZE</code>: Dimensions of the game field.<br>
    - <code>FIELD_RES</code>, <code>WIN_RES</code>: Resolutions for the field and the game window.<br>
    - <code>INIT_POS_OFFSET</code>, <code>NEXT_POS_OFFSET</code>: Initial and next positions for tetrominoes.<br>
    - <code>MOVE_DIRECTIONS</code>: Dictionary mapping key presses to movement vectors.<br>
    - <code>TETROMINOES</code>: Dictionary defining shapes of different tetrominoes.
</p>

<h2>3. Block Class (<code>tetromino.py</code>)</h2>

<h3>3.1. Description</h3>
<p>
    The <code>Block</code> class represents individual blocks in the Tetris game. Each block is associated with a
    tetromino, has a position, and can undergo special effects when removed.
</p>

<h3>3.2. Methods</h3>
<ul>
    <li><code>sfx_end_time()</code>: Checks if the special effects cycle has ended.</li>
    <li><code>sfx_run()</code>: Executes special effects animation.</li>
    <li><code>is_alive()</code>: Manages block's state and handles removal animation.</li>
    <li><code>rotate(pivot_pos)</code>: Rotates the block around a specified pivot position.</li>
    <li><code>set_rect_pos()</code>: Sets the rectangle position based on the current or next position.</li>
    <li><code>update()</code>: Updates the block's state and position.</li>
</ul>

<h2>4. Tetromino Class (<code>tetromino.py</code>)</h2>

<h3>4.1. Description</h3>
<p>
    The <code>Tetromino</code> class represents the tetrominoes in the Tetris game. It includes methods for rotation,
    movement, updating, and collision detection.
</p>

<h3>4.2. Methods</h3>
<ul>
    <li><code>rotate()</code>: Rotates the tetromino.</li>
    <li><code>is_collide(block_positions)</code>: Checks if the tetromino collides with the game field.</li>
    <li><code>move(direction)</code>: Moves the tetromino in a specified direction.</li>
    <li><code>update()</code>: Updates the tetromino's state and position.</li>
</ul>

<h2>5. Text Class (<code>main.py</code>)</h2>

<h3>6.1. Description</h3>
<p>
    The <code>Tetris</code> class manages the overall game state, including the game field, tetrominoes, scoring, and
    game progression.
</p>

<h3>6.2. Methods</h3>
<ul>
    <li><code>get_score()</code>: Calculates and updates the player's score.</li>
    <li><code>check_full_lines()</code>: Checks for and clears full lines in the game field.</li>
    <li><code>put_tetromino_blocks_in_array()</code>: Places the tetromino's blocks in the game field array.</li>
    <li><code>get_field_array()</code>: Initializes an empty game field array.</li>
    <li><code>is_game_over()</code>: Checks if the game is over.</li>
    <li><code>check_tetromino_landing()</code>: Manages the landing of a tetromino on the game field.</li>
    <li><code>control(pressed_key)</code>: Handles user input for tetromino control.</li>
    <li><code>draw_grid()</code>: Draws the grid lines on the game field.</li>
    <li><code>update()</code>: Updates the game state, including tetromino movement and scoring.</li>
    <li><code>draw()</code>: Draws the game field and tetromino blocks.</li>
</ul>