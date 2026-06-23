+++
date = '2026-06-22'
draft = false
title = 'Generalist AI as second opinion'
description = "How physicians actually use LLMs, and the potential of generalist AI to avoid medical group think"
summary = "the potential of generalist AI to avoid medical group think: the case of pleural effusion in dengue fever"
+++

Counter-intuitively, a Nature Paper (Vishwanath etc 2025) concludes that “Clinical AI tools lagged behind frontier models on every evaluation: knowledge, expert alignment and real-world clinical use across multiple dimensions.”. 

Despite the furore, my bet is the results don’t really matter. Even though the methodology of this short communication has been dissected to death,[^1] I presume clinicians will continue to use both generalist and clinical AI tools, regardless of what the results say.[^2] 

Just as patients seek second opinions, physicians do too.
 
Recently, Dr Lee Cheng Chuan of the National Center of Infectious Diseases encountered a situation where generalist frontier model was able to provide a view and explanation that clinical AI did not, that ultimately was convincing to him and his colleagues in infectious diseases.

A patient with dengue fever developed a massive pleural effusion requiring chest tube insertion. When the pleural fluid was analyzed, it came back as exudative rather than transudative, which immediately raised a clinical question: was there a secondary cause? The implicit assumption driving that concern was that dengue-associated pleural effusions are transudative. This belief was near-universal held consistently since medical school.

Dr Lee gave the prompt “Pleural effusion in dengue fever is a transudate or exudate?” to both generalist tools (Gemini and Deepseek) and clinical AI (OpenEvidence). (Full texts in Annex) 

Both generalist models answered that pleural effusions were exudative, while clinical AI reflected the prevailing medical dogma, stating that effusions were transudative instead. The generalist model also offered a mechanistic explanation: in severe dengue, third-spacing is not limited to fluid alone, albumin leaks out as well, which would shift the effusion into exudative territory.

Looking at the responses it was startling how different the sources of evidence cited were. Clinical AI models are provided access to journals from the traditional bastions of academic medicine, and their citations tend to reflect this curated scope. Generalist models, by contrast, drew from a broader range of sources, resources that fall outside conventional definitions of 'reputable' medical literature. This included physician-sourced wikis (WikEM) and even a Korean blog! The sources that clinical AI cited were behind a paid wall, as expected of a physician-led approach, while the generalist models incorporated sources from mostly open source journals, sometimes via ResearchGate.

Most startlingly, the definitive answer from both generalist models came from a single article (Shabbir et al. 2018) that was published in a predatory journal. 

What I take from this experience is this: Generalist frontier models play a role in challenging medical dogma by surfacing sources that clinical AI models do not deem as sufficiently legitimate. Within academic medicine, there is a hierarchy of knowledge, with systematic reviews at the top and the humble case report near the bottom, the Lancets or NEJMs more trustworthy than an unheard-of journal. 

Clinical AI recreates and reflects that hierarchy. Dengue is concentrated within geographical global south, where the machinery needed for academic medicine might be relatively lacking. While clinical AI only accessed sources published by centers with a rich tradition of academic medicine, it inadvertently left out case series from the global south, where dengue is more likely to be treated, instead citing reviews of the condition. 

Generalist AI, at least in this instance, have shown to be inclusive of knowledges otherwise subjugated.

---

[^1]: Briefly, my critique of the paper is: *1.	Does what measured really matter?* I would almost completely disregard the USMLE question bank for USMLE questions does not tolerate the uncertainty of clinical practice; neither have USMLE test scores been correlated to physician success in any sense aside from matching into highly competitive and highly paid specialties. OpenEvidence’s lack of clarity is almost expected. Communication will not matter as much to physicians who can read and understand medical jargon, and the complexity of the language is meant to convey the nuance anyway. *2.	What is actually measured?* The paper is also published as a brief communication, and difficult to fully evaluate the methodology. The real clinical queries (RCQ), meant to mimic real life searches by physicians, development was added as an afterthought is not rigorous. *3.	Who measures?* The HealthBench is meant to address the patient usage, while USMLE question banks are used for clinician evaluation. Lumping the evaluation of USMLE question banks with HealthBench is likely to obfuscate results. 

