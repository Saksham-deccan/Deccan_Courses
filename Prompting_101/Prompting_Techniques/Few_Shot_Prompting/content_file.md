## Few-Shot Prompting

Imagine learning a new card game. If someone explains the rules with just a few example rounds, you quickly pick up the gameplay and can play on your own.

This is how **Few-Shot Prompting** works for language models. You show the model a few examples, and it learns the pattern to respond correctly.

> ###  Why Few-Shot Prompting Works:
>
> - **Clear Guidance:** Learning from examples reduces ambiguity and sets clear expectations.  
> - **Better Answers:** With a few examples, the model understands the task and produces more accurate responses.  

---

### ✅ Steps to Few-Shot Prompting:

1. Provide sample Q&A with correct answers to set a pattern.  
2. After seeing a few examples, the model applies the pattern to new prompts—even if the exact answer wasn’t shown earlier.  

---

### Example:

```plaintext
❌ Classify the following product review:  
   "The battery life is great, but the camera quality could be better."  
   as Positive/Neutral/Negative.  