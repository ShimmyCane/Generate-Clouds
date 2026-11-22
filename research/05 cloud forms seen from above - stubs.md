# Cloud forms seen from above: stubs

Research stubs for Generate Clouds, 2026-11-22. Each entry says what the form is and what would need to be learned before anyone designs for it. None of these is built, and none is in the current model. They are a to-do list, not a design.

Rule for later: anything that is not in the measured data (contrails, hole-punch holes made by aircraft, anything drawn as a sample) is labelled "Made-up" or "human-made" in the reading panel, as the tornado and waterspout rule already requires.

## Forms seen from a plane

### Cloud streets (rolls)
- **Looks like:** long parallel lines of cumulus, aligned with the wind, in cold air blowing over warmer sea or land.
- **Mechanism:** convective rolls, a lift and sink pattern in the boundary layer.
- **To learn:** the typical spacing and alignment; how the wind direction at the cloud base sets the roll direction.
- **Would need:** the wind at a few heights (already in the wind grid), and a roll-aligned pattern in the low layer.

### Sea of cloud (cloud deck from above)
- **Looks like:** a flat, bright, wrinkled top covering everything below, with the ground hidden.
- **Mechanism:** a stratus or stratocumulus deck, often at an inversion, or a fog layer lifted off the ground.
- **To learn:** how the deck top height varies, and what makes the surface below visible through gaps.
- **Would need:** a deck layer that can cover the whole view from above.

### Lenticular (lee-wave) clouds
- **Looks like:** smooth, stacked lens shapes, often still over a mountain ridge while the wind blows through them.
- **Mechanism:** air crosses a ridge and ripples downwind; the cloud forms at the crests of the waves.
- **To learn:** the wave length from the wind speed and the stability; why the cloud stays still.
- **Would need:** a stationary wave pattern tied to the terrain height map (`js/terrain.js`).

### Wave clouds and Kelvin-Helmholtz billows
- **Looks like:** regular rows of curls or ripples in a cloud layer, like waves on a sea.
- **Mechanism:** shear between two layers of air moving at different speeds.
- **To learn:** the shear needed, the typical spacing, and how long the pattern lasts.
- **Would need:** the wind at two close heights; currently the wind grid is three heights only.

### Roll cloud (shelf cloud along a gust front)
- **Looks like:** a horizontal roll of cloud along the front edge of a storm.
- **Mechanism:** cold outflow from a thunderstorm lifts the warm air ahead of it.
- **To learn:** the link to a storm (a made-up or a measured storm only), and its typical size.
- **Would need:** the storm feature system, which is still a note (`todo.md`, storm structure).

### Mammatus
- **Looks like:** pouches or bubbles hanging under the base of a cumulonimbus anvil.
- **Mechanism:** sinking air cooled by evaporation under the anvil.
- **To learn:** when they form, how long they last, typical size.
- **Would need:** a shape under the anvil, in the cloud shader; the anvil shape is not yet in the model.

### Overshooting tops and cloud-top texture
- **Looks like:** domes or turrets rising above the flat anvil; a cauliflower top from above.
- **Mechanism:** strong updraft pushes above the level of the surrounding cloud top.
- **To learn:** the height above the anvil, and how it is seen from a plane.
- **Would need:** a top height above the layer, in the cumulonimbus profile.

### Pileus (cap cloud) over a cumulus
- **Looks like:** a smooth, thin cap sitting on top of a growing cumulus.
- **Mechanism:** a rising bubble cools as it pushes into the air above and condenses there.
- **To learn:** the conditions that make it, and how short-lived it is.

### Cloud holes and cloud pockets
- **Looks like:** gaps in a sheet of cloud, sometimes with a ring of cloud around, sometimes a clean round hole.
- **Mechanism:** a clear patch where cloud evaporates or freezes, or a broken field of cumulus showing sea between the clouds.
- **To learn:** the natural cause (broken cumulus, sinking air) versus the aircraft-caused hole-punch.
- **Label:** aircraft-caused holes are **human-made** and must say so.

### Contrails and contrail-cirrus
- **Looks like:** straight white lines from aircraft; in the sky above, spreading sheets of thin cloud.
- **Mechanism:** hot exhaust mixes with cold air and freezes into ice crystals.
- **Label:** **human-made**. Not in the weather data; not to be drawn as weather.
- **To learn:** only if the app ever shows them at all, which is a question for Jimmy.

### Cloud shadows on the ground or sea, seen from above
- **Looks like:** dark patches moving across the land or water below the cloud deck.
- **Mechanism:** the cloud blocks the sun.
- **To learn:** the cloud shadow position from the sun angle and the cloud height.
- **Would need:** the cloud shadow on the ground, already in the list of next candidates (`todo.md`).

### Valley fog and inversion pools
- **Looks like:** flat white fog filling valleys below the ridges, with the peaks sticking out.
- **Mechanism:** cold air sinks into the low ground at night and forms fog; an inversion keeps it there.
- **To learn:** the inversion height and how long the fog stays after sunrise.
- **Would need:** a fog layer tied to the height map.

### Optical effects from above (halo, glory, rainbow, Brocken spectre)
- **Looks like:** coloured rings around the plane's shadow on the cloud top (a glory), or rainbow arcs.
- **Mechanism:** light scattered by water droplets of a particular size, seen from the right angle with the sun behind.
- **To learn:** the geometry from the sun and the view angle; the rainbow is a planned next candidate in `todo.md`.

## What to check first (for later)

1. Which of these are common enough to matter for the app's sky (cloud streets and the sea of cloud, probably).
2. Whether the wind grid needs more heights for shear-driven forms.
3. Whether any human-made form (contrails) should appear at all.

## Sources to read before designing

- WMO International Cloud Atlas (already linked from note 01).
- Any pilot or aviation reference on cloud forms seen from above.
- The Met Office and NOAA cloud guides for cloud streets and lenticular clouds.