[^2]: Or maybe they’ll use the AI that will be embedded within their EMR as a clinical decision support where the main benefit would be from the contextual clues within a patient’s file. On a day-to-day basis, I find it unlikely physicians will take the time to input de-identified information, just to get a diagnosis.

---
Annex:

**Open evidence:**

Pleural effusion in dengue fever is transudate, resulting from increased vascular permeability and plasma leakage rather than inflammation or infection of the pleural space itself.

*Pathophysiology:*
The pleural effusion in dengue occurs during the critical phase of illness (typically around the time of defervescence) as part of a systemic vasculopathy characterized by increased capillary permeability.[1][2] This leads to plasma leakage from the intravascular space into serous cavities, including the pleural, peritoneal, and sometimes pericardial spaces.[1][2] The post-capillary venules are the predominant site of increased permeability.[2]

*Clinical characteristics:*
The serosal effusions reflect the severity of the vasculopathy and are often accompanied by other signs of plasma leakage such as hemoconcentration, ascites, and gallbladder wall edema.[1] Pleural effusions are commonly present during the critical phase and can be detected early with ultrasound, even as early as day 2-3 of fever.[1][3] In one prospective study, pleural effusions were detected in 24% of dengue patients using lung ultrasound, occurring only during the critical-convalescence phase.[3]

The transudative nature of the effusion is consistent with the underlying mechanism of capillary leak syndrome rather than inflammatory or infectious processes. This distinguishes dengue-related pleural effusions from exudative effusions seen in bacterial pneumonia or other inflammatory conditions.

Would you like to explore the fluid management strategies for dengue patients with significant plasma leakage and pleural effusions?

*References*
[1] Dengue. Wilder-Smith A, Ooi EE, Horstick O, Wills B. Lancet (London, England). 2019;393(10169):350-363. doi:10.1016/S0140-6736(18)32560-1.
[2] Pathogenesis of vascular leak in dengue virus infection. Malavige GN, Ogg GS. Immunology. 2017;151(3):261-269. doi:10.1111/imm.12748.
[3] Lung Ultrasound Findings of Patients With Dengue Infection: A Prospective Observational Study. Koyama H, Chierakul W, Charunwatthana P, et al. The American Journal of Tropical Medicine and Hygiene. 2021;105(3):766-770. doi:10.4269/ajtmh.20-1274.

