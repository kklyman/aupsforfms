# In Brief: Methodology for Tagging Foundation Model Developers’ Acceptable Use Policies


Below is a brief writeup of the methodology for tagging acceptable use policies. This will be further detailed in a forthcoming paper.

#### Disclaimer
As stated in the [post](https://crfm.stanford.edu/2024/04/08/aups.html), this work is a preliminary analysis of companies’ acceptable use policies. It does not include every item from every company’s acceptable use policy, as the intention is to provide a useful aggregation of commonalities between company policies. This data ~should not~ be read to state that a company does not have rules relating to any one of these particular uses, just that its acceptable use policy as defined in the post does not explicitly prohibit that use per these tagging criteria. Please refer to the post (in particular its footnotes) for details on further caveats, including that (i) companies have broad prohibitions on various kinds of content, meaning that it is difficult to draw conclusions solely on the basis that a company does not include a certain prohibition verbatim and (ii) companies have many policies that contain use restrictions besides the acceptable use policies for their foundation models.

#### Process for identifying acceptable use policies
1. Compile a list of foundation model developers from Stanford Center for Research on Foundation Models’ [Ecosystem Graphs](https://crfm.stanford.edu/ecosystem-graphs/index.html?mode=table).
2. For each foundation model developer, check the developer’s terms of service on its website. If the terms of service includes an acceptable use policy with content restrictions that plausibly cover its foundation models, use this portion of the TOS as the acceptable use policy.[^1]
3. For each remaining foundation model developer, check the license for its [“flagship foundation model.”](https://arxiv.org/abs/2310.12941) If the license includes use restrictions or a reference to a version of the company’s acceptable use policy, use that portion of the license or the external document as the acceptable use policy.

#### Process for tagging acceptable use policies

* In the first round of tagging, for each line item in each acceptable use policy:
  * Tag each distinct prohibited use category 
  * Do not tag different types of actions related to prohibited use categories
  * Do not distinctly tag prohibited use categories with substantial overlap that do not use distinct phrasing
* This produced a list of prohibited use categories that is the union of prohibited use categories across all policies. In the second round of tagging, relabel each line item in each acceptable use policy in line with this larger set of prohibited uses. 
  * In general, each subcomponent of each line item should count only towards one category. 
  * The standard for this relabeling was typically a question of whether a line item includes the exact wording as the prohibited use category, though there were a handful of cases where it was reasonable to infer that marginally different terminology was allowable.
  * This process excluded:
    * Different formulations of restrictions on the same category of use (to avoid double counting and produce distinct categories to the extent possible)
    * Restrictions that do not fit well in this general framework (which is focused on prohibitions on generating violative outputs), are excessively vague (e.g. “dangerous,” “offensive”), or are in almost every case prohibited by some other policy for many companies (e.g. documentation, disclosing known limitations or risks). 
* In the third round of tagging, group categories of prohibited use together to provide structure for the analysis and combine categories where there is substantial overlap. Several examples of these combinations include:
  * Automated decision-making about housing, credit, financing, and employment are one category (automated decision-making in economic domains)
  * Child abuse includes child sexual exploitation
  * Political includes political manipulation

#### Categorizations for Figures 3-6

For Figure 3, the categories of violative use include the following line items:
1. Mis/disinformation, Misleading info: misinformation, false harmful info, misleading, disinformation
2. Harassment/Abuse: harassment, abuse
3. Harm to children, CSAM: harm to children, child sexual abuse material, grooming, pedophilia, child abuse
4. Privacy: privacy, violate third party privacy rights, extract private information, personal information
5. Discrimination: discrimination, classification of individuals
6. Violence: violence
7. Defamation: defamation, disparagement, libel, slander
8. Fraud/Spam: fraud, spam
9. Hate: hate, hate speech
10. Sexual/Pornographic: sexual, pornography, adult content
11. Impersonation: impersonation
12. Threats: threats
13. Malware/Malicious code: malware, malicious code
14. Terrorism/Violent Extremism: terrorism, violent extremism
15. Self-harm: self-harm, cutting, eating disorders, suicide

For Figures 4-6, the categories of violative use include the following line items:
1. Defamation: defamation, disparagement, libel, slander
2. Discrimination: discrimination, classification of individuals
3. Fraud/Spam: fraud, spam
4. Harassment/Abuse: harassment, abuse
5. Harm to children: CSAM: harm to children, child sexual abuse material, grooming, pedophilia, child abuse
6. Hate: hate, hate speech
7. Illegal: violating the law
8. Impersonation: impersonation
9. Malware: malware, malicious code
10. Mis/disinformation: misinformation, false harmful info, disinformation (note: this is different than above as it does not include misleading)
11. Political: influence political decisions, political campaigns, influencing elections, political advertisements/propaganda, influence political opinions, lobbying, political advocacy, discouraging voting
12. Privacy: privacy, violate third party privacy rights, extract private information, personal information
13. Self-harm: self-harm, cutting, eating disorders, suicide
14. Sexual/pornographic: sexual, pornography, adult content (note: this does not include illegal pornography, as that is narrow in comparison to the pornography category and is covered by the illegal category)
15. Terrorism: terrorism, violent extremism
16. Threats: threats
17. Violence: violence

[^1]: As discussed in the post, this resulted in Amazon and Mistral having two distinct but interrelated policies count as their acceptable use policy. 
