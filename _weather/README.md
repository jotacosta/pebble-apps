# _weather — MinMax Weather

Weather only: today's minimum and maximum temperature — the
raw temperature pair (a feels-like trial in
2.7.8 was reverted in 2.7.13 — it read too low) — as a big
two-line ladder, the precipitation chance at the top, and a
hand-drawn condition icon at the bottom. Data from Open-Meteo
via the phone's location; no API key. After sunset the face
inverts to white on black. The temperatures lean 5 degrees
anticlockwise, Lean-style. Current version: 2.7.38. 2.7.38 removes the corner marks from _weather (user): the app no longer draws the earmarks. The button slide on Select is untouched, and the exit is still the instant cut from 2.7.37. 2.7.37 makes the exit an instant cut — no slide animation at all (window_stack_pop(false)), so there is nothing for the marks to flash against while sliding. 2.7.36 hides the corner marks before the exit pop (the QT layer is hidden, so the frame that slides off has no marks — the watchface's own marks are then the only ones in the corners). The idle exit hides them too, through a new family pre-pop hook. 2.7.35 freezes the display before the exit pop — the wobble, the fetch animation and the slide all stop first, so nothing redraws mid-pop (the exit-glitch fix). 2.7.34 speeds the button slide to 250 ms (was 350). 2.7.33 evens the slide flares: top flare 30 px to match the bottom (edge height 116 px on emery). 2.7.32 makes the slide shallower (nose depth 4..7 px) and the bottom flare longer (30 px, top stays 10). 2.7.31 also randomizes the nose peak's vertical position (-6..+6 px off the button row's center) with every press. 2.7.27 added the
family button slide; 2.7.28 narrows it to the center button only
(activation viz only when staying in the app): Up exits instantly
again, Down is unsubscribed.
