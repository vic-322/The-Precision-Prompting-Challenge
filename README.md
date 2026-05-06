The-Precision-Prompting-Challenge
You are the newly appointed AI Strategy Lead at AfyaTech, a Nairobi-based health tech startup. Your team is building an SMS-based maternal health assistant for expectant mothers in rural Kenya and Uganda. Early testing shows your current AI prompts produce generic, urban-centric advice that ignores:
Prompt A: Nutrition Advice (Localized)

AIM Framework

A (Audience): Pregnant women in rural Kenya and Uganda with limited income and access to markets
I (Intent): Provide practical, affordable, culturally relevant nutrition advice
M (Mode): SMS-friendly, simple language, actionable tips

MAP Framework

M (Model Constraints): Must use locally available foods such as: ugali, sukuma wiki, matooke, beans, groundnuts); avoid imported foods
A (Augmented Context): Consider seasonal food availability, local markets, and common diets
P (Prompt Instruction):
“Provide 3–5 simple nutrition tips for a pregnant woman living in a rural area of Kenya or Uganda. Use locally available foods such as ugali, sukuma wiki, matooke, beans, groundnuts, milk, and eggs. Ensure tips are affordable, culturally appropriate, and easy to follow via SMS. Avoid suggesting foods that may not be locally available.”

Key Improvement:
Reduces hallucination and irrelevance by anchoring advice in real, local food systems instead of generic global recommendations.

Prompt B: Appointment Reminders (Context-Aware)

AIM Framework

A (Audience): Pregnant women in rural areas with limited transport and clinic access
I (Intent): Encourage timely clinic visits without causing stress or impractical expectations
M (Mode): Short SMS reminders with flexible planning

MAP Framework

M (Model Constraints): Account for travel time, transport costs (e.g., motorbike, walking), clinic days, and CHW availability
A (Augmented Context): Rural clinics may operate on specific days; community health workers (CHWs) may assist locally
P (Prompt Instruction):
“Generate a friendly SMS reminder for a pregnant woman about an upcoming clinic visit. Consider that she may need to walk or use a motorbike, clinics may only open on certain days, and community health workers may be available. Suggest planning ahead and offer an alternative such as contacting a CHW if travel is difficult.

Key Improvement:
Improves usability and adherence by aligning reminders with real-world access constraints instead of assuming urban healthcare availability.

Prompt C: Emergency Triage (Chain-of-Thought + Verifier)

Prompt Instruction (Enhanced Pattern):
“You are assisting a pregnant woman in a rural area via SMS.

Step 1: Ask 2–3 short clarifying questions about symptoms (e.g., type of pain, duration, bleeding, fever).
Step 2: Based on responses, classify the situation as mild, moderate, or urgent.
Step 3: Provide calm, clear next steps using locally realistic options (home care, contacting a community health worker, or going to a clinic).
Step 4: Avoid causing panic—use reassuring language.
Step 5 (Verifier): Before giving final advice, check:

Is the recommendation safe?
Is it feasible in a rural setting?
Does it avoid unnecessary urgency?

Then provide the final SMS response.”

Key Improvement:
Reduces panic and unsafe recommendations by forcing clarification and validation before advice, ensuring context-aware triage.

Reflection (≈100 words)

This exercise reframes AI from a knowledge generator to a contextual decision-support tool. In healthcare, accuracy alone is insufficient—relevance determines impact. By embedding local realities into prompts, AI becomes more inclusive and trustworthy. The use of structured frameworks like AIM and MAP ensures outputs are grounded, while patterns like Chain-of-Thought and Verifier introduce safety checks. I now see AI not as replacing healthcare systems, but as augmenting them—bridging gaps where infrastructure is limited. Precision prompting transforms AI from a generic advisor into a culturally aware assistant that respects constraints and improves real-world health outcomes.

Savannah Adventure – Quiz Answers
1. MAP Failure + Redesign

Failure Explanation (MAP):

M: Model defaulted to global nutrition knowledge
A: Missing local food context (Kakamega availability)
P: Prompt too vague (“nutrition tips”)

Redesigned Prompt:
“Give nutrition advice for a pregnant woman in Kakamega County using only locally available foods such as sukuma wiki, maize flour, ugali, beans, sweet potatoes, groundnuts, and local fruits. Ensure affordability and cultural relevance.”

2. Verifier Pattern for Triage

Improved Prompt:
“Before giving advice for abdominal pain during pregnancy, ask:

How severe is the pain?
How long has it lasted?
Are there other symptoms like bleeding or fever?

Then verify:

Does the situation require urgent care?
Can the user realistically access a clinic?

Only then provide calm, step-by-step guidance.”

3. Chain-of-Thought vs Summarization

Chain-of-Thought adds value by adapting global guidelines to local realities. Instead of repeating WHO recommendations, it reasons through constraints like transport, cost, and cultural beliefs. This produces actionable advice, not just information. In rural East Africa, applicability matters more than completeness—making CoT far more impactful.

4. OCEAN Framework for Data Validation
O (Origin): Check data source credibility
C (Currency): Ensure data is up-to-date (detect outdated stats like 1.8 vs 0.9)
E (Evidence): Cross-check with trusted datasets
A (Accuracy): Validate figures before reporting
N (Nuance): Consider regional disparities

Outcome: Prevents misinformation by enforcing data verification before dissemination.
