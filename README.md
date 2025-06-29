WACROP (Waveform And CROssbar Programmer) is an educational and research-oriented tool designed to create, visualize, and export custom electrical pulse waveforms (see Section A) and 1T1R crossbar programming schemes (see Section B). It is ideal for researchers working on memristive arrays, neuromorphic circuits, or pulse-driven hardware, offering intuitive design and automated export in multiple formats.

===== HELP & INSTRUCTIONS =====

A.1 SETUP THE WAVEFORM EDITOR TAB:
   - Total Time & Time Step: Define time grid resolution.
   - Base Voltage: Voltage value when no waveform segment is active.

A.2 BUILD CUSTOM WAVEFORMS:
   ➤ Add Segment: Create waveform sections using 5 types:
       • Square .......... constant value in a time window
       • Ramp ............ centered triangle wave
       • Sinusoid ........ burst of sine wave (user-defined freq/phase)
       • Inverted ........ forcibly sets to 0 V in a time range
       • Gaussian ........ smooth Gaussian pulse

   ➤ Edit or delete segments from the waveform table.
   ➤ Ready-to-use Templates:
       • Pulse Train ............. periodic square pulses
       • Ramp Sweep .............. linear ramp over full time
       • Sinusoid Burst .......... sine wave in a specific window
       • Poisson Spikes .......... randomly timed spikes
       • Poisson Bursts .......... random bursts of spikes
       • Random Amplitude Spikes . spikes with variable strength

A.3 EXPORT & SAVE:
   - Save the waveform preview as a (.png) image.
   - Export waveform as (.csv) or as (.txt) file (the latter is compatible for usage in Cadence® Virtuoso® VPWLF instance).
   - Save your custom waveform as a template (.mat).

B.1 1T1R CROSSBAR WRITER TAB:
   - Set crossbar size (NxN) and writing voltage values on the lookup table for each cell.
   - Random Fill: Fills table using quantized voltage range and step.
   - Rename Rows/Cols: Change default R1, R2, C1... naming.
   - Reset Table: Clear to 0 and restore default labels.
   - Save Crossbar: Export voltage preview as a (.png) image.
   - Import/Paste Crossbar voltages from file or clipboard.

   ➤ Waveform Settings:
     - Total Duration, Time Step, Pulse Width, Spacing define the timing parameters of the control and writing waveforms.
     - Start Delay: delays all pulses (rows & columns) by the given time offset.
     - Writing Waveform applies to rows only (Step, Ramp, Half-Sine).
     - Column pulses are always square pulses and identical in amplitude (specified by Column Min/Max Voltage parameters).

B.2 PREVIEW PULSES FUNCTION:
   - Select rows to preview.
   - Visualize row pulses, heatmap over time, and generic column activation.
   - You can save the plots you want in a (.png) image.
   - Ramp is centered. Column pulses are always square, scaled between Min/Max.

B.3 EXPORT TO AN ARCHIVE (.zip):
   - Export mode: All / Rows / Columns. A (.zip) file is generated with the appropriate sub-folders. Its filename includes a timestamp for version tracking.
   - File format: You can choose among (.txt), (.csv), or (.mat).
   - Generates ROW_#, COL_#, and log.txt files.
   - Log file includes waveform metadata and also details about the crossbar's calculated write energies.

🧠 TIPS:
   • The "Reset App" button closes all the open plots or dialogs. It also resets the waveform editor, table data, labels, and options.
   • All parameters are expressed in SI units and can be entered using scientific notation. For example, to specify 1 nanosecond, you can type 1e-9.
   • Use "Preview Pulses" before exporting for validation.
   • Column control mode is time-multiplexed. Each column is active only briefly.
   • Zoom and inspect plots for waveform accuracy.
   • Use the Delay on the 1T1R tab to align control and writing pulses with other external signals.

📊 Example qualitative shapes for the waveform generation sub-tool (see the images at the bottom).

===== LICENSE & ATTRIBUTION =====
📘 This software is intended for research and educational use only. Please contact the author for permission if you wish to redistribute or modify it.

WACROP - Version 1.0.3  |  © 2025  All rights reserved.
Created by: Ioannis K. Chatzipaschalis - Ph.D. Student
Contact E-mail: ioannis.chatzipaschalis@upc.edu
