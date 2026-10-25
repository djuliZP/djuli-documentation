# Conversion Offset

Manual additive offset applied when converting from the input unit to the output unit.

Used together with [`ConvertionFactor`](../ConvertionFactor) to apply the full transformation `output = factor × input + offset`. Leave at zero for a pure rescaling.

Typical use case: a sensor that ships data offset by a known baseline (e.g. potential reported relative to a different reference electrode) — set the offset here to translate every reading into the desired reference frame without modifying the raw file.
