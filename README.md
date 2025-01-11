# VHDL Counter Range Bug

This repository demonstrates a potential range error in a simple VHDL counter. The `count` signal has a specified range, but this range might be inappropriate if the counter is expected to reach a higher value.  This can lead to unexpected behavior, potentially including silent overflow.

**Bug Description:** The `internal_count` signal and the output `count` are declared with a range of 0 to 15. If the counter is intended to run for more than 15 cycles, an overflow will occur.  The code does not handle this case gracefully, resulting in unpredictable behavior.

**Solution:** Expand the `INTEGER` range to accommodate the desired upper limit or add an overflow check.
