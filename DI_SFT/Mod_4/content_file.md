# Writing Effective DI Responses

Crafting effective responses to prompts requires a structured approach that ensures clarity, accuracy, and thorough reasoning. A well-written response enables the AI model to understand the logic behind the answer and learn how to reason through data in a similar fashion.

## Rubric for Responses

### <span style="color:#364BC9">Completeness</span>

* The response should fully address all aspects of the prompt, ensuring no part of the question is overlooked.&#x20;
* It should provide a thorough explanation that leaves no gaps or unanswered elements.

### <span style="color:#364BC9">Clarity</span>

* The response must be straightforward and easy to follow, with no ambiguity.&#x20;
* It should clearly present information and conclusions derived from the image, making the interpretation accessible and understandable.

### <span style="color:#364BC9">Accuracy</span>

* The response must be precise, using evidence directly from the image to support any claims, conclusions, or calculations.&#x20;
* No fabricated details or assumptions that cannot be supported by the image should be included.

### <span style="color:#364BC9">Formatting (Markdown)</span>

* The response should be well-structured using markdown formatting for readability.&#x20;
* This includes using headers, bullet points, or numbered lists as needed to organize the information clearly and professionally.

### <span style="color:#364BC9">Grammar</span>

* The response should be grammatically correct, free from spelling or syntactical errors.&#x20;
* It must present the information in a polished and professional manner, ensuring that it is easy to read and comprehend.&#x20;

***

## Writing Responses to a Contextual Prompt 

<img height="686" width="686" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdh_quPKpb9piQOoeFdqrm46jX06JlupnZjUe-rPDq8BU68IrfXShEPLplu5kAoqcLuu7AsovmDFX2NUYdT-l0V7vn_BHTIkgn8MzDf2pRYorVuWnsYAjvX6g9q_mKFdTKsSBUD7g?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

:::note
Identify the intoxicants in the given image that do not lead to 'drug-related mortality.' Present the findings in a table.
:::

**Observation:**&#x20;

The provided image visually represents various intoxicants, each showing segments that correspond to "drug-related mortality." This is marked with a particular colour (a shade of magenta-pink). By examining the chart, we can identify which intoxicants have this "drug-related mortality" segment and which do not. Based on a **visual approximation**, two intoxicants appear not to have any drug-related mortality segment. &#x20;

**Explanation:**&#x20;

To determine which intoxicants do not lead to drug-related mortality, we must cross-check the colored segments corresponding to each intoxicant in the image. All intoxicants with the magenta-pink segment are associated with drug-related mortality, while those without it are not. Based on this observation, **LSD** and **Mushrooms** are the only intoxicants that do not show this segment.

### **Response**

(In Markdown)

