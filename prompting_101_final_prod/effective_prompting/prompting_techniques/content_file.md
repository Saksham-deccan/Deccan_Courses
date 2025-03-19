# Getting Better Responses from LLMs with Prompting Techniques

<video src="${PRIVATE_PROMPTING_101_VIDEO_3}" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; object-fit: cover;" controls="" controlslist="nodownload nofullscreen" style="width: 100%" />

Think of prompting as giving instructions. If one way doesn’t work, you try another—just like explaining directions to a friend using landmarks or a map. Language models work similarly. Different tasks need different prompting techniques to get the best results.

Sometimes, showing examples helps (**Few Shot method**). For more complex reasoning, breaking down tasks step-by-step (**Chain of Thought method**) or exploring multiple possibilities works better (**Tree of Thought method**).

In the next few sections we’ll look at the three methods mentioned here. Learning these techniques is like adding tools to your problem-solving toolbox.

<img height="300" width="800" src="${PRIVATE_PROMPTING_101_8}" />

## Few-Shot Prompting

Imagine learning a new card game. If someone explains the rules with just a few example rounds, you quickly pick up the gameplay and can play on your own.

This is how **Few-Shot Prompting** works for language models. You show the model a few examples, and it learns the pattern to respond correctly.

**Why Few-Shot Prompting Works:**

* **Clear Guidance:** Learning from examples reduces ambiguity and sets clear expectations.
* **Better Answers:** With a few examples, the model understands the task and produces more accurate responses.

#### <span style="color:#364BC9">✅ Steps to Few-Shot Prompting</span>

1. Provide sample Q\&A with correct answers to set a pattern.
2. After seeing a few examples, the model applies the pattern to new prompts—even if the exact answer wasn’t shown earlier.

### Example:

:::danger
❌  Classify the following product review:  "The battery life is great, but the camera quality could be better."  as Positive/Neutral/Negative.
:::

<img height="500" width="900" src="${PRIVATE_PROMPTING_101_9}" />

***

## Chain-of-Thought Prompting

Ever solved a puzzle by breaking it into smaller pieces? That’s exactly how **Chain-of-Thought (CoT) prompting** works. Instead of jumping straight to the answer, a CoT prompt explicitly asks the model to think through a problem step-by-step before arriving at a final conclusion. This makes it perfect for tasks involving reasoning, logic, or multi-step calculations.

**Why Use Chain-of-Thought Prompting?**

* **Structured Thinking:** Helps the model logically process information.
* **Better Accuracy:** Reduces errors in complex tasks by considering each detail.
* **Clear Explanations:** Produces more transparent and understandable responses.

#### <span style="color:#364BC9">✅ Steps to Chain-of-Thought Prompting:</span>

1. **Define the problem** – Clearly state the problem for the model.
2. **Instruct the model to think step-by-step** – Use phrases like *"Let’s think step by step"* or *"Break this down"* to guide the model through the reasoning process.
3. **Present the solution** – Once the steps are logically followed, ask the model to provide the final answer

### Example:

:::danger
❌  What is the theme of "Moby Dick"?
:::

<img height="500" width="900" src="${PRIVATE_PROMPTING_101_10}" />

***

## **Tree-of-Thought Prompting**

Imagine brainstorming every possible solution before making a decision. That’s what **\*\*Tree-of-Thought (ToT) prompting\*\*** helps models do. &#x20;

Instead of sticking to one answer, the model generates multiple thought paths, explores different solutions, and backtracks when needed to find the best response.  With ToT prompting, models become strategic thinkers, exploring creative and logical solutions like a master problem-solver!  &#x20;

**Why Use Tree-of-Thought Prompting?**

* **Diverse Solutions** – Models are trained to explore many possibilities, not just one.&#x20;
* **Reduced Errors** – Backtracking allows fixing mistakes along the way. &#x20;
* **Complex Problem Solving** – Ideal for deep reasoning and multi-step decision-making tasks.

#### <span style="color:#364BC9">✅  Steps to Tree-of-Thought Prompting:</span>

1. **Thought Decomposition** – Break the task into smaller parts. &#x20;
2. **Thought Generation** – Encourage multiple ideas at each step. &#x20;
3. **State Evaluation**– Ask the model to evaluate and refine its choices. &#x20;

### Example:

:::danger
❌  What are some ways to increase website traffic?
:::

<img height="500" width="900" src="${PRIVATE_PROMPTING_101_11}" />