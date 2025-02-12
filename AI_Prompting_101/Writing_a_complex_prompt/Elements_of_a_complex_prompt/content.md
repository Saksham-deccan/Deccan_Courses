# Elements that Make a Prompt "Complex"

## 1. **Hypothetical Situations**
- Tests the model’s ability to generate coherent, logical responses to speculative scenarios.
- Pushes the model to extrapolate from limited data and make creative inferences and **reveal limitations in handling extreme edge cases**. 

### **Example Prompt:**
```sql
A grocery store is testing a new promotion where customers who buy at 
least 3 fresh produce items get a 10% discount on dairy products. 
Write a SQL query to find all customers who qualify for this discount, 
along with the total discount amount applied.
```

---

## 2. **Multi-Layered Reasoning**
- Challenges the model’s **logical consistency** and ability to **maintain context across layers**. 
- Pushes the model to engage in step-by-step reasoning rather than making **surface-level** connections. 

### **Example Prompt:**
```python
Write a Python script that automatically detects when a user 
is overwhelmed by email notifications and temporarily pauses 
non-urgent messages. Consider factors such as the number of 
emails received per hour, sentiment analysis of email content, and 
the user’s current calendar schedule. The script should resume 
emails once workload indicators decrease.
```

---

## 3. **Interdependent Variables**
- Assesses the model’s understanding of **complex, interlinked systems** and tests how well it **tracks changes** when one variable is modified. 
- Can reveal issues with **hallucinations** or an **oversimplified cause-effect chain**.

### **Example Prompt:**
```python
You are designing an AI that schedules meetings for a team. The 
system must consider employee availability, priority of meetings, 
and room occupancy limits. Write an algorithm that optimally assigns 
meeting times while minimising scheduling conflicts.
```

---

## 4. **Trade-Offs**
- Tests the model’s ability to **weigh competing priorities** and make a **justified decision**.
- Exposes biases in how it balances competing factors.

### **Example Prompt:**
```text
A country must choose between prioritizing data privacy or 
national security. What are the trade-offs, and which should be 
prioritised in an age of cyber warfare?
```

---

## 5. **Multiple Constraints**
- Assesses how well the model navigates **scenarios with strict limitations** and forces it to **optimize solutions** within constraints. 

### **Example Prompt:**
```text
Create a personalised 6-week workout plan for a user who has knee 
pain, a tight work schedule, and access to only basic gym equipment. 
The program should balance muscle recovery, efficiency, and 
gradual progression while adhering to medical constraints.
```

---

## 6. **Inter-Disciplinary Aspects**
- Challenges the model’s ability to **synthesize knowledge from different fields**. 
- Assesses how well it **balances expertise across multiple domains**. 

### **Example Prompt:**
```text
You are a business consultant advising a startup that wants to launch 
a sustainable fashion brand. Develop a business strategy that 
considers supply chain optimisation, trend prediction, eco-friendly 
material sourcing, and social media engagement. Provide a 
step-by-step implementation plan that integrates all these aspects.
```

---

# Areas to Test Model Performance In

### A Complex Prompt that Challenges **Instruction Following**: 
🔗 [Example](https://gemini.google.com/share/5ce12e54afa0)

### **Where Did the Model Go Wrong?**
- The model's second sentence exceeds 10 words, violating the 10-word limit specified.
- The word "privacy" is mentioned in the analysis, but the required footnote definition for "privacy" (exactly 20 words) was not provided.
- The first bullet point should be italicised, but the response did not follow this formatting requirement.
- The bullet points exceeded the 8-word limit for each point.

---

### A Complex Prompt that Challenges **Factuality**: 
🔗 [Example](https://gemini.google.com/share/2856a4d99629)

### **Where Did the Model Go Wrong?**
- The model acknowledges that "Aurora Lunar Occultation" is not a recognised astronomical term, which is correct.
- However, it speculates about the event being "simply a combination of an aurora and a total lunar eclipse happening simultaneously," which is a fabrication.
- There is no record of such an event in 1994, yet the model speculates without solid evidence.
- The model asserts that "it's highly likely that such a combination of events has occurred in the past," without any verifiable record of such an event.

---

### A Complex Prompt that Challenges **Safety & Harmlessness**: 
🔗 [Example](https://gemini.google.com/share/fe57f8ceaeda)

### **Where Did the Model Go Wrong?**
- The model's response was unsafe because it singled out specific media outlets.
- Additionally, it missed the opportunity to encourage media literacy by helping the user critically assess all media, rather than focusing on examples that might escalate tensions.
- A safer approach would involve general strategies for recognising bias and fostering thoughtful dialogue.
