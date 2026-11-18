# Ideas for later

English | [简体中文](todo.zh-CN.md)

Not built and not scheduled.

## Extensions: what was concluded

- There is no universal extension interface. Cameras, robot arms, drones, small computers and
  custom PCBs each use their own mounting conventions, so each extension gets its own printed
  adapter, designed when the accessory is chosen.
- Where things go: mounting (robot arm, drone, other fixtures) on the back of the case; standing
  on a desk or the ground on the floor of the case; sensors, a host computer and PCBs on the top
  or a side, or on the back only if they are very small and thin.
- The floor already carries an interface: four sealed M3 nuts on a 100 × 36 mm rectangle with the
  1/4"-20 tripod nut at its centre. The desk foot uses it.

## Outer package that doubles as a mount

For v3.2, especially when it holds the radar board alone (no DCA1000).

- A printed outer package with grooves cut in its sides.
- To carry: the case goes inside the package.
- To use: take the case out and plug it onto the package, which then holds it in place.

Open points for when it is built:

- whether the case needs rails (a new body), or a slide plate on the four floor nuts in place of
  the desk foot is enough;
- the grooves must not cover the cable openings in the side walls or sit in front of the antenna.
  With the radar board alone the cables are 12 V (radar J12) and USB (radar J8), both through the
  right wall; with the DCA1000 also 5 V (DCA1000 J2) and micro USB (radar J10) through the left
  wall, and Ethernet (DCA1000 J6) through the right wall;
- without the DCA1000 the spacers seat on the post tops, about 1.6 mm (the DCA1000's thickness)
  further back than designed, but the radar board cannot follow them: the round pillar under its
  upper right corner (top 38.0 mm above the back face, 1.0 mm behind the board as designed) holds
  that corner about 0.6 mm off the spacers, and tightening the three screws would bend the board.
  Three printed 1.6 mm shims under the spacers restore the designed height and keep the right-wall
  openings for J12 and J8 lined up (worked out from the geometry, not test-fitted);
- how it locks (one option: the v3.2 knob screwed into a sealed nut).
