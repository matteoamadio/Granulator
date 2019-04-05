# Granulator
I developed this patch after the idea of having an easily controlled granulator which allows to create a continuous but dynamic flow of sound that could be used for example as an instrument in live sampling performances.

Every grain has size and frequency randomly choosen in the range [central-deviation; central+deviation] and its amplitude is modulated by a window.

Both frequency and size have a "Max deviation" mode, which cause the deviation to be set to the maximum value allowed (dev = central * 0.99) at every change of the central value.

Every grain parameter is used to modulate a sample randomly chosen from the loaded buffer, but it's also sent to a sine, triangular or square wave oscillator.

The resulting grain is then a mix between the sample and the oscillator output.

The number of voices can be set from 1 up to 50, and they are automatically spatialized with a given ramp time over 2 o 4 channels, basing on the choice of the performer.

extract1.wav, fm_samples3.aif and fm_samples5.aif are three audio files that can be used to try the patch immediately, fm_samples3.aif is loaded on startup.
