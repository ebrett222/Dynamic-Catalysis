"Parameter_Sweep" is a big, bulky code that is a little difficult to navigate at first.

However, it lets us iterate up to 4 (can easily be made for any number) parameters between runs in any order we want. We can also choose to vary dG or V with time (but not both at once).

Every time the code is run, the solver is fed a combination of the parameters you have given the code at the beginning. It runs through every possible combination of those parameters.
The "modes" can be turned on or off in the "Switchboard" section (1=on). Each mode has "subsettings" that can be turned on if the mode is active (mostly printing out plots)
What happens after the solver runs depends on what "modes" are active (most of the time it's just printing plots):
  - "Normal Mode":   prints out basic plots we're used to: coverage vs time, current vs voltage, voltage vs time, etc.
  - "Pass/Fail Mode":   as the solver runs, it (or Python itself) may encounter issues. Depending on what issues arrise, this creates color-coded "pass/fail" plots: the two
                        most-frequently-varied parameters are iterated through all their combinations, then colored markers tell us what combinations of parameters gave
                        parameters gave us what issues
  - "Static Volcano Mode":    plots static volcano stuff, of course. Has the option to make "dG(max) vs (parameter)" plots, lettng us see how static volcano peaks change
                              with that parameter
  - "Dynamic Volcano Mode":   makes dynamic volcano plots and does your laundrey if you ask nicely

