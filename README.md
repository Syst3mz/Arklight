# Characters
A character is a players avatar in the game. Characters are comprised by:
* A bag of tokens $T$
* A number of action points $AP$
* A number of shield points $S$
* a number of strain points $R$
* a set of gear $G$
* a level $L$


## Action Points
Action points represent the ability of characters to act in the world. If a player's AP ever reaches zero they are considered *incapacitated*, and can no longer activate, nor participate in challenges. Players may be brought back from being incapacitated by raising their $AP$ to be half of that players starting $AP$ total.


## Shield
Each player has a shield, they may describe it as they wish (brownie points for giving explanations related to tokens). A players shield may be regenerated while on a mission, a players action points cannot.
## Strain
Players may *strain* themselves to change the results of a draw. See [[#Straining]] for more detail.
# Tokens
A token is the a $(H, L)$ where $H$ is either a college of technology or a school of magic, and $L$ a level from $[1,4]$.
Each player has bag of tokens. This defines their character's abilities.


## Magic

| School        | Description                                            |
| ------------- | ------------------------------------------------------ |
| Beasts        | Control of animals                                     |
| Conjuring     | Making something out of nothing                        |
| Transmutation | This for that                                          |
| Illusion      | ...Now you see me                                      |
| Flow          | Control of the world around you (think avatar bending) | 

## Technology

| College     | Description                                |
| ----------- | ------------------------------------------ |
| Netrunning  | Manipulation of the digital                |
| Mechcraft   | Construction of mechanical devices         |
| Energetics  | Control of the flow of electricidal energy |
| Cybernetics | Fusing the biological and technical        |
| Explosives  | For when it do go down                     |

# Challenge
A challenge is any time the characters face an obstacle, requests one, or frequently in combat. Challenge all have a timer and a rating. The timer is most often 1, but can be larger. If the timer reaches zero before the rating is reached the people doing the challenge fail.

Multiply the challenge by the number of characters and number of rounds to hold the difficulties stable.

| Rating | Difficulty            |
| ------ | --------------------- |
| 1      | Normal                |
| 2      | Difficult             |
| 3      | Challenging           |
| 4      | Extremely Challenging |


To execute a challenge the challenged player or players each draw 2 tokens from $T$. If they are both the same token, they act as a token of 1 higher level. Players *must* explain how they use their drawn tokens to resolve the challenge. So long as the value $\sum\textrm{Drawn Tokens}.L\geq\textrm{Rating}$ the challenged succeeds.

Whenever players draw tokens they loose AP equal to the number of tokens drawn.

## Straining
Players may strain up to $L$. When a player strains, they may draw an additional token. They may now use any two of the drawn tokens in the challenge. 

### Dealing with Strain
When player has strain, they subtract their strain from their $AP$ at the start of their activation, and after every challenge any player initiates (or causes to be initiated in cases such as traps). 

### Soothing Strain
Players strain is removed at the start of any mission, during anytime players would be able to relax for sufficient time, or if another player takes the soothe action while in combat.

# Gear
Gear is all equitable items that a player may have. Players should work with their game master to make gear that is meaningful to them.
// todo: impl the rest of this

# Combat
Combat is broken into rounds. Each character and enemy gets one activation per round. Players must choose an order to go in at the start of a round. Players may make a challenge(1,1) to have the first activation. Otherwise, enemies activate first. Players and Enemies alternate activations until all entities have acted.

Combat occurs at 3 ranges: Adjacent, Near, Far. Characters may change ranges by 1 on their activation by using the "Change Range" action.

Players may preform 1 assumed action and 1 complex action or 2 assumed actions. 

## Assumed actions:
Change Range
Use a consumable
Delay their activation until after a designated friendly

## Complex Actions
Actions that require more thought that walking, eating, or waiting!

### Making a Challenge / Attacking an Enemy
Attacking an enemy is a Challenge. Other challenges may be used if a player want to (such as destroying parts of the environment). Enemies are dealt damage equal to $\sum\textrm{Drawn Tokens}.L+1$ distributed into as many instances of damage as makes sense.

### Taking Cover
A character taking cover may make a challenge to make cover, or if cover is apparent may take cover by forgoing any further actions this activation.

Being in cover grants you increased defenses. Reduce each incoming instance of damage by 2.

### Regenerate Shield
A character may regenerate their shield by making a challenge. They recover $2\sum\textrm{Drawn Tokens}.L$ up to their maximum shield.

### Soothe
Provided the target is in cover, a friendly in adjacency can use their activation to soothe the target. You remove $L$ strain from your target

## Taking Damage 
Players take damage in *instances*. An instance of damage is the full damaged invoked by one source of damage. A single instance of damage might be multiple points of damage.

Players first remove shield, then subtract the remaining points of damage from their $AP$.