:::info
\`\`\`

"To find which intoxicant doesn't have a drug related morality rating 

in the provided image, we have to look at the segments in the bars with respect to 'Drug-related mortality (6.4)' this is represented by a shade 

of color (shade of magenta-pink)



\*\*Note\*\*: The values presented are based on visual approximation.



\*\*Let's visualize the list of Intoxicants:\*\*



First, we must identify intoxicants that cause both 

'drug-related mortality' and those that do not.




|\*\*List of Intoxicants\*\*|\*\*Drug-related mortality Segment\*\*| 

\|:---:|:---:|

\| Alcohol | Yes | 

\| Heroin |Yes | 

\| Crack Cocaine |Yes |

\| Methylamphetamine |Yes |

\| Cocaine |Yes|

\| Tobacco |Yes|

\| Amphetamine |Yes|

\| Cannabis |Yes|

\| GHB |Yes|

\| Benzodiazepines |Yes|

\| Ketamine |Yes|

\| Methadone |Yes|

\| Mephedrone |Yes|

\| Butane |Yes|

\| Anabolic Steroids |Yes|

\| Ecstasy |Yes|

\| Qat/Khat |Yes |

\| LSD |No |

\| Buprenorphine |Yes|

\| Mushrooms |No|



From the Observation it seems that \*\*LSD\*\* and \*\*Mushrooms\*\* 

are the intoxicants that don't have Drug-related a mortality.



\*\*Medicinal drug that can cause drug-related mortality\*\*



\- Methadone, although used to treat substance abuse and chronic pain, 

can cause drug-related mortality if overdosed since it impairs

respiratory function. 



\- Misuse or incorrect dosage, particularly in people with no 

opioid tolerance, raises the risk of fatal respiratory depression."

\`\`\`
:::

***

## Writing Responses to a Semi-Contextual Prompt 

<img height="656" width="656" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXf9eInU-gzRagq8qlliHdqUpYCavCDMefR1uDOZ2LrBpeTMsnk73knqgToifi4EEfF_w3WOdS2PQhHVkFGa0eX90HzqklzUddOmzXCEiYrz_nAMeSn9HC663l1XNlDBXGQxxgSd?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

:::note
List each major event, along with the year it occurred and the corresponding dust concentrations, that took place between the first appearance of black band disease and the recorded seagrass death. Additionally, indicate whether any of these events coincided with significant climatic events?
:::

**Observation:**

The chart shows key events in the aquatic ecosystem, such as coral die-offs, the appearance of black band coral disease, and seagrass deaths, along with dust concentrations (measured in µg/m³) over the years from 1965 to 1995. Notable dust concentrations range from around 8 µg/m³ to 16 µg/m³, and several of these events coincide with major climatic occurrences, like El Niño.

**Explanation:**

Between the first appearance of black band coral disease in 1973 and the recorded seagrass death in Florida in 1987, the ecosystem experienced multiple significant changes. These changes are associated with fluctuating dust concentrations, with higher dust levels correlating with more severe ecological impacts. For instance, in 1982, both coral death and the mass die-off of the sea urchin Diadema Antillarum across the Caribbean occurred, coinciding with a 15 µg/m³ dust concentration and a major El Niño event. Similarly, in 1987, black band disease became rampant in Florida, alongside coral bleaching, at a dust concentration of 16 µg/m³, also during an El Niño year.

### Response

(In Markdown)

:::info
\`\`\`

Here’s a summary of the major events between the first records 

of black band disease and the first recorded sea grass death, 

along with the corresponding dust concentrations and any 

associated climatic events:



1.  \*\*First Appearance of Black Band Coral Disease\*\*

    -   \*\*Year:\*\* 1973

    -   \*\*Dust Concentration:\*\* \~13 µg/m³

    -   \*\*Climatic Event:\*\* Not explicitly mentioned.

2.  \*\*Staghorn and Elkhorn Corals Die in Florida\*\*

    -   \*\*Year:\*\* 1978

    -   \*\*Dust Concentration:\*\* \~8 µg/m³

    -   \*\*Climatic Event:\*\* Not explicitly mentioned.

3.  \*\*Staghorn and Elkhorn Corals Die in Jamaica\*\*

    -   \*\*Year:\*\* 1980

    -   \*\*Dust Concentration:\*\* \~10 µg/m³

    -   \*\*Climatic Event:\*\* Not explicitly mentioned.

4.  \*\*Staghorn and Elkhorn Corals Die Throughout the Caribbean 

(Major El Niño)\*\*

    -   \*\*Year:\*\* 1982

    -   \*\*Dust Concentration:\*\* \~15 µg/m³

    -   \*\*Climatic Event:\*\* Major El Niño.

5.  \*\*Sea Urchin Diadema antillarum, a Key Reef Herbivore, 

Dies Throughout the Caribbean (Major El Niño)\*\*

    -   \*\*Year:\*\* 1982

    -   \*\*Dust Concentration:\*\* \~15 µg/m³

    -   \*\*Climatic Event:\*\* Major El Niño.

6.  \*\*Black Band Disease Rampant in Florida; Corals Bleach 

throughout the Caribbean and Sea Grasses Die in Florida 

(Major El Niño)\*\*

    -   \*\*Year:\*\* 1987

&#x20;   \-   \*\*Dust Concentration:\*\* \~16 µg/m³

    -   \*\*Climatic Event:\*\* Major El Niño.



These events show a correlation between high dust concentrations 

and significant ecological impacts, with major climatic events such 

as El Niño coinciding with the most severe occurrences.

\`\`\`
:::