Task 1 — Playing Cards (CSS)

Start from: styles.css and the supplied HTML.

Goal: Show two overlapping playing cards on a green felt table.

Required CSS changes

.table

background: linear-gradient from forestgreen → darkgreen.

.card

border-radius: 5px;

box-shadow: black, 3px x-offset, 3px y-offset (blur/spread optional if not specified).

Position the two cards absolutely inside their container:

.card-top: left: 150px; top: 100px;

.card-bottom: left: 240px; top: 120px;

Layering:

Apply z-index values so .card-top renders above .card-bottom.

Corner symbols on each card:

.top-left: absolute; left: 2px; top: 2px;

.bottom-right: absolute; right: 2px; bottom: 2px;



Task 2: Animating the answer

Required CSS changes

Define keyframes moveFraction:

0%: color: yellow; transform: translate(-355px, 60px);
(Fraction starts off the left side, slightly below the question.)

50%: transform: translate(0px, 60px);
(Moves under and to the right of the question.)

100%: color: red; transform: translate(0px, 0px);
(Ends next to the = sign.)

#answer rule:

animation-name: moveFraction;

animation-duration: 2s;

animation-delay: 1s;

animation-fill-mode: forwards; (keeps final position/color)

#question rule:

transition: transform 0.6s ease-in-out;

#question:hover rule:

transform: scale(0.9);
