# CURVE_TRACER_USB-C
Curve tracer powered by +5V USB from the oscilloscope under use. 

![Picture](img_curveTracer_revA0.png)

Most curve tracer designs require using a transformer connected to line voltage. While simple, this setup is bulky, using components that are not readily available (at least not for me). This design is powered by the USB connection present on modern oscilloscopes, aiming for convenience at the cost of complexity. Additionally, most components are cheap and easily sourced. 

# Design

The waveforming portion of the design was inspired by a forum post: https://www.mikrocontroller.net/topic/528893

As explained in the post, the design uses op-amps to generate a 1KHz sinewave. This sinewave is put across the DUT, connected in using the banana jacks. The resulting sinewave is then sent to an oscilloscope configured to X-Y mode, with J3 connected to the X channel and J4 connected to the Y channel. Different components produce different waveforms, providing information on how the components looks in the circuit, helpful in troubleshooting potential failures. 
