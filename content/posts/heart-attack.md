+++
date = '2023-12-12'
draft = false
title = '... Heart Attack?'
description = ''
+++

On my first 24 hour call, I cared for a man who almost died of a heart attack. I was first called in the mid-afternoon for sweating, a symptom dreadfully non-specific.

This could be a heart attack, I thought, looking at his vasculopathic history on the electronic medical record. Glancing quickly at my crumpled list of bed numbers of patients I needed to see, I rushed to see him first. Do you have any chest discomfort, difficulty breathing, nausea, neck or shoulder pain? No, no, no, he chirped, sitting with his legs dangling off the hospital bed, eating his lunch.

Relieved, but still on high alert - I sent investigations off. The electrocardiogram was suspicious of, but did not meet the strict criteria of a heart attack. The cardiac enzymes were high, but not unexpected in a man with a failing kidney. I alerted my immediate senior, just in case this was something more and required a cardiology referral. The plan was clear, for the time being, to continue to trend both the electrocardiogram and cardiac enzymes and to monitor his vital signs closely.

Hours later, my senior called. The patient's oxygen level had dropped dramatically. Compared to hours ago, he was now agitated, hurling his torso back and forth, limbs flailing, screaming to his wife on video call that he was going to die. For minutes that felt like hours, I tried to insert a cannula and get a arterial blood sample, with the movement, I just couldn't.

Then, he stopped. He fell backwards, limp. He had no pulse. Code blue was activated.

Eventually, the pulse returned. He was admitted to the intensive care unit, and the investigations showed he had a definite heart attack.
~70 overnight calls and many code blues later, I still remember the terror in his eyes, and the terror I felt that night. Did I do something wrong? Should I have known?

To satisfy this hunger, I looked at the data.

Research Question
"In a resource-limited setting, what are the best predictors of cardiac disease requiring cardiac catheterisation?"
In the popular imagination, a heart attack usually conjures up an image of a person clutching their chest in indescribable pain, before suddenly collapsing. The diagnosis of acute myocardial infarction, which is what a heart attack actually is, requires a constellation of symptoms and investigations to point towards a diagnosis¹ (1) Symptoms - chest pain, which has a typical description, is a key feature² (2) Electrocardiogram findings (3) Cardiac enzymes. In reality, the diagnosis of atherosclerotic coronary vessel disease requiring cardiac catheterisation, is complex. Cardiac catheterisation is not without risks - it requires a large needle inserted in the groin to track up to the blood vessels of the heart. There is risk of injury to the major vessels of the groin, a risk of tearing the heart wall, or aorta, and instigating life-threatening irregular heart rhythm. Unfortunately, the gold standard for diagnosis, a coronary angiogram, is also almost just as invasive as the treatment.

What we do for a patient who clearly is clearly having an acute myocardial infarction is clear - but what do we do for the patients whom we suspect but who don't fit the criteria? Many technologies have been developed, but they are often only available in tertiary centres, and are not appropriate for an acute setting of a heart attack.

Going back to that night, his symptoms and investigations did not clearly point to a diagnosis of myocardial infarction. As the nurses were busy, I applied the electrocardiogram leads on, and took the bloods myself, but what if there was a delay in the laboratory? I would have missed a key diagnostic data point.

Cardiologists, like surgeons, needed to be alerted at the exact moment with the exact information and exact investigations done; too early and you're wasting their time, too late, and the patient might have passed the point of no return.

I wondered, what if I only had the patient's history, and electrocardiogram findings - how useful would that be in predicting the need for catheterisation?

Methodology

Dataset
The UC Irvine Heart Disease dataset³ was first published in 1989, and comprised patients undergoing cardiac catheterisation from various institutes in the US and Europe. These patients underwent non-invasive testing including a stress testing in which vitals signs were measured and an electrocardiogram was performed. With over a thousand patients, it has been used in machine learning datasets.
The raw data includes 13 factors, patient factors (age, sex, thalassaemia), symptoms (type of chest pain - typical angina, non-anginal pain, atypical angina, asymptomatic, and exercise-induced angina), vital signs (resting blood pressure, maximum heart rate achieved during exercise stress test), laboratory test results (cholesterol, fasting blood glucose), non-invasive cardiac investigations (electrocardiogram at rest - ST-T wave abnormalities, left ventricular hypertrophy, or normal, with exercise stress test - if exercise induced ST depression, slope of ST segment), and the number of vessels of involved in coronary angiogram.

The statistical analysis was performed with Python on Juptyner lab using the LogisticAT package.

![alt text](/heartattack1.webp)
![alt text](/heartattack2.webp)

Weaknesses of the dataset

We don't have much information about how the symptom data was collected. People can report a heart attack in many different ways, and there are many factors that are not accounted for that could affect the expression and interpretation of a symptom. For example, the cultural background, the language spoken by the patient or the data collector could interact with the eventual reporting of the symptoms. Only recently has the myth that women with myocardial infarction present differently from men been debunked.⁴

