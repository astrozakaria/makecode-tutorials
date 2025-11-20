# Bubble Stacking Tutorial

## Step 1: Create a New Project
Let's begin by setting up your game environment.

1. Click **New Project** in MakeCode Arcade.  
2. Name your project **Bubble Stacking**.  
3. Open the empty workspace.

---

## Step 2: Create the Game Board
Let's set the scene by adding the "core memories" board to the game window.

1. Open the **Bubble** category in the toolbox.  
2. Drag the **create board** block.  
3. Snap it **inside the `on start` block** already in the workspace.

---

## Step 3: Add a Player Bubble
Now let's add the main bubble the player will control.

1. Open the **Sprites** category.  
2. Drag **set mySprite to sprite of kind Player**.  
3. Choose an image for the bubble.  
4. Place it *below* the `create board` block.

---

## Step 4: Enable Player Movement
Allow the player to move the bubble around.

1. From the **Controller** category, drag **move mySprite with buttons**.  
2. Add it under the player sprite block.

---

## Step 5: Add Falling Bubbles
Let's add bubbles falling from the top of the screen.

1. Open **Loops** and drag **every 500 ms**.  
2. Inside this loop:
   - Go to **Sprites**
   - Drag **set sprite to sprite of kind Enemy**
   - Place it inside the timer loop
3. In the same block, add:
   - **set enemy x to pick random 0 to 160**
   - **set enemy vy to 50**

---

## Step 6: Detect Collisions
Let's detect when the player touches a falling bubble.

1. Open **Sprites → Overlaps**.  
2. Drag **on sprite of kind Player overlaps otherSprite of kind Enemy**.  
3. Inside, add:
   - **destroy otherSprite**
   - **change score by 1**

---

## Step 7: Game Over Condition
When too many bubbles fall, the game should end.

1. Add a variable named **misses**.  
2. Increase it whenever an enemy reaches the bottom.  
3. Inside an **if** block:  
   - If misses > 3 → **game over lose**

---

## Step 8: Finish!
Great job! You now have a bubble stacking game with:

- A board
- A controllable bubble
- Falling enemies
- Score detection
- Game over logic

Click **Download** to play it on your device!
