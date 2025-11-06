---

title: "CARE: Collaborative AI-Assisted Reading Environment"

source: 2023.acl-demo.28v2-1.pdf

layout: "single-column"

note: "Extracted automatically; text preserved 1-to-1 except de-hyphenation across line breaks."

---

# Ubiquitous Knowledge Processing Lab (UKP Lab)

### Authors & Affiliations

Department of Computer Science and Hessian Center for AI (hessian.AI)
Technical University of Darmstadt
ukp.informatik.tu-darmstadt.de

### Abstract

Recent years have seen impressive progress in
AI-assisted writing, yet the developments in
AI-assisted reading are lacking. We propose
inline commentary as a natural vehicle for AIbased reading assistance, and present CARE:
the first open integrated platform for the study
of inline commentary and reading. CARE facilitates data collection for inline commentaries in
a commonplace collaborative reading environment, and provides a framework for enhancing
reading with NLP-based assistance, such as text
classification, generation or question answering. The extensible behavioral logging allows
unique insights into the reading and commenting behavior, and flexible configuration makes
the platform easy to deploy in new scenarios.
To evaluate CARE in action, we apply the platform in a user study dedicated to scholarly peer
review. CARE facilitates the data collection
and study of inline commentary in NLP, extrinsic evaluation of NLP assistance, and application prototyping. We invite the community to
explore and build upon the open source implementation of CARE1.
### 1 Introduction
Individual and collaborative text work is at the
core of many human activities, including education,
business, and research. Yet, reading text is difficult
and takes considerable effort, especially for long
and domain specific texts that require expert knowledge. While past years have seen great progress
in analyzing and generating text with the help of
AI – culminating in strong generative models like
GPT-3 (Brown et al., 2020) and ChatGPT (Ouyang
et al., 2022)2 – the progress in applications of AI to
reading and collaborative text work is yet to match
these achievements. The ability of modern generative models to create natural-sounding but factually


*These authors contributed equally to this work
1 https://github.com/UKPLab/CARE
2 https://openai.com/blog/chatgpt


Figure 1: CARE allows users to collaboratively read and
discuss texts, provides a generic interface for AI-based
reading assistance, and collects research-ready textual
and behavioral data.
flawed outputs (Ji et al., 2022) stresses the need for
supporting humans in critical text assessment.
Humans use annotations to read and collaborate over text, from hand-written print-out notes to
highlights in collaborative writing platforms. This
makes in-text annotations – inline commentaries
– a promising vehicle for AI-based reading assistance. For example, an AI assistant could automatically classify the user’s commentaries, or verify
and provide additional information on the highlighted passages. Yet, the lack of data and key insights limits the NLP progress in this area: from the
foundational perspective, we lack knowledge about
the language of inline commentaries, as most of
this data is not openly available for research. From
the applied perspective, little is known about the
hands-on interactions between humans and texts,
how they translate into NLP tasks, and how the
impact of NLP-based assistance on text comprehension can be measured. While ethical, controlled
data collection has been receiving increasing attention in the past years (Stangier et al., 2022), data
collection tools for inline commentary are missing,
and so are the tools for applying and evaluating
NLP models within a natural reading environment.
To address these limitations, we introduce


---

#### Page 1

CARE: Collaborative AI-Assisted Reading Environment
Dennis Zyska∗, Nils Dycke∗, Jan Buchmann, Ilia Kuznetsov, Iryna Gurevych
Ubiquitous Knowledge Processing Lab (UKP Lab)
Department of Computer Science and Hessian Center for AI (hessian.AI)
Technical University of Darmstadt
ukp.informatik.tu-darmstadt.de
Abstract
Recent years have seen impressive progress in
AI-assisted writing, yet the developments in
AI-assisted reading are lacking. We propose
inline commentary as a natural vehicle for AIbased reading assistance, and present CARE:
the first open integrated platform for the study
of inline commentary and reading. CARE facilitates data collection for inline commentaries in
a commonplace collaborative reading environment, and provides a framework for enhancing
reading with NLP-based assistance, such as text
classification, generation or question answering. The extensible behavioral logging allows
unique insights into the reading and commenting behavior, and flexible configuration makes
the platform easy to deploy in new scenarios.
To evaluate CARE in action, we apply the platform in a user study dedicated to scholarly peer
review. CARE facilitates the data collection
and study of inline commentary in NLP, extrinsic evaluation of NLP assistance, and application prototyping. We invite the community to
explore and build upon the open source implementation of CARE1.
1
Introduction
Individual and collaborative text work is at the
core of many human activities, including education,
business, and research. Yet, reading text is difficult
and takes considerable effort, especially for long
and domain specific texts that require expert knowledge. While past years have seen great progress
in analyzing and generating text with the help of
AI – culminating in strong generative models like
GPT-3 (Brown et al., 2020) and ChatGPT (Ouyang
et al., 2022)2 – the progress in applications of AI to
reading and collaborative text work is yet to match
these achievements. The ability of modern generative models to create natural-sounding but factually
*These authors contributed equally to this work
1https://github.com/UKPLab/CARE
2https://openai.com/blog/chatgpt

**Figure (from PDF):**
Figure 1: CARE allows users to collaboratively read and
discuss texts, provides a generic interface for AI-based
reading assistance, and collects research-ready textual
and behavioral data.
flawed outputs (Ji et al., 2022) stresses the need for
supporting humans in critical text assessment.
Humans use annotations to read and collaborate over text, from hand-written print-out notes to
highlights in collaborative writing platforms. This
makes in-text annotations – inline commentaries
– a promising vehicle for AI-based reading assistance. For example, an AI assistant could automatically classify the user’s commentaries, or verify
and provide additional information on the highlighted passages. Yet, the lack of data and key insights limits the NLP progress in this area: from the
foundational perspective, we lack knowledge about
the language of inline commentaries, as most of
this data is not openly available for research. From
the applied perspective, little is known about the
hands-on interactions between humans and texts,
how they translate into NLP tasks, and how the
impact of NLP-based assistance on text comprehension can be measured. While ethical, controlled
data collection has been receiving increasing attention in the past years (Stangier et al., 2022), data
collection tools for inline commentary are missing,
and so are the tools for applying and evaluating
NLP models within a natural reading environment.
To address these limitations, we introduce
CARE: a Collaborative AI-Assisted Reading
Environment, where users can jointly produce in