# Conversion Factor

Manual multiplicative factor applied when converting from the input unit to the output unit.

Djuli already knows how to convert between standard SI prefixes; use this field only when the conversion needs a value the platform can't infer — for example, an instrument-specific scaling, a calibration coefficient, or a unit Djuli doesn't ship with.

The conversion is `output = factor × input + offset` (see [`ConvertionOffset`](../ConvertionOffset)).
