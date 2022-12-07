# Mulan and Mushu's Adventure!!
# Playable. lnik: https://gba.ninja/?autorun=https://ramyaramaswamy21.github.io/Media-Device-Architectures/Project.gba
## My Final Project!! [UPDATES FOR MILESTONE 4 ARE IN BRACKETS]

**IMPORTANT-[BEGINNERS HELP]**
        The first time you collide with Shan Yu, Shan Yu will give you a couple seconds to hit him before sending you back to Mulan's
        house. This is different because I wanted to help beginners learn how to kill Shan Yu and give them a head start for when
        they're first starting to learn the game. However, after the first time you collide with Shan Yu, it becomes harder and you get sent back
        the second you collide wiith Shan Yu. 
## What is finished about the game:

**[ALL SPRITES ARE DONE! YAY]**
        *Spritesheet:*
            1st row (top left for 3 down): Right states for Mushu
            2nd row (top second left for 3 down): Left states for Mushu
            3rd row (top third left for 3 down): Back states for Mushu
            4th row (top fourth left for 3 down): Front states for Mushu
            5th row (top fifth left for 4 down): Front, Right, Back, and Left states for Mushu catching crickets
            6th row (top sixth left for 4 down): Front, Right, Back, and Left states for Mushu fighting Shan Yu with Sword
            7th row (top seventh left for 3 down): Cricket states (3)
            8th row (top eigth left for 3 down): Evil Cricket states (3)
            1st row (bottom left for 3 down): Shan Yu states (3)
            All mini game characters!:
                2nd row (light blue for 3 down): Right states for Mulan (3)
                3rd row (light blue for 3 down): Left states for Mulan (3)
                4th row (small dark green 2x2): Rice bowl
                4th row (dark green for 3 down): Right states for Ling/ChienPo (3)
                5th row (dark green for 3 down): Left states for Ling/ChienPo (3)
                6th row (dark blue with light green): Mushu kill state when Shan Yu is dead
**[STATE MACHINE IS DONE! YAY]**
        *The state machine is done:*
            START: art and able to go to game with Start button and go to instructions with Select button
            INSTRUCTION: art and able to go back to start with Select button and to game with Start button
            PAUSE: art and able to go back to game with Start button and back to Start screen with Select button and back to minigame with Start button
            GAME: can go to Pause screen with Enter button and to Win screen by getting all crickets and killing shan yu and to Lose screen with time running out 
            or by colliding with Evil Cricket and then losing mini game
            MINIGAME: can go to Pause screen with Enter button and go to Lose screen by not winning the mini game, but if you win the mini game, then you get to
            start the game again
            WIN: art and can go back to Start screen with Start button
            LOSE: can go back to Start screen with Start button
**[ALL GAMEPLAY IS ALSO DONE! YAY]**
        *Gameplay:*
            Mushu can move using button controls (left, right, up, down)
            Mushu can activate MUSHUCATCH by clicking the A button near a cricket and is able to catch up to 3 crickets at a time
            Mushu can activate MUSHUSWORD by clicking the L button
            Shan Yu moves around the screen at random until Mushu has caught one cricket- when he has caught one cricket, Shan Yu starts chasing him
            Crickets move at random all over the screen
            Evil Cricket moves at random all over the screen and goes invisible every few seconds to confuse Mushu
            Every time Mushu collides with the Evil Cricket, Mushu immediatally dies, and you move to the lose screen
            Mushu can't collide with the center of the screen as that is Mulan's house
            All characters (Mushu (all states), crickets, Shan Yu, evil cricket) are animated and have different frames for walking/catching/fighting
**[MINIGAME GAMEPLAY IS DONE YAY!]**
        *MiniGame:*
            After colliding with evil cricket, you get a second chance to not lose the game by having a mini game where you're running away from rice
            that is falling from the sky and if you win that mini game, you can get back to the game and start from the beginning
            Use right and left buttons to move back and forth to escape the rice!
**[FIXED ALL BUGS :)]**
        
**[CHEAT IS DONE!]**
            Press Button B to activate the cheat and use a magnet to capture crickets faster and within closer distance!
            The cheat also uses the MUSHUCHEAT state and that helps the player know that they are currently using the cheat.                                                                                             
**[SOUNDS ARE DONE!]**
            Used looping sounds for each state (except pause since that pauses the music)
            Each state (Start, Instructions, Game, MiniGame, Win, Lose) all have different songs from the Mulan soundtrack!
**[CHANGING TILES AT RUNTIME IS DONE!]**
            After capturing a cricket, if Mushu collides with Shan Yu and gets sent back to Mulan's house, then a dirt tile appears at the front
            of Mulan's house (basically telling you that it will be harder to go back home as you keep colliding with Shan Yu since time
            will run out)
            This will happen repeatedly until it reaches 10 times of getting back to the house or time has run out and then you lose the
            game
            You will see the several dirt tiles add up in a row in the front of the house as you move along
**[CHANGING PALETTE AT RUNTIME IS DONE!]**
            As time goes on, the color of the river changes turning darker and bluer- telling Mushu to hurry up!! Basically another version
            of a timer that is embedded in the game background to make it more intuitive for the player
**[BACKGROUND REQUIREMENTS-PARALLAX]**
            The start state has a parallax background with cherry blossoms falling down (there are two backgrounds of cherry blossoms and 
            one is falling faster than the other)

## Things I've changed from Milestone 2:
        -If you collect all 10 crickets and then you also kill Shan Yu (hit him 3 times) all within the time limit, then you win the game! (way to win the game)
        -You don't have to hit shan yu 3 times to kill him- you just need to hold down the button L for a certain number of seconds and collide with him and then have one cricket captured
        -I wanted to introduce a kill state for Mushu when Shan Yu dies to differentiate when he goes back to the center after killing him
        vs. when he goes back to the center after Shan Yu killing him (the other way around) and Mushu having to start over
    
## Win/Lose:
        -Win by killing Shan Yu when clicking the sword button and catching all crickets
        -Lose by colliding with evil cricket and then losing the mini game by colliding with rice falling down
        -Shan Yu can send you back to the beginning of your cricket count to 0 constantly if you keep colliding with him without
        killing him
