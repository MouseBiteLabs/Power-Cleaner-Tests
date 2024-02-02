# Power Cleaner Tests

This repository is a compilation of recordings of the Game Boy Advance (AGB) audio output, before and after adding various capacitors provided by "Power Cleaner" mods. There has been a lot of discussion about what these mods achieve, but I haven't seen any actual empirical evidence. I've been looking at the AGB more recently, so I figured I'd do a deeper dive into the topic and provide some recordings so people can hear the differences for themselves.

This repository only compiles data - I will not be publishing my conclusions on the effectiveness of the added capacitances. It is up to you, dear reader/listener, to decide for yourself. All of the resulting audio recordings will be posted in their own folders above.

![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/5d602105-9260-4540-ba54-c683789a591b)

## Test Procedure

For these tests, I will be taking various models of GBA boards, and following the procedure detailed on this website: https://www.retrosix.wiki/dehum-dehiss-removing-noise-from-gba-audio

On this page, there are a handful of steps for how to improve the audio quality. They are:

1) Cleaning the volume wheel
2) Cleaning the power switch
3) Adding the "dehiss" capacitors - 1uF and 10uF ceramic capacitors in parallel with C15
4) Adding the "dehum" capacitor - a 680uF, 6.3V solid state capacitor from VDD3 to GND 
5) Adding a capacitor to clean up noise induced by IPS kits (I will refer to this as the "over current capacitor") - a 680uF, 6.3V solid state capacitor from VCC to GND

One step that is not included that's often recommended is also cleaning the headphone jack.

### Controlling for Clean Components

In order to remove any lack of personal skill involved in cleaning the volume wheel, power switch, and headphone jack, I will be performing the following control conditions:

1) Short VR2-3 and VOL test points using a wire to force the volume to be maximum. (The volume wheel will also be in the maximum volume position)
 
![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/77c333ec-ee2b-4ebb-96db-bb26c74765c6)

2) Short SW1-2 and VCC test points using a wire to force the power switch to be on all the time. This will bypass any ill effects of an old/dirty power switch. The switch will be in the ON position to prevent the 150 ohm bleeder resistor R13 from being connected to the batteries.

![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/06117612-4d25-4d21-bf45-f86eee24c015)

3) Use a brand new headphone jack wired in parallel with the original headphone jack, with which to record audio. The original socket will have a blank jack plugged in to force the audio to output in headphone mode.

### Test Points

I will record audio for seven test points, output from the headphone jack into the microphone input of my PC, as defined by steps 3 through 5 above:

1) An original PCB with no added capacitance, and a stock screen
2) An original PCB with no added capacitance, and an IPS kit
3) Adding the dehiss capacitors, with a stock screen
4) Adding the dehiss capacitors, with an IPS kit
5) Adding the dehum and dehiss capacitors, with a stock screen
6) Adding the dehum and dehiss capacitors, with an IPS kit
7) Adding the dehum, dehiss, and over current capacitors, with an IPS kit

These data points will be collected for every model of GBA board I am able to test. The standard test set up will be with AA batteries, but I will collect one set of data with a lithium ion battery as well to compare.

I will also record the following information for every tested GBA:

1) Board revision
2) AGB CPU revision
3) PMIC part number
4) Audio amp part number
5) LCD bias chip presence (32-pin vs 40-pin screen connector)

## Test Equipment and Components

- Various revisions of GBAs
- 2x eneloop Pro AA batteries (fully charged) connected via battery holder
- 1x PKCELL LP803860 lithium-ion battery (charged to 3.65V, only used for testing AGB-CPU-03)
- 1x of each stock AGB screen (32-pin and 40-pin)
- 1x IPS AGB screen kit (Funnyplaying GBA IPS v2)
- 1x brand new headphone jack (SJ2-3525N)
- 1x 1uF, 25V, X5R ceramic capacitor (C0603C105K3PACTU)
- 1x 10uF, 25V, X5R ceramic capacitor (GRM188R61E106KA73J)
- 2x 680uF, 6.3V, solid state aluminum electrolytic capacitor (A750EK687M0JAAE008, specifically chosen for the low ESR)
- 1x audio cable, connected from headphone jack to PC's microphone input
- Pokemon Fire Red version, authentic

# Results

## AGB-CPU-02

- **CPU Revision:** CPU AGB
- **PMIC:** MM1514X
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-02">Link to folder of recordings</a>

## AGB-CPU-03 #1

- **CPU Revision:** CPU AGB A
- **PMIC:** 9750B
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

Recordings were taken with both AAs and LiPo

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-03">Link to folder of recordings</a>

## AGB-CPU-03 #2

- **CPU Revision:** CPU AGB
- **PMIC:** 9750A
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-03_%232">Link to folder of recordings</a>

## AGB-CPU-10 #1

- **CPU Revision:** CPU AGB A
- **PMIC:** 9750B
- **Amp:** IR3R60N
- LCD bias chip not included (32-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-10">Link to folder of recordings</a>

## AGB-CPU-10 #2

- **CPU Revision:** CPU AGB A
- **PMIC:** S6960
- **Amp:** BH7835AFS
- LCD bias chip not included (32-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-10_%232">Link to folder of recordings</a>
