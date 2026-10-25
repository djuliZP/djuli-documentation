# Input Time Units

The units Djuli expects the **raw time values** to be in, exactly as your instrument exports them.

Pick the unit that matches the timestamp column in the file (seconds, milliseconds, minutes…). Djuli will then convert internally to whatever you choose under [`OutputTime`](../OutputTime) for display. Setting this incorrectly is the most common cause of x-axis values that look off by 1000×.
