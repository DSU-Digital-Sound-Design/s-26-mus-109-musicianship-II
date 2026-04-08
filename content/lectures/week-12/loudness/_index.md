+++
title = "Loudness, the Confluence of Domains and Deep Listening"
outputs = ["Reveal"]
[reveal_hugo]
theme = "beige"
margin = 0.2
separator = "##"
+++


## What is Loudness? Perception vs. Physics

- **Loudness:** How loud we *feel* or *perceive* a sound is.
- It's related to physical sound pressure (amplitude), but it's subjective.
- Our ears hear different frequencies (pitches) at different perceived loudness levels, even if their physical intensity is the same.
- Context matters! Our biases, expectations, and environment change how loud we think something is.

{{% note %}}

- Loudness is the perceived intensity of sound — a psychological experience, not a physical measurement.
- Many things beyond the sound itself shape perception: personal biases, listening context, and expectation all play a role.
- What one person considers "loud" varies by cultural background, environment, and emotional state.
- The equal-loudness contours (Fletcher-Munson curves) show this directly: hearing sensitivity varies across frequencies, so a 1kHz tone can sound much louder than a 100Hz tone at identical SPL.

{{%/ note %}}

---

## Loudness as a Recording Tool

- Producers and engineers actively shape loudness in recordings.
- They can make sounds seem louder or softer than they were in the original performance, creating unique sonic textures.
- When analyzing recordings, we try to focus on the sensation of loudness itself, separate from performance energy (intensity) or sound color (timbre).
- This requires focused, critical listening.

{{% note %}}

- Shaping loudness is one of the most basic tools in recording and mixing. A producer can make something sound louder or softer than it was in the room, shifting the feel of a performance entirely.
- When listening analytically, try to isolate the sensation of loudness itself — separate from the performer's physical exertion (intensity) or the character of the sound (timbre).
- That separation takes practice. Once you can hear loudness on its own, you can approximate levels against a reference like the RDL and follow how loudness shifts across the track.
- Loudness gives sounds presence, but not necessarily prominence. A quiet sound can command more attention than a loud one.

{{%/ note %}}

---

## Loudness vs. Prominence: What's the Difference?

- **Loudness:** How intense a sound *feels* subjectively.
- **Prominence:** What grabs your attention in the mix.
- **Key Idea:** The most prominent sound isn't always the most intense (SPL)
    - Example: A quiet but unexpected shaker entry might be more *prominent* than a constant loud pad sound.
- Attention directs perception

{{% note %}}

- Attention changes what we hear. Focus on a quiet sound and it can feel louder than its physical level suggests — that's the gap between *prominence* and *loudness*.
- Prominence has many sources besides level:
    - Novelty — a new sound entering the texture
    - Timbre — a contrasting or unusual sound color
    - Spatial location — something appearing where you didn't expect it in the stereo field
    - Rhythm — a syncopated or disruptive rhythmic pattern
    - Expectation — hearing something you were waiting for

{{%/ note %}}

---

## Prominence Example & Musical Dynamics

- **Dynamics (in Music):** More than volume — *overall* shifts in expression, energy, and intensity across loudness, timbre, articulation, and performance feel.
- **Example:** "Let It Be" (Spector mix) — the hi-hat at 0:53 is *prominent* due to surprise, not volume.
- <iframe allow="autoplay *; encrypted-media *;" frameborder="0" height="150" style="width:100%;max-width:660px;overflow:hidden;background:transparent;" sandbox="allow-forms allow-popups allow-same-origin allow-scripts allow-storage-access-by-user-activation allow-top-navigation-by-user-activation" src="https://embed.music.apple.com/us/album/let-it-be/1441164495?i=1441164738"></iframe>

{{% note %}}

- The hi-hat at 0:53 in the Spector mix isn't unusually loud — but it stops the ear cold. Its timing and surprise do more than its level. That's prominence.
- Keep dynamics broad when you use the term. Loudness is part of it, but dynamics also include timbre changes, articulation, and the raw energy of the performance. When analyzing, try to hear loudness as its own layer, separate from those other things.

{{%/ note %}}

---

## Why Measuring Perceived Loudness is Tricky