We also don't know much about the patient selection criteria for the dataset, which may reflect the resources available to certain centres.⁵ It is unclear why patients who are asymptomatic and have normal electrocardiograms are referred for invasive coronary angiogram in the first place.

We don't have the patient's past medical history which is crucial. That night, despite the absence of classic symptoms and investigations, I had a high index of suspicion for cardiac disease because of his vasculopathic history. Diabetes mellitus⁶ is a risk factor for silent myocardial infarction, and fasting blood sugar itself is not sufficient for diagnosis.

Data Preparation

I focused specifically on information that would be available within minutes, such as type of chest pain, exercise-induced angina, and electrocardiogram findings, and how these might affect the number of vessels involved in cardiac disease as shown on coronary angiogram.

First, I checked the number of unique data points per data type.
![alt text](/heartattack3.webp)

Second, as the data was presented in textual form, I converted the information in numerical form for ease of analysis. I ordered the data points in ranking from least to most likely to have cardiac disease requiring catheterisation.
![alt text](/heartattack4.webp)
![alt text](/heartattack5.webp)

Third, I wanted to examine the interaction between data points, to reflect the reality of clinical practice, which is often based on the basis of interaction of different pieces of information.

Fourth, for simplicity, I isolated only the relevant data points that were needed.
![alt text](/heartattack6.webp)

Data Analysis
I performed a linear regression to examine the strength of prediction between individual data points and their interaction on coronary disease requiring catheterisation.
![alt text](/heartattack7.webp)

Results
![alt text](/heartattack8.webp)

Data Interpretation

While most of the factors were statistically significant, in the absence of cardiac enzymes availability, electrocardiogram findings had the strongest correlation with the number of occluded vessels.

Counterintuitively, the combination of factors turned the coefficient negative and reduced the magnitude of the coefficient. This warrants further analysis.

Discussion

The usual way learning is through a sequence of history, physical examination, investigations, and then management. However, with evidence-based medicine, certain components are given greater weight in decision making. While I originally intended this study to answer a question I was facing, I also wondered about the wider implications for clinical practice, what about do we do with patients who don't fit into this sequence? Who are asymptomatic but need coronary intervention, or who have chest pain but don't have cardiac disease - when should I stop with the expensive investigations?

Medicine is both an art and a science - but above all it is a practice. While medical school teaches you how diseases should occur, and should be treated, most patients don't present as textbook case studies. As I've learnt, the practice of medicine requires dealing with the grey zone, and therefore requires a clinical judgement, balancing (legally indefensible) gestalt and evidence-based medicine.

Ultimately, what we do, we do for patients. For this patient, he refused cardiac catheterisation, and was discharged home shortly afterwards against medical advice. More than heroic interventions, I wondered what were the barriers to care were, and what we could do as healthcare entities/institutions to reach out, and prevent heart disease in the very first place.

---

Bibliography

¹ 2021 AHA/ACC/ASE/CHEST/SAEM/SCCT/SCMR Guideline for the Evaluation and Diagnosis of Chest Pain: A Report of the American College of Cardiology/American Heart Association Joint Committee on Clinical Practice Guidelines | Journal of the American College of Cardiology. Accessed December 24, 2023. https://www.jacc.org/doi/10.1016/j.jacc.2021.07.053#sectitle0090

² Anderson HV ("Skip"), Masri SC, Abdallah MS, et al. 2022 ACC/AHA Key Data Elements and Definitions for Chest Pain and Acute Myocardial Infarction: A Report of the American Heart Association/American College of Cardiology Joint Committee on Clinical Data Standards. Circulation: Cardiovascular Quality and Outcomes. 2022;15(10):e000112. doi:10.1161/HCQ.0000000000000112

³ Janosi,Andras, Steinbrunn,William, Pfisterer,Matthias, and Detrano,Robert. (1988). Heart Disease. UCI Machine Learning Repository. https://doi.org/10.24432/C52P4X.

⁴ van Oosterhout REM, de Boer AR, Maas AHEM, Rutten FH, Bots ML, Peters SAE. Sex Differences in Symptom Presentation in Acute Coronary Syndromes: A Systematic Review and Meta‐analysis. Journal of the American Heart Association. 2020;9(9):e014733. doi:10.1161/JAHA.119.014733

⁵ Kentenich H, Müller D, Wein B, Stock S, Seleznova Y. Methods for assessing guideline adherence for invasive procedures in the care of chronic coronary artery disease: a scoping review. BMJ Open. 2023 Mar 15;13(3):e069832. doi: 10.1136/bmjopen-2022–069832. PMID: 36921955; PMCID: PMC10030787.

⁶ Kumar A, Sanghera A, Sanghera B, Mohamed T, Midgen A, Pattison S, Marston L, Jones MM. Chest pain symptoms during myocardial infarction in patients with and without diabetes: a systematic review and meta-analysis. Heart. 2023 Sep 28;109(20):1516–1524. doi: 10.1136/heartjnl-2022–322289. PMID: 37080764.
