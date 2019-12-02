<h1>User Guide</h1>

Inspired by the humanized and offbeat sounds of Hip-Hop and IDM productions, JayMeter is a 16-step timing and dynamics sequencer for Ableton Live with Max 4 Live. It is a MIDI effect which does not produce MIDI notes on its own. Rather MIDI notes need to be fed from either Ableton's sequencer or external MIDI fed through Ableton. JayMeter then transforms the timing and velocity (dynamics) of the MIDI notes, pushing the results out through the other end of the MIDI effect slot.

<h2>Requirements</h2>
  <ul>Ableton Live 9</ul>
  <ul>Max 4 Live 7</ul>

<h2>Usage</h2>

Add the file [JayMeter-Definitive.amxd](/devices/JayMeter-Definitive.amxd) to your favorite Max 4 Live MIDI effects path.<br>
Drag & drop the patch into an available MIDI channel with or without an existing plugin instrument.<br>
By default, the device is enabled but does not produce a noticable effect on incoming MIDI.<br>
Modify the behavior of the incoming MIDI by changing the value dials as follows.<br>

<h2>Parameter Guide</h2>

<h3>Timing (MIDI Delay)</h3>

<h4>Step Sequencer</h4>
<img src="/img/timing-07-seq.png" alt="Step Sequencer">
16-step sequencer which pushes or pulls the offset by a % of 1 full beat.

<h4>Offset</h4>
<img src="/img/timing-01-offset.png" alt="Offset">
Global offset of the offset as a positive or negative percentage of 1 beat.

<h4>Strength</h4>
<img src="/img/timing-02-strength.png" alt="Strength">
Strength percentage of offset steps. 1.00 is full strength.

<h4>Random</h4>
<img src="/img/timing-03-random.png" alt="Random">
Percentage width of random postive and negative offsets. The closer to 1, the greater the possible randomness up to +/- 1 full beat.

<h4>Multiplier</h4>
<img src="/img/timing-04-multiplier.png" alt="Multiplier">
A final pass multiplier to current offset values. This is different from strength as it is applied globally rather than the step sequencer only and is a whole integer multiplier rather than a percentile from 0.0-1.0.

<h4>Sequencer Speed</h4>
<img src="/img/timing-05-s_speed.png" alt="Sequencer Speed">
How fast the sequencer moves between steps. 1 is one beat per step. Moving to the left from the center increases the speed to sub-step divisions. Moving to the right from the center slows the seqence down to multiples of beats per step.

<h4>Enabled</h4>
<img src="/img/timing-06-enabled.png" alt="Enabled">
Bypasses the timing effect.

<h3>Dynamics (MIDI Velocity)</h3>

<h4>Step Sequencer</h4>
<img src="/img/dynamics-07-seq.png" alt="Step Sequencer">
16-step sequencer which increases or decreases a given velocity value by the number indicated in the step value.

<h4>Offset</h4>
<img src="/img/dynamics-01-offset.png" alt="Offset">
Globla offset of the velocity as a positive or negative whole number.

<h4>Width</h4>
<img src="/img/dynamics-02-width.png" alt="Width">
Width of step sequencer offset as a percentage.

<h4>Random</h4>
<img src="/img/dynamics-03-random.png" alt="Random">
Percentage width of random postive and negative velocity adjustments. The closer to 1, the greater the possible randomness up to +/- 127.

<h4>Curve</h4>
<img src="/img/dynamics-04-curve.png" alt="Curve">
Velocity curve applied as a final pass to the MIDI velocity. Center of 0.00 is a straight even distribution with right expanding the velocity curve and right compressing it. Use subtly to handle velocity offsets which would clip at 127 or hover at low values.

<h4>Sequencer Speed</h4>
<img src="/img/dynamics-05-s_speed.png" alt="Sequencer Speed">
How fast the sequencer moves between steps. 1 is one beat per step. Moving to the left from the center increases the speed to sub-step divisions. Moving to the right from the center slows the seqence down to multiples of beats per step.

<h4>Enabled</h4>
<img src="/img/dynamics-06-enabled.png" alt="Enabled">
Bypasses the dynamics effect.

<h2>Tips, Tricks, Notes, & Recommendations</h2>
  <ul>JayMeter is capable of extreme settings, please be aware of this with initial usage. Start with small changes.</ul>
  <ul>Start with constructed Ableton sequences rather than played-through external MIDI to debug settings.</ul>
  <ul>Unlike similar MIDI effects, JayMeter interpolates timing and dynamics between steps in a sequence. This gives the effect a more fluid flow for dense sub-step sequences.</ul>
  <ul>Timing module handles the concept of push offset in the step sequencer as combination of negative step sequencer values combined with positive global offsets. The result is that all MIDI note events are delayed, however some are delayed less than others, creating the effect of a human pulling the beat or note forward.</ul>
  <ul>Timing module is best applied after recording a sequence or through the use of another MIDI sequencer. Live playback with unpredictable MIDI delays may produce unintended results</ul>
  <ul>MIDI delay (timing) values are clipped to 0.00 for negative values for obvious reasons that time travel has yet to be invented.</ul>
  <ul>Likewise the MIDI standard limits values of velocity (dynamics) to 0-127 and will be clipped to that range.</ul>
  <ul>Timing module effects both the note on and note off MIDI events.</ul>
  <ul>Max/MSP handles note off as Velocity of 0. Please keep this in mind when using the dynamics module.</ul>
  
