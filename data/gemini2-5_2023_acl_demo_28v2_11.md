
---

[cite_start]**CARE: Collaborative AI-Assisted Reading Environment** [cite: 50]

[cite_start]Dennis Zyska\*, Nils Dycke\*, Jan Buchmann, Ilia Kuznetsov, Iryna Gurevych [cite: 51]
[cite_start]Ubiquitous Knowledge Processing Lab (UKP Lab) [cite: 51]
[cite_start]Department of Computer Science and Hessian Center for AI (hessian.AI) [cite: 52]
[cite_start]Technical University of Darmstadt [cite: 53]
[cite_start]ukp.informatik.tu-darmstadt.de [cite: 53]

[cite_start]**Abstract** [cite: 54]

[cite_start]Recent years have seen impressive progress in Al-assisted writing, yet the developments in Al-assisted reading are lacking. [cite: 55] [cite_start]We propose inline commentary as a natural vehicle for AI- based reading assistance, and present CARE: the first open integrated platform for the study of inline commentary and reading. [cite: 56] [cite_start]CARE facilitates data collection for inline commentaries in a commonplace collaborative reading environ- ment, and provides a framework for enhancing reading with NLP-based assistance, such as text classification, generation or question answer- ing. [cite: 57] [cite_start]The extensible behavioral logging allows unique insights into the reading and comment- ing behavior, and flexible configuration makes the platform easy to deploy in new scenarios. [cite: 58] [cite_start]To evaluate CARE in action, we apply the plat- form in a user study dedicated to scholarly peer review. [cite: 59] [cite_start]CARE facilitates the data collection and study of inline commentary in NLP, extrin- sic evaluation of NLP assistance, and applica- tion prototyping. [cite: 60] [cite_start]We invite the community to explore and build upon the open source imple- mentation of CARE¹. [cite: 61]

[cite_start]**1 Introduction** [cite: 62]

[cite_start]Individual and collaborative text work is at the core of many human activities, including education, business, and research. [cite: 63] [cite_start]Yet, reading text is difficult and takes considerable effort, especially for long and domain specific texts that require expert knowl- edge. [cite: 64] [cite_start]While past years have seen great progress in analyzing and generating text with the help of AI - culminating in strong generative models like GPT-3 (Brown et al., 2020) and ChatGPT (Ouyang et al., $2022)^{2}$ - the progress in applications of Al to reading and collaborative text work is yet to match these achievements. [cite: 65] [cite_start]The ability of modern genera- tive models to create natural-sounding but factually flawed outputs (Ji et al., 2022) stresses the need for supporting humans in critical text assessment. [cite: 75]

[cite_start]Humans use annotations to read and collabo- rate over text, from hand-written print-out notes to highlights in collaborative writing platforms. [cite: 76] [cite_start]This makes in-text annotations a promising vehicle for AI-based reading assis- tance. [cite: 77, 78] [cite_start]For example, an Al assistant could automat- ically classify the user's commentaries, or verify and provide additional information on the high- lighted passages. [cite: 78] [cite_start]Yet, the lack of data and key in- sights limits the NLP progress in this area: from the foundational perspective, we lack knowledge about the language of inline commentaries, as most of this data is not openly available for research. [cite: 79] [cite_start]From the applied perspective, little is known about the hands-on interactions between humans and texts, how they translate into NLP tasks, and how the impact of NLP-based assistance on text compre- hension can be measured. [cite: 80] [cite_start]While ethical, controlled data collection has been receiving increasing atten- tion in the past years (Stangier et al., 2022), data collection tools for inline commentary are missing, and so are the tools for applying and evaluating NLP models within a natural reading environment. [cite: 81]

[cite_start]To address these limitations, we introduce CARE: a Collaborative Al-Assisted Reading Environment, where users can jointly produce in- [cite: 82]

---
[cite_start]\*These authors contributed equally to this work [cite: 67]
[cite_start]¹[https://github.com/UKPLab/CARE](https://github.com/UKPLab/CARE) [cite: 67]
[cite_start]²[https://openai.com/blog/chatgpt](https://openai.com/blog/chatgpt) [cite: 67]
