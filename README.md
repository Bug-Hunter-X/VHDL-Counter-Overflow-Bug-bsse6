# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL: counter overflow. The provided code implements a simple counter; however, it lacks a check to prevent the counter from exceeding its defined range. This can lead to unexpected behavior or simulation errors.

## Bug Description

The `counter.vhdl` file contains a VHDL counter that increments on each rising clock edge.  The counter is designed to count from 0 to 15, but it does not handle the case when the counter reaches its maximum value (15).  When the counter reaches 15, it will increment to 16, causing an overflow and potentially leading to unpredictable behavior.

## Solution

The `counter_fixed.vhdl` file shows the corrected code. This version includes a check to prevent the counter from exceeding the maximum value.  When the counter reaches 15, it will reset to 0 on the next clock cycle.