- **Equal Loudness Contours:** Same SPL sounds different across frequencies.
- **Subjective Increments:** No agreed-upon steps for "how much louder."
- **Confusion with SPL:** dB is physical; loudness is perceptual. Not the same scale.
- **No perfect meter:** LUFS approximates it, but no method fully captures perception.

{{% note %}}

- Equal-loudness contours make a single linear scale impossible — the relationship between frequency and perceived loudness isn't uniform.
- You can't easily define "twice as loud" because loudness is subjective, unlike frequency or physical sound pressure.
- The dB/SPL confusion trips people up constantly. Doubling SPL does not double perceived loudness.
- No measurement method fully captures how humans hear loudness across all sounds and contexts. LUFS is the best working approximation we have.

---

{{%/ note %}}

## Measuring Loudness: Meet LUFS

- **LUFS:** Stands for Loudness Units Full Scale.
- It's the modern, standardized way to measure perceived loudness in digital audio.
- **Goal:** To measure loudness more like humans actually *hear* it, unlike older methods (Peak, RMS dB).
- **Why?** Creates consistency across platforms (broadcast, streaming, etc.). Essential for mastering today.

{{% note %}}

- LUFS is based on ITU-R BS.1770, developed to stop wildly mismatched loudness levels across TV, radio, and streaming.
- K-weighting is built into the measurement: an EQ curve that boosts frequencies where hearing is most sensitive and pulls back the extremes, so the meter responds more like an ear would.
- That's what makes it more useful than peak or RMS. Peak ignores duration; RMS ignores frequency sensitivity. LUFS accounts for both.

{{%/ note %}}

---

## Key LUFS Measurements

- **Integrated LUFS:** Average loudness over the entire track. *(streaming targets)*
- **Short-Term LUFS:** Rolling 3-second average. *(section loudness)*
- **Momentary LUFS:** Rolling 400ms average. *(immediate peaks)*
- **True Peak (dBTP):** Highest peak, including between samples. *(prevents clipping)*

{{% note %}}

- Integrated LUFS is the headline number: average loudness across the whole track, start to finish. Streaming platforms specify this one.
- Short-Term LUFS is a three-second rolling window. Use it to see how loudness shifts between sections or to keep a longer program consistent.
- Momentary LUFS moves fast — it catches brief spikes and shows immediate loudness at any moment.
- True Peak catches peaks that fall between sampled points, which standard peak meters miss entirely. Those inter-sample peaks cause clipping when audio converts to analog or gets encoded as MP3/AAC. That's how you catch them before they cause problems.

{{%/ note %}}

---

## Putting Loudness Meters to Use

