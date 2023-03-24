# JS30, Day 2 - JS and CSS Clock

Encountered a bug, where the hands will rotate anti-clockwise when the current second reached to 0. This was happening because the transition that we have added is applied to every degree movement of the hand so when there is a sudden change in the degrees from 0 to 360. The transition is applied to this change as well so visually it appears that the hand is moving in backwards direction from
