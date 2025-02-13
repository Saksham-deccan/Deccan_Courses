# Getting Better Responses from LLMs with Prompting Techniques

Think of prompting as giving instructions. If one way doesn’t work, you try another—just like explaining directions to a friend using landmarks or a map.&#x20;

Language models work similarly! Different tasks need different prompting techniques to get the best results.  Sometimes, showing examples (**Few-Shot**) helps. For more complex reasoning, breaking down tasks step-by-step (**Chain-of-Thought**) or exploring multiple possibilities (**Tree-of-Thought**) works better.&#x20;

:::tip
We’ll look at the three methods mentioned here. Learning these techniques is like adding tools to your problem-solving toolbox!&#x20;
:::

<img height="160" width="602" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXexvy8vpjo7Xx9Nvt6kWUOc10LGU_dwzjoauvSvc2zaIR6dlLWcGBg4xxtGrLnrKG7Jl8KveFD3Su9kPCEE4syx3Xx12mve3VQPnjYpadClNRb--Qb_nrfg1UP6_hTAnBzSyv8GdA?key=knaq4zjgrnXCUPImADjMOLLn" />

## <span style="color:#364BC9">Few-Shot Prompting</span>

Imagine learning a new card game. If someone explains the rules with just a few example rounds, you quickly pick up the gameplay and can play on your own. This is how Few-Shot Prompting works for language models. You show the model a few examples, and it learns the pattern to respond correctly.&#x20;

**Why Few-Shot Prompting Works:**

* <u>Clear Guidance</u>: Learning from examples reduce ambiguity and set clear expectations.
* <u>Better Answers</u>: With a few examples, the model understands the task and produces more accurate responses.&#x20;

:::caution
**🪜 Steps to Few Shot Prompting:**&#x20;

* Provide sample Q\&A with correct answers to set a pattern.
* After seeing a few examples, the model applies the pattern to new prompts-even if the exact answer wasn’t shown earlier.
:::

**Example:**&#x20;

> ❌ Classify the following product review: "The battery life is great, but the camera quality could be better." as Positive/Neutral/Negative. &#x20;

<img height="394" width="742" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeHUOjwIUZnr8oZKkI1nkP9uaEQrfe_eq4uivIVnrSaCDq5XtVpdQ3GeZ5idii8xCSi6zj5wzxQ14w81zVxdjWtAZaZ90zAHL1MaknLs2VKNADdw_sYyXRjY1O6064mwpYqsXuB?key=knaq4zjgrnXCUPImADjMOLLn" />

***

## <span style="color:#364BC9">Chain-of-Thought Prompting</span>

Ever solved a puzzle by breaking it into smaller pieces? That’s exactly how Chain-of-Thought (CoT) prompting works. 

Instead of jumping straight to the answer, a CoT prompt explicitly asks the model to think through a problem step-by-step before arriving at a final conclusion. This makes it perfect for tasks involving reasoning, logic, or multi-step calculations.&#x20;

**Why Use Chain-of-Thought Prompting?**

* <u>Structured Thinking</u>: Helps the model logically process information.
* <u>Clear Explanations:</u> Produces more transparent and understandable responses.

:::caution
**🪜 Steps to Chain of Thought Prompting:**

1. **Define the problem**: Clearly state the problem for the model.
2. **Instruct the model to think step-by-step**: Use phrases like "*Let’s think step by step*" or "*Break this down*" to guide the model through the reasoning process.
3. **Present the solution**: Once the steps are logically followed, ask the model to provide the final answer.&#x20;
:::

**Example:**

> ❌  What is the theme of "Moby Dick"?

<img height="428" width="796" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXebinKbi3zvlIGmsRnczppv8cmNPSDK6CDw94OWYJk_pEO1HoDVe9it1DKejOh3ZGp-J6es9IRZcKpx5kDGlR6yL8curr4X5J4DMlgKz3RX0NtSkV3roXCg0pikYHsiprc1xs8V?key=knaq4zjgrnXCUPImADjMOLLn" />

***

## <span style="color:#364BC9">Tree-of-Thought Prompting</span>

Imagine brainstorming every possible solution before making a decision. That’s what Tree-of-Thought prompting helps models do.  Instead of sticking to one answer, the model generates multiple thought paths, explores different solutions, and backtracks when needed to find the best response. With ToT prompting, models become strategic thinkers, exploring creative and logical solutions like a master problem-solver!&#x20;

**Why Use Tree-of-Thought Prompting?**

* <u>Diverse Solutions</u>: Models are trained to explore many possibilities, not just one.
* <u>Reduced Errors</u>: Backtracking allows fixing mistakes along the way.
* <u>Complex Problem Solving</u>: Ideal for deep reasoning and multi-step decision-making tasks.

:::caution
🪜 **Steps to Tree-of-Thought Prompting:**

1. **Thought Decomposition**: Break the task into smaller parts.
2. **Thought Generation**: Encourage multiple ideas at each step.
3. **State Evaluation**: Ask the model to evaluate and refine its choices.
:::

**Example:**&#x20;

> ❌  What are some ways to increase website traffic?

<img height="435" width="811" src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcj0MKbUUpv15PHqncuBMRPwFqTuQcPcukxGiX98rzPt1mKzn_YVPymnumEbmhU6UO3HKuAu-qfmvzSHu3z5I7JzADS3IMKK2VVnFK17fZ6MNXx4l4mdzo0EPmcGujb6nzGygEdAg?key=knaq4zjgrnXCUPImADjMOLLn" />