- Listen actively while watching a LUFS meter (routed through software like Reaper).
- Compare the LUFS readings of different songs (e.g., older vs. newer tracks).
- Use tools like [MLoudnessAnalyzer](https://www.meldaproduction.com/download/documentation/MLoudnessAnalyzer.pdf) to visualize loudness over time.
- This helps develop your ear for perceived loudness and understand how tracks meet delivery standards.

{{% note %}}
Route audio through Reaper and watch the LUFS meter in real time — it's one of the fastest ways to connect the numbers to what you're hearing. Compare mastered tracks from different eras: pre-streaming records are often much louder, and the loudness wars of the 2000s show up clearly in the Integrated readings. Melda's analyzer visualizes all four measurements at once, which helps when you're first learning to correlate them.
{{%/ note %}}

---

## Key Loudness Concepts in a Mix

- **Loudness Balance (Musical Balance):** How loud individual instruments/sounds are *relative to each other*. Crucial for the mix's character.
- **Reference Dynamic Level (RDL):** The track's overall *impression* of intensity or energy level. A stable reference point.
- **Track Loudness Contour:** The *shape* of the overall loudness (combination of all sounds) as it changes throughout the entire track.

{{% note %}}

- Loudness balance is what mixing is about at the most basic level. Engineers set it with fader levels, processing, and arrangement — it determines foreground, background, and everything in between.
- The RDL isn't a dB value you can read off a meter. It's the felt intensity level of the whole track — performance energy, tempo, and instrumentation rolled into one impression. You use it as a reference when judging how loud or soft any part of the track sounds in context.
- The Track Loudness Contour is the shape of overall loudness across the whole track, moment to moment. When you can see and hear that shape, the track's structure becomes much more legible.

{{%/ note %}}

---

## Understanding the RDL (Reference Dynamic Level)

- Think of it as the track's 'home base' or central intensity level.
- It's a *holistic feeling* reflecting the overall energy, performance force, emotion, and tempo.
- We use this felt RDL as a reference point to judge how loud or soft other parts of the track feel *in context*.
- Related to the idea of "Crystallized Form" - the track's core essence felt all at once.

{{% note %}}

- The RDL encapsulates the overall intensity signature of a track. It's derived from the interplay of all sounds, musical materials, performance gestures, and even lyrical meaning. It's experienced as a single, stable level of intensity.
- Interpreting the RDL is a qualitative assessment. It involves reflecting on the track's felt energy and essence without getting lost in moment-to-moment details. It's about grasping the track's singular, coherent whole.
- The concept of "Crystallized Form" represents perceiving the track's entire essence—its shape, character, energy, meaning—instantaneously, as a unified presence. The RDL is a key component of this overall intensity aspect of the crystallized form.
- While subjective, the RDL aims to capture a shared cultural understanding of the track's intensity, acknowledging that familiarity can refine this perception over time.

{{%/ note %}}

---

## RDL

![](RDL.png)

---

## The Track Loudness Contour

- The overall loudness journey of the entire track, moment by moment.
- It's the combined loudness of *all* instruments and sounds mixed together.
- Imagine a single master volume meter needle dancing throughout the song – that's the contour.
- This changing shape adds drama, movement, and structure to the music.

{{% note %}}
At the highest level of perspective, the track is distilled to a single sensation of loudness; we perceive this level to change continually and to form a contour across the entire track.

This can also be called the "program dynamic contour" or "track loudness contour."

The track loudness contour is the single loudness-level of the track’s aggregate sound; it is the result of the combination of all source loudness levels. It helps some to envision this sensation and concept by thinking of a single VU (voltage unit) meter that displays a representation of the signal level, following the loudness level of the program as it potentially changes at every moment.
{{%/ note %}}

---

## Overall Loudness Level of the Track

![](loudness-hierarchy.png)

{{% note %}}
This image illustrates the hierarchy: the overall track loudness contour sits at the top, representing the aggregate of all underlying source loudness levels and their individual contours.
{{%/ note %}}

---

## Loudness Shapes and Structure

- Loudness exists at different levels: the whole track, sections, individual sounds.
- The shape of the track loudness contour is structurally important!
- It can highlight sections (verse vs. chorus), build tension, and provide release.
- Example: "Here Comes the Sun" uses loudness changes to define its form.

{{% note %}}

- Just like pitch or rhythm, loudness can be analyzed hierarchically. We can discuss the loudness of a single drum hit, a whole drum pattern, a verse section, or the entire track.
- The track loudness contour, the top level of this hierarchy, often mirrors the musical structure. Changes in instrumentation, texture, and performance intensity naturally create loudness shapes that define sections.
- Engineers and producers deliberately craft this contour through arrangement, mixing, and automation to enhance the music's emotional impact and narrative flow.
- In "Here Comes the Sun," the analysis shows how distinct loudness shapes correspond to structural divisions (like verses, choruses, bridge), contributing significantly to the listener's experience of the song's form and dynamic journey.

{{%/ note %}}

---

## "Here Comes the Sun" - Loudness Contour Example

![](dynamic-contour-graph.png)

{{% note %}}
Figure 9.2 illustrates the changes in overall loudness level throughout the track “Here Comes the Sun” (1969, 1987). The graph contains the reference dynamic level of the track (RDL, shown as a line, likely around low mf), against which the contour can be heard. Imbedded in the contour are shapes of loudness that correspond to structural divisions; as the shapes emerge within one’s hearing of the track, their role in defining sections through their repetition becomes apparent. The loudness shape of the track is clearly evident from its beginning at the lower portion of mp to its peak within ff. The wide dynamic range of the track contains subtle changes of loudness as well as large and sudden shifts.

“Here Comes the Sun” is among the uncommon tracks in which the reference dynamic level is prominently experienced. During the final moments of the coda, the level of the track loudness contour matches the track’s RDL; the reference dynamic level is audible as the track’s overall loudness arrives at the track’s overall sense of energy, exertion, and expression (that is the RDL). At this moment, the low mf RDL delivers a sense of arrival and a settling in the place of the conception and expression in which the track exists. It is common for a track to arrive at its RDL as an important occurrence, but it is not common for it to be a point of arrival that provides aesthetic closure to a track.
{{%/ note %}}

---

## Beyond Loudness: The Confluence of Domains

A recorded track isn't just sound – it's a blend of three key areas:

1.  **Music:** Notes, rhythms, harmony, melody, structure.
2.  **Lyrics:** Words, meaning, story, poetic devices.
3.  **Recording:** Mic choices, effects (reverb, delay), mixing decisions (panning, EQ, *loudness balance*), performance capture.

These domains merge and interact to create the final *overall sound quality* and meaning.

{{% note %}}

- This concept emphasizes that a recording is more than the sum of its parts. It exists as a multidimensional texture where elements from music, lyrics, and the recording process itself converge.
- The mix stage is a critical point of confluence, where decisions about spatial image (panning, width), depth (reverb, delay), timbral balance (EQ), and loudness balance shape how these domains are presented together.
- The interplay *between* these domains generates unique qualities and meanings that might not exist in any single domain alone. For example, the way a specific lyric is sung (music/performance) and processed with reverb (recording) creates a combined effect.

{{%/ note %}}

---

## Timbre: The Glue Between Domains

- **Timbre:** The unique 'sound color' or quality of an instrument or voice. What makes a trumpet sound different from a violin playing the same note at the same loudness.
- Timbre acts like glue, binding elements from Music, Lyrics, and Recording together through the actual *sound*.
- It's not just *one* thing – it emerges from the blend (a multi-domain gestalt).
- The range of frequencies a sound occupies (pitch density) and the loudness balance of its internal parts contribute to its overall timbre.

{{% note %}}

- Timbre is a complex percept that integrates various acoustic properties. It doesn't belong exclusively to music (instrument choice) or recording (mic/EQ choices) but emerges from their interaction during performance and production.
- Understanding timbre involves considering its physical attributes (waveform, spectrum), how we perceive it (bright, dull, rough, smooth), how we interpret it (warm, cold, aggressive), and even the imagined physical action creating it (bowing, striking, blowing).
- Concepts like pitch density (how wide or narrow a sound's frequency footprint is) and the internal loudness balance of harmonics and noise components are part of what defines the track's overall timbral texture, influenced by both musical arrangement and recording choices.

{{%/ note %}}

---

## Deep Listening: Hearing More Detail

- **Deep Listening:** Paying extremely close, focused attention to sound.
- It means hearing the subtle details *within* sounds – the texture of a voice, the decay of a reverb, the attack of a drum.
- Different from casual, everyday listening. Requires intention.
- Crucial for noticing the nuances of recording choices and how different elements interact.
- Inspired by composers like Pauline Oliveros and Pierre Schaeffer.

{{% note %}}

- Deep listening involves a deliberate focus on sonic details at any level, from the overall mix down to the micro-textures within a single sound. It's about actively engaging with sound beyond its surface or primary function.
- This practice connects to both analytical listening (identifying musical events, structures) and critical listening (evaluating sound quality, making judgments about recording choices).
- It requires consciously directing attention to aspects of sound we might normally ignore, accessing finer dimensions of timbre, space, and loudness relationships.
- The principle of "equivalence" – being open and receptive to *all* sounds present, without immediate judgment or hierarchy – can facilitate deeper listening.

{{%/ note %}}

---

## Why Listen Deeply?

- Helps you truly understand how loudness works alongside timbre, space, and performance within the mix.
- Reveals how the Music, Lyrics, and Recording domains blend and influence each other.
- Allows you to better perceive the track's overall essence or "Crystallized Form".
- Unlocks a richer, more insightful appreciation of recorded music by revealing hidden sonic layers.

{{% note %}}

- By practicing deep listening, you can better isolate the sensation of loudness and observe its intricate interactions with other elements emerging from the confluence of domains (music, lyrics, recording).
- It allows for a more nuanced perception of how loudness contributes to or contrasts with timbre, spatial placement, rhythmic feel, and lyrical meaning.
- This focused attention helps in sensing the "Crystallized Form" – that instantaneous, holistic grasp of the track's core identity and energy, which includes the RDL.
- Ultimately, deep listening enhances analytical capabilities and deepens the aesthetic experience by making perceptible the subtle craft involved in creating recorded music.

{{%/ note %}}