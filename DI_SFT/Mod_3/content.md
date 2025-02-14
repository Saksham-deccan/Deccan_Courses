# Crafting Complex and Effective Prompts

Writing effective prompts is key to challenging AI models to deeply analyse and accurately interpret visual data, avoiding simplistic responses. This section covers prompt types, areas where models may struggle, examples, and the components of a strong prompt.

## Types of Prompts

<img height="329" width="602" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeWnwQ61OQWkO6kXss1YCtS3Y2mPvQ1S0aXSI8maoQ-DSmjTva6oCPzIrrYVJ6SaonQekvhlzGFVUFdwbvOBEYcNCZ3ybD-CwgZjak93hA5FTJo3r2D5i_j3NXfy1h17BMg43dt?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

### <span style="color:#364BC9">1. Contextual Prompts:</span>&#x20;

* Questions where the image data provides a clear answer, allowing the model to respond confidently. 
* Example, "***What was the GDP growth in 2015?*** " can be directly answered using the chart. 

### <span style="color:#364BC9">2. Semi-Contextual Prompts:</span>

* These questions cannot be fully answered with the image alone and highlight missing information. &#x20;
* The model must describe the image details, clarify the limitations, and provide educated guesses or possible explanations, stating assumptions clearly.
* "***List each major event between 2012 and 2019 that could have impacted the GDP growth, and indicate whether any of these coincided with significant global events***." Now, this requires the AI to link the data with external factors, not just what's shown in the chart.&#x20;

***

## What makes an effective data interpretation prompt?

<img height="550" width="670" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc7JLTSBFmNO7rEDfhC-4KiFqRxhwQVyiPaOF30kRCf0bC7Z_sB40sjrbT-nUn2KZ1ZZ6kCk4guMpLpYsIHBH3PWM1Lm97BJpNPEv0QgMDrIKRV-JLYiQzDZDO_9RylkQDlugx7Xg?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

### <span style="color:#364BC9">1.  Relevance</span>

* The prompt must be directly related to the content of the image. 
* It should focus on information or analysis that is specific to what is depicted in the image, ensuring that the question can only be answered by referring to the image. 

**Good Prompt**:&#x20;

:::info
Examine the visual data provided, identify any intoxicants that are present and do not result in drug-related mortality. Then, organise your findings into a table format, specifying the name of each intoxicant and its categorisation.
:::

**Why it's good?**

The prompt directly engages with the image, asking the AI to analyse and interpret specific details related to the intoxicants depicted in the image.

**Bad Prompt:**&#x20;

:::danger
List all the intoxicants that do not cause drug-related deaths based on toxicity level and display them in a table.
:::

**Why it's bad?**

This prompt doesn't require the model to engage with the image itself and instead allows the model to pull from general knowledge, which isn’t effective for visual data interpretation training.

***

### <span style="color:#364BC9">2.  Clarity</span>

* The prompt should be clear and easy to understand, with no ambiguity. 
* It must clearly outline what information is required, making the objective of the question explicit to the reader.

**Good Prompt**:&#x20;

:::info
Analyse the historical data from 1933 to 2023 and identify the years when the federal debt was equal to or exceeded the GDP. For each of these years, calculate the federal debt amount in USD and the total GDP, then present your findings in a table with columns for 'Year,'  'Federal Debt (USD),' and 'Total GDP (USD).
:::

**Why it's good?**

The prompt specifies the exact data range, the calculations needed, and how the results should be structured, ensuring clarity. 

**Bad Prompt:**&#x20;

:::danger
Check when the debt was higher than GDP and show it in a table.
:::

**Why it's bad?**

The prompt lacks specific instructions on the time frame, what calculations are required, and how the information should be presented, making it too vague for effective analysis.

***

### <span style="color:#364BC9">3.  Advanced Reasoning</span>

* The prompt should require advanced reasoning, such as making inferences, drawing conclusions, or analyzing relationships within the image. 
*  It should not be a basic observation or a simple request for information but should challenge the reader to think critically about the image's content.

**Good Prompt**:&#x20;

:::info
Identify the top three browser families by page views in August 2016. Calculate the percentage of the global population that used each specific browser, assuming one page view per person.
:::

**Why it's good?**

The prompt requires the AI to interpret data, perform calculations, and connect browser usage with the global population—a task that requires advanced reasoning beyond simple observation.

**Bad Prompt:**&#x20;

:::danger
Show the top browsers by page views for 2016 and estimate how many people use each.
:::

**Why it's bad?**

This prompt is too simple and does not specify how the AI should make the connection between browser page views and the global population, making it insufficiently challenging.

***

### <span style="color:#364BC9">4.  Length and Detail</span>

* The prompt should be detailed and longer than 25 words, providing enough context to fully specify the required analysis or information. 
*  It should set up a scenario or question that makes the focus and scope clear. 

**Good Prompt**:&#x20;

:::info
From 1980 to 2020 which year had the highest and lowest gender gap in life expectancy at birth, provide the data in a table along with life expectancy of both genders and the total  population of Germany in that year.
:::

**Why it's good?**

The prompt is sufficiently long and complex, requiring the model to extract and compare multiple data points, perform calculations (gender gap), and present information in a detailed table.

**Bad Prompt:**&#x20;

:::danger
Find the highest and lowest gender gap in life expectancy and list the population.
:::

**Why it's bad?**

This prompt is too brief and lacks the necessary complexity. It does not provide enough detail for the model to engage in multi-step processing or present data systematically.

***

### <span style="color:#364BC9">5.  Challenge Points</span>

* Identify areas where the model may struggle (e.g., approximations, external factors) to ensure it is adequately challenged.

**Good Prompt**:&#x20;

:::info
Calculate the percentage decrease for three countries that showed the most significant reduction in road accident deaths between 2000-2010. Then, propose three potential factors that could have contributed to this reduction. Present your findings in a table format.
:::

**Why it's good?**

The prompt is structured to challenge the AI, requiring it to analyse data over a timeline, perform calculations, and contextualise the findings with relevant explanations—testing both data handling and reasoning capabilities.

**Bad Prompt:**&#x20;

:::danger
List countries with the biggest drop in road accidents and explain why.
:::

**Why it's bad?**

This version doesn’t provide enough structure or challenge points. It does not specify the period or require percentage calculations, and it’s too open-ended, which reduces the model's opportunity to demonstrate advanced analytical skills.

***

## Teaching LLMs Image Analysis: Overcoming Key Challenges with Effective Prompts

**AI models may struggle with certain aspects of image analysis:**

* **Visual Approximations**: When exact values are not labeled, models might have to approximate (e.g., estimating a bar's position between two y-axis marks).
* **Multi-step Reasoning**: Combining multiple data points or performing complex calculations can be challenging. Prompts should guide the model to reason step by step.
* **Comparisons**: Comparing trends over different periods or categories requires deep understanding, which can be difficult for models.
* **External Factors**: When prompts involve factors not shown in the image (e.g., political or global events), models may invent information. Prompts should guide models to acknowledge when information is insufficient.

***

## Prompt Example: Contextual

<img height="699" width="699" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdh_quPKpb9piQOoeFdqrm46jX06JlupnZjUe-rPDq8BU68IrfXShEPLplu5kAoqcLuu7AsovmDFX2NUYdT-l0V7vn_BHTIkgn8MzDf2pRYorVuWnsYAjvX6g9q_mKFdTKsSBUD7g?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

:::note
Identify the intoxicants in the given image that do not lead to 'drug-related mortality.' Present the findings in a table.
:::

### Why is this a good prompt?

* The user is asking specifically for intoxicants that do \_not\_ contribute to “drug-related mortality,” which means filtering out substances that do not have the corresponding color segment (associated with drug-related mortality) in the stacked bar chart.
* The model must extract each intoxicant from the chart and analyse whether the corresponding bar contains the color that signifies “drug-related mortality.” This requires structured visual parsing.&#x20;

***

## Prompt Example: Semi-Contextual

<img height="642" width="642" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc9yuhpeMTPNc8ej58k7a9wqVlnXcD6axByN0RVh2HaQ8M3xNkVCGoJ_TILP7yAWyIpI0zo38g1pWUhyILHjE_RYgXG90TNgI5MjADq7-ZE6u4o5I4yUJgkz-cf_ktsJj11LMjmmg?key=YaA7O7hAZEQAu4dYSRxJ8o4v" />

:::note
List each major event, along with the year it occurred and the corresponding dust concentrations, that took place between the first appearance of black band disease and the recorded seagrass death. Additionally, indicate whether any of these events coincided with significant climatic events?
:::

### Why is this a good prompt?

* The prompt requires identification of a time period : This requires locating both events on the timeline and extracting only the relevant occurrences in between.
* &#x20;It requires interpreting spatial relationships in images.
* The prompt asks if any of the extracted events coincided with significant climatic events. This requires recognising references to “major El Niño” which is not explicitly mentioned anywhere in the image. 

***

## Summary of a Good Prompt:

:::caution
* It is clear, detailed, and specific to the image.
* It challenges the model to think through the data, encouraging advanced reasoning and multi-step processes.
* It avoids surface-level questions and asks for deeper analysis or insight that would be difficult to provide without the image.
* It contains enough complexity that the model has to consider trends, calculations, or missing data to provide a meaningful response.

By designing prompts with these components in mind, you’ll help train AI models to better interpret complex visual data, make informed inferences, and reason through challenging scenarios.
:::