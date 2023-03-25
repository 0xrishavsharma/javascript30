# JS30, Day 2 - JS and CSS Clock

Encountered a bug, where the hands will rotate anti-clockwise when the current second reached to 0. The glitch happens because the clock hand rotates through a full circle of 360 degrees to return to the 0th second position. Because 0 and 360 degrees are in the exact same place, any transition effect applied to the clock hand can interpret the return from 360 to 0 degrees as a backward transition, rather than a forward transition.

The transition effect will follow the shortest path to the new position, and since the 0th second position is in the same place as the 360th second position, the shortest path is to spin the clock hand backwards from 0 to 360 degrees before transitioning to the new second position. This rapid spinning creates the visual glitch that we want to avoid.

By disabling the transition effect at the 0th second position and then re-enabling it at the 1st second position, we can avoid the backward transition and ensure that the clock hand always moves forward to the new second position over the course of one second.