**DeepSeek** (Thought Process: https://chat.deepseek.com/share/bzhpd32jgnrwrwq67f)

The pleural effusion in dengue fever is generally classified as an exudate. Multiple clinical studies and literature reviews have confirmed this, primarily because the fluid is rich in protein, a direct consequence of the increased capillary permeability that characterizes the disease.

Here is a summary of the supporting evidence:

•	Case Reports and Clinical Studies: An analysis of pleural fluid from a patient with dengue fever found it to be exudative in nature.[1] A separate study of 79 patients reported that all pleural effusions were exudative, with a mean protein content exceeding 3.5 g/dL.[2]
•	Reviews and Expert Consensus: A review on the topic notes that pleural effusions in dengue infection are generally exudative, mild, and often bilateral.[3] Similarly, a chapter on imaging in dengue fever states that the effusion is exudative due to increased vascular permeability and plasma loss, which increases the protein content of the fluid.[4]

The primary reason for this exudative nature is the increased vascular permeability caused by the dengue virus. This leads to the "leakage" of plasma, including significant amounts of protein (like albumin) and other large molecules, from the bloodstream into the pleural space. This protein-rich fluid is the hallmark of an exudative effusion.[4, 

Important note: While the above sources classify the effusion as an exudate, it's worth noting that some older or less definitive sources have described it as a transudate. This discrepancy may arise from differences in diagnostic criteria or the methods used to analyze the fluid. However, the most recent and comprehensive evidence supports the classification of the pleural effusion in dengue fever as an exudate. [2,3]

*References*
[1] Paul R, Sinha A. Pleural effusion in Dengue fever: a case report. Asian J Pharm Health Sci. 2014;4(1):893-894.
[2] Shabbir M, Ameen F, Roshan N, Israr M. Nature and clinical course of pleural effusion in dengue fever. Int J Intern Emerg Med. 2018;1(1):1006. (via ResearchGate)
[3] Khurram M, Qayyum W, Umar M, Jawad M, Mumtaz S, Bushra Khaar HT. Ultrasonographic pattern of plasma leak in dengue haemorrhagic fever. J Pak Med Assoc. 2016;66(3):260-264.
[4] Reyna R. Imaging in Dengue Fever. In: Sperança MA, ed. Dengue Fever in a One Health Perspective: Latest Research and Recent Advances. IntechOpen; 2023. doi:10.5772/intechopen.109858
[5] Fotedar S, Singh J, Garg A, Chinu M, Chaudhary V, Gaur V. Pulmonary manifestations of dengue fever at a tertiary care centre in northern India: a cross-sectional study. J Clin Diagn Res. 2023. doi:10.7860/JCDR/2023/63382.18343
[6] Causes of transudative pleural effusions [image]. UpToDate. https://sjr.uptodate.com/contents/image?imageKey=PULM/73530. 
[7] Dengue. WikEM. https://www.wikem.org/w/index.php?title=Dengue&direction=next&oldid=374025. 
[8] Khor BS, Liu JW, Lee IK, Yang KD. Dengue hemorrhagic fever patients with acute abdomen: clinical experience of 14 cases. Am J Trop Med Hyg. 2006;74(5):901.
[9] Soni A, Chugh K, Sachdev A, Gupta D. Management of dengue fever in ICU. Indian J Pediatr. 2001;68(11):1051-1055.
[10] Pleural effusion differential diagnosis. WikiDoc. https://www.wikidoc.org/index.php?title=Pleural_effusion_differential_diagnosis&oldid=1642246.
[11] 세균맨. Transudative와 exudative pleural effusions [Transudative and exudative pleural effusions, translated from Korean]. Internal Medicine Since 2012. 세균맨 [blog]. Published January 1, 2020. https://tistorysjloveu2.tistory.com/1569?category=762160

**Gemini**
Pleural effusion in dengue fever is exudative in nature.

*Why it is an Exudate*
In dengue fever—particularly during the critical phase of Dengue Hemorrhagic Fever (DHF) or Severe Dengue—the virus triggers an intense immune response. This leads to a massive release of cytokines (sometimes called a "cytokine storm"), which directly causes acute hyperpermeability of the vascular endothelium (capillary leakage).

Because the capillary "gates" open up, the fluid that escapes into the pleural space isn't just water; it is highly rich in proteins, albumin, and cellular components.
•	Transudates occur when systemic mechanical pressures change (like increased hydrostatic pressure in heart failure, or decreased oncotic pressure in severe cirrhosis), pushing mostly low-protein fluid out of intact vessels.
•	Exudates occur when local or systemic inflammatory processes alter the structural integrity of the blood vessels, letting large proteins and fluids leak out.

*Fluid Analysis Profile*
When clinical studies have tapped and analyzed the pleural fluid in dengue patients using Light's Criteria, the findings consistently reveal:
•	High Protein Content: Usually well above 3.0g/dL (often averaging between 3.5g/dL and 3.9g/dL). [1]
•	Pleural to Serum Protein Ratio: Greater than 0.5. 
•	Pleural to Serum LDH Ratio: Greater than 0.6. 

*Clinical Relevance*
Even though it has an inflammatory, exudative profile, the pleural effusion in dengue is typically benign and self-resolving. [1]

As the patient moves into the recovery phase (usually 24 to 48 hours after the fever drops), the capillary permeability normalizes, and the lymphatic system completely reabsorbs the extravasated fluid. Therapeutic pleural taps are rarely needed unless the effusion is massive enough to cause severe respiratory distress.

*References*
[1] Shabbir M, Ameen F, Roshan N, Israr M. Nature and clinical course of pleural effusion in dengue fever. *Int J Intern Emerg Med.* 2018;1(1):1006. (via ResearchGate)
 
