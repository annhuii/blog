
+++
date = '2026-06-15'
draft = false
title = 'How I use an Ambient Scribe'
description = "and why it has made me a better doctor"
summary = "even "good enough" has made me a better doctor.
The case of an in-house ambient scribes in public healthcare"
+++

## Introduction

I'm sharing my experience of using NoteBuddy, the only white-listed ambient scribe in Singapore's public healthcare system.

The reasons for my note are two-fold:

1. I have significant difficulty convincing colleagues to uptake an ambient scribe, noticing this resistance to the new, despite my promises of the exponential benefits, and walking them through the process. I hope this platform allows reach beyond my immediate colleagues.
2. NoteBuddy is a rare example of what an ambient scribe with no commercial incentives can look like in a public healthcare system. Globally, ambient scribes have grown with expanded clinical decision support offerings. NoteBuddy was developed by an in-house team together with Microsoft, localized for the multi-lingual Singaporean population. Is NoteBuddy is clunky (and ugly)? Yes. Has it brought the joy back to medicine? Yes. Does that make it good enough? Yes!

---

## When do I use an ambient scribe

In the chaos of the ER (or A&E, or ED), I find the scribe most helpful in the ambulatory setting, where there is a quiet, and a dedicated desk.

I used to absolutely dread ambulatory shifts. It's no exaggeration that NoteBuddy is the main reason why I now find ambulatory shifts a welcome break from the higher acuity settings. I am expected to see around 15 patients in 9 hours, in an ER that sees 320 patients a day. Knowing that I have an ambient scribe has allowed me returned my focus on the person before me, the reason why doctors enter medicine.

NoteBuddy is seamlessly embedded within my workflow to a T.

1. Right before my patient enters my room, I start my scribe such that the encounter starts at the very beginning of hello.
2. With the EHR open, I quickly save a blank entry note. At the end of my history taking, I ask my patient to lie on the couch, while I quickly order investigations.
3. When my patient leaves the room, I click the generate note button (NoteBuddy will take about 30 seconds to generate a summary in the SOAP format).
4. Simultaneously, I am printing my stickers for my blood tubes, placing the stickers on my blood tube.
5. That short walk to the pneumatic tube sending station, gives me a moment to gather my thoughts, while my hands are busy placing the blood tubes into a ziplock.
6. When back in my room, I review the summary and makes edits. I accept that the output will still require my review.

Another far less common, though unavoidable, scenario is the documentation of a lengthy clinical encounter, for whatever reason (such as healthcare worker abuse, or against medical advice discharge). Using a family conference communication prompt I've borrowed from my oncology colleagues, I've found that I've needed to make minimal changes to the summary, which is accurate, factual and professional. While the encounter itself might take 30 minutes, the documentation might take just as long. This is a far cry from my days when I was an intern (or house officer), and I sometimes had to sit into family conferences to take minutes, which my senior would then review for language. I've often been uncomfortably aware of the power discrepancy in the clinical note, where the patient's voice is transcribed through my perception, and with a scribe, I have found that the patients perspectives feature with more weight.

---

## Using an ambient scribe has made me a better doctor

While patients triaged in the ambulatory setting are the least sick, their concerns can be grave. Why else would they come to the hospital and wait three hours? In a time-strapped environment, I have noticed the risk to dismiss. What's the most efficient in the ambulatory setting is to foreground their concerns first. Patients might be embarrassed but now I can look them in the eye and they know they have my full attention.

Looking at my patients, has given me the ability to notice the patient as a person, and a tacit understanding of the social context of my patient. What's the body language between the patient and their family like? Might there be a reason for visit that is not medical, such as an unsafe home environment, and I have to exercise my fiduciary role to intervene?

I am a translator of my patient's experience into medicalese.[^1] One of the most common complaints is giddiness, rather than taking that as face value, I have to ask patients what do they mean exactly, is that weakness, or vertigo? I dislike the imprecision of the term numbness, is that a reduced sensation as opposed to a tingling sensation (ants crawling on your skin), can mean the world of a difference of urgency. With a scribe, I am not fixated on using my working memory in trying to remember what has just been said, and I don't have to resort to typing my notes while my patient is speaking.

---

## How do I select/design/use a prompt?

1. Select a prompt based on your department. Do not start from scratch: "Steal" a prompt from the super users in your department, or prompts from the same department in different hospitals. I don't find that the specific hospital matters that much.
2. Update the prompts to suit your needs.
   - I like my note to reflect the personality of my patient, and my thought process. The danger I found with the blank prompts, is that it reduces the clinical encounter to a checklist, without reflecting the nuance of the humanity.
   - Additionally, clinical decision making inherently carries uncertainty, and I wanted my note to show how my thought process and with the diagnosis or plan as a natural conclusion.

### a. Subjective

- The first line of all my notes in the ED will reflect their social circumstances. Who do they live with, how did they come in, what's their baseline functional status.
- When I edit the summary, the next line will be a one liner of their presenting complaint, and includes the duration of their symptoms. The line that follows after, will be their concern.
- E.g. First time, sudden onset vertiginous giddiness, a/w nausea starting at 9am, 2 hours after she woke up. Patient is concerned about a heart attack, as her father passed away from a cardiac event when she was a child.

### b. Objective

- I still type out the vitals manually, because that's how I internalize the vitals.
  - How it might change from at triage, to a repeated reading, and one by my bedside, or even at the outpatient setting where the patient visited before coming to the ER.
- I usually remove all the physical examination findings. The summary usually states the results it in a way that is unnatural, through a systems approach with NEURO, CARDIO headers. I prefer my notes to reflect the process of inspection, palpation, auscultation. I still find it unusual to narrate the physical examination findings out, for I find it still gives me flashbacks to final year medical school exams.

### c. Assessment and Plan

- I usually completely remove this section completely, alongside the physical examination findings; however, I usually these sections in my prompt because it sometimes remembers to capture information I've forgotten.
- With this, I find that I had to update the prompt to standardize the of headers. I usually only retain the headers of the subjective section, which is the first section. Out of habit and for visual consistency, I have standardized the header to be `=hx=`, rather than `S/`.

---

## Suggestions to increase the uptake of NoteBuddy

The use of ambient scribes is far from universal. I wouldn't have started using NoteBuddy had my attending didn't show me how to use it one slow Saturday afternoon. Now I repeat this process with my colleagues, yet have not been an unsuccessful proselytizer.

To improve my experience of NoteBuddy, and hopefully reduce friction to adoption, I've some suggestions:

- First of, I purchased an inexpensive <$10 conference microphone that I can plug into the audio jack of any hospital computer, to improve the quality of sound capture and hence summary quality. I've tried loaning this to my colleagues (often those I've handed over my patients to) to use on their shifts, if every computer came with a microphone, there would be a much lower barrier of usage.
- Second, I've bookmarked NoteBuddy on the internet browser for every computer I use. As NoteBuddy attempts outreach outside of SingHealth institution, the cumbersome log-in method of clicking through the web application section of SingHealth website needs to be revised.
- Third, in an inpatient setting when rounding is the source of documentation, the mobile app version is not reliable or user-friendly enough to be usable. For security reasons, NoteBuddy has to be accessed through the Microsoft Teams mobile app. To use the output, NoteBuddy must be opened on a web application on a physical computer. When there are multiple patients, this can become extremely disruptive.
  - That being said, a potential use case is on call rounding, especially in surgical teams. Capturing the information rapidly and sitting around to gather and edit the notes together makes far more sense. This could make calls less tiring, and capture information more completely when one's already sleep deprived and more prone to forgetting.
 
[^1]   "Since eighty percent of diagnoses in primary care result from the history alone, the anamnesis (the account the physician assembles from the patient's history) is crucial. The tale of complaints becomes the text that is to be decoded by the practitioner cum diagnostician." Kleinman A. The illness narratives: suffering, healing, and the human condition. New York, NY: Basic Books; 1988. p. 17.<img width="468" height="74" alt="image" src="https://github.com/user-attachments/assets/c98957ea-94b1-417c-a2ed-68e0f6fbadb7" />


---

## Conclusion

There are concerns of deskilling from within the medical community that taking away the practice of note writing, will take away the skills of clinical reasoning.

Notes, in my experience, have rarely captured the reality of the clinical encounter. As a medical student, I often read notes and left with no understanding of why the patient was here. As a house officer, I was struck by how the team knew about and retained information on patients purely through the verbal presentations during rounds.

Doctors will always need to write a note synthesizing information. What I've found is to the contrary, with my experience in a limited setting, I have been able to attain a higher practice of medicine, more than just reasoning, but also storytelling.

