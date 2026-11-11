# _battery — Battery Days

Battery percentage shown as days remaining ("5.3 days"), with
one big battery outline behind the percentage. The prediction
learns the watch's real drain rate silently from samples taken
each time the app is opened. After sunset the face inverts to
white on black. Current version: 2.8.34. 2.8.34 removes the corner marks from _battery (user): the corner layer is gone, so the app draws no earmarks. The shared helper stays in family.h (kept). 2.8.33 makes the exit an instant cut — no slide animation at all (window_stack_pop(false)), so there is nothing for the marks to flash against while sliding. 2.8.32 moves the corner marks to their own topmost layer and hides it before the exit pop, so the frame that slides off has no marks (the watchface's own marks are then the only ones in the corners). The idle exit hides them too, through a new family pre-pop hook. 2.8.31 stops the wobble before the exit pop, so nothing redraws mid-pop (the exit-glitch fix, same as _weather 2.7.35). 2.8.30. 2.8.28 added the family button
slide; 2.8.29 removes it from all buttons (no activation viz here) and
2.8.30 removes the half-circle center mark added in 2.8.29 as well:
Select toggles the readout between days and % (session-only;
reopening returns to auto), Up exits instantly, Down is unsubscribed.
