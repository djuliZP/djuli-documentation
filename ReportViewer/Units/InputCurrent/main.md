# Input Current Units

The units Djuli expects the **raw current values** to be in, exactly as your instrument exports them (A, mA, µA, nA, pA).

Pick the unit that matches the current column in the file. Djuli will then convert internally to whatever you choose under [`OutputCurrent`](../OutputCurrent) for display. Setting this incorrectly is a common cause of y-axis values that look off by a factor of 10³ or 10⁶.
