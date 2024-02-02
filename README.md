# Power Cleaner Tests

This repository is a compilation of recordings of the Game Boy Advance (AGB) audio output, before and after adding various capacitors provided by "Power Cleaner" mods. There has been a lot of discussion about what these mods achieve, but I haven't seen any actual empirical evidence. I've been looking at the AGB more recently, so I figured I'd do a deeper dive into the topic and provide some recordings so people can hear the differences for themselves.

This repository only compiles data - I will not be publishing my conclusions on the effectiveness of the added capacitances. It is up to you, dear reader/listener, to decide for yourself. All of the resulting audio recordings will be posted in their own folders above.

![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/5d602105-9260-4540-ba54-c683789a591b)

## Test Procedure

For these tests, I will be taking various models of GBA boards, and following the procedure detailed on this website: https://www.retrosix.wiki/dehum-dehiss-removing-noise-from-gba-audio

On this page, there are a handful of steps for how to improve the audio quality. They are:

1) Cleaning the volume wheel
2) Cleaning the power switch
3) Adding the dehiss capacitors - 1uF and 10uF ceramic capacitors in parallel with C15
4) Adding the dehum capacitor - a 680uF, 6.3V solid state capacitor from VDD3 to GND 
5) Adding a capacitor to clean up noise induced by IPS kits (I will refer to this as the "over current capacitor") - a 680uF, 6.3V solid state capacitor from VCC to GND

One step that is not included here that's often recommended is also cleaning the headphone jack.

### Controlling for Dirty/Old Components

In order to remove any lack of personal skill involved in cleaning the volume wheel, power switch, and headphone jack, I will be performing the following control conditions:

1) Short VR2-3 and VOL test points using a wire to force the volume to be maximum. (The volume wheel will also be in the maximum volume position)
 
![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/77c333ec-ee2b-4ebb-96db-bb26c74765c6)

2) Short SW1-2 and VCC test points using a wire to force the power switch to be on all the time. This will bypass any ill effects of an old/dirty power switch. The switch will be in the ON position to prevent the 150 ohm bleeder resistor R13 from being connected to the batteries.

![image](https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/06117612-4d25-4d21-bf45-f86eee24c015)

3) Use a brand new headphone jack wired in parallel with the original headphone jack, with which to record audio. The original socket will have a blank jack plugged in to force the audio to output in headphone mode.

### Test Points

I will record audio for seven test points, output from the brand new headphone jack into the microphone input of my PC, as defined by steps 3 through 5 above:

1) An original PCB with no added capacitance, and a stock screen
2) An original PCB with no added capacitance, and an IPS kit
3) Adding the dehiss capacitors, with a stock screen
4) Adding the dehiss capacitors, with an IPS kit
5) Adding the dehum and dehiss capacitors, with a stock screen
6) Adding the dehum and dehiss capacitors, with an IPS kit
7) Adding the dehum, dehiss, and over current capacitors, with an IPS kit

These data points will be collected for every model of GBA board I am able to test. The standard test set up will be with AA batteries, but I will collect one set of data with a lithium ion battery as well to compare.

I will also note the following information for every tested GBA:

1) Board revision
2) AGB CPU revision
3) SRAM part number
4) Crystal oscillator manufacturer
5) PMIC part number
6) Audio amp part number
7) LCD bias chip presence (32-pin vs 40-pin screen connector)

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

As mentioned earlier, I will not be posting my personal analysis of the data to keep this as impartial as possible. I can confirm that the recordings here match what I hear with headphones *and* on the speaker, so my recording set up is a valid way of capturing the audio.

Each folder contains .wav recordings of all tests, including an Audacity project compiling all recordings for further analysis, if anyone wants to plot some audio spectrums or something.

For each of these headings, I will include a .mp4 file (GitHub does not allow embedding of .wav files) to show what a stock system sounds like, unmodified. The .wav files of these recordings are included in each folder as well, they're just posted here for reference and easy comparison. Not all Game Boy Advances are created the same! There are definite differences in audio quality between the systems I tested (though none are unbearable to listen to, in my opinion).

## AGB-CPU-02

- **CPU Revision:** CPU AGB
- **SRAM:** NEC D442012AGY-BC85X-MJH
- **Crystal:** Kinseki
- **PMIC:** MM1514X
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-02">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/92ffb846-9aab-4656-bb53-d61d84b8b03d

## AGB-CPU-03 #1

- **CPU Revision:** CPU AGB A
- **SRAM:** Toshiba TC55V200FT-70
- **Crystal:** Kinseki
- **PMIC:** 9750B
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

Recordings were taken with both AAs and LiPo

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-03">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/5fbff1c3-a372-483c-83d0-be5cc0ea4e91

## AGB-CPU-03 #2

- **CPU Revision:** CPU AGB
- **PMIC:** 9750A
- **SRAM:** NEC D442012AGY-BC85X-MJH
- **Crystal:** Daishinku
- **Amp:** IR3R60N
- LCD bias chip included (40-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-03_%232">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/d9caf81d-3ee3-4260-bb24-644a31c1a194

## AGB-CPU-10 #1

- **CPU Revision:** CPU AGB A
- **SRAM:** Fujitsu MB82D12160-10FN
- **Crystal:** Kinseki
- **PMIC:** 9750B
- **Amp:** IR3R60N
- LCD bias chip not included (32-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-10">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/f3edeebb-2702-4dd0-abea-1fca8014b980

## AGB-CPU-10 #2

- **CPU Revision:** CPU AGB A
- **SRAM:** Hynix HY62LF16206A-LT12C
- **Crystal:** Daishinku
- **PMIC:** S6960
- **Amp:** BH7835AFS
- LCD bias chip not included (32-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-10_%232">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/45feb38f-c7ad-4641-a2d2-dfc1bd15fdbd

## AGB-CPU-10 #3

This one is actually a combination of #1 and #2. It is the same as #1, but I swapped the audio amplifier chip from #2 onto it and removed C45, C46, and C47 (as seems to be done with the BH amp according to the Game Boy Hardware Database).

- **CPU Revision:** CPU AGB A
- **SRAM:** Fujitsu MB82D12160-10FN
- **Crystal:** Kinseki
- **PMIC:** 9750B
- **Amp:** BH7835AFS
- LCD bias chip not included (32-pin)

<a href="https://github.com/MouseBiteLabs/Power-Cleaner-Tests/tree/main/AGB-CPU-10_%233">Link to folder of recordings</a>

### Baseline System Recording

https://github.com/MouseBiteLabs/Power-Cleaner-Tests/assets/97127539/d95b09b7-42ab-49c6-b106-172001a0e08a

# Resources

- Retrosix Wiki - https://www.retrosix.wiki/dehum-dehiss-removing-noise-from-gba-audio
- Game Boy Hardware Database - https://gbhwdb.gekkio.fi/consoles/agb/
- Console5 Wiki - https://wiki.console5.com/wiki/Game_Boy_Advance
