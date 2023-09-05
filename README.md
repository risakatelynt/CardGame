# Tactical Card Game

Welcome to the Tactical Card Game project! This project is aimed at creating an online card game that combines card-game mechanics with a chess-like board. It is created using Java that manages and progresses the game as players take actions in a web browser. The final product will enable a human player to complete a game against a (semi-)intelligent AI opponent.

<img width="884" alt="game1" src="https://github.com/risakatelynt/GameTeamProject/assets/124533180/f41009d5-4f51-48fd-89c1-23885cf02b42">
<img width="833" alt="game2" src="https://github.com/risakatelynt/GameTeamProject/assets/124533180/15e31bff-7789-4898-b4ac-2a58afb9bcaf">

## Game Rules

### Counter-Attacking

- When a unit attacks, it reduces the health of the unit it attacked by its 'attack value'.
- If the unit that was attacked still has greater than 0 health, it counterattacks.
- The counterattack reduces the health of the original attacker by the counterattacker's 'attack value'.
- Counterattacks are not recursive, meaning they do not trigger further counterattacks.
- A unit can only counterattack once per player turn.

### Running Out of Cards

- If you attempt to draw a card and have no cards remaining in your deck, you lose the game.

### Hand Size

- The maximum hand size is 6 cards.
- When you draw a card, it is inserted into your hand. You may choose to sort your hand, but this is not required.
- Drawing a card happens at the end of your turn when you press the "end-turn" button.
- If you draw a card and your hand is full (6 cards), you must discard (lose) the newly drawn card.

### Unit Actions in a Turn

- If a unit has just been summoned, it cannot take any actions during that turn.
- If a unit started the turn on the board, it has an available 'attack action' and an available 'move action' that it can spend before the end of the turn.
- A unit can spend its move action, followed by its attack action (either as a single move-then-attack or as separate actions).
- If a unit attacks and has not moved, it loses its move action for that turn.
- A unit that can attack twice has two attack actions in a turn rather than one.

### Multiple Units in a Turn

- Multiple units can act during a player's turn.

## Installation and Running

To run the Tactical Card Game code, follow these steps:

1. Clone the repository using Git:
   ```
   git clone https://github.com/risakatelynt/GameTeamProject.git
   ```

2. Navigate to the project directory:
   ```
   cd CardGame
   ```

3. Compile the code using SBT (Simple Build Tool):
   ```
   sbt compile
   ```

4. Run the game using SBT:
   ```
   sbt run
   ```

This will start the game server, and you can access it via a web browser by navigating to the URL `http://localhost:9000/game`.

Enjoy playing the Tactical Card Game, and may your strategic and tactical skills lead you to victory!
