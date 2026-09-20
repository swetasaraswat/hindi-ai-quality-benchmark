# Evaluation Rubric

Every example in `dataset/hindi_ai_evaluation.csv` is scored 1–5 on four **independent** axes. A response can score high on one axis and low on another — that gap is often the most useful signal (see the Key Finding in the main README).

---

## Language Quality

How natural and grammatically correct is the Hindi itself?

| Score | Definition |
|---|---|
| 5 | Native, natural, grammatically correct — reads like something a fluent native speaker would actually write. |
| 4 | Correct and understandable, with a minor stylistic issue (slightly stiff register, awkward word order). |
| 3 | Understandable but unnatural — a native speaker would notice it was translated/generated. |
| 2 | Significant grammatical or word-choice problems that impede natural reading. |
| 1 | Difficult to understand or fundamentally incorrect Hindi. |

## Factual Accuracy

Is the factual content of the response correct?

| Score | Definition |
|---|---|
| 5 | Fully accurate — every claim checks out. |
| 4 | Accurate with a very minor omission or imprecision that doesn't mislead. |
| 3 | Partially accurate — a mix of correct and questionable claims. |
| 2 | Contains a clear factual error alongside some correct content. |
| 1 | Fundamentally incorrect or fabricated. |

## Cultural Appropriateness

Is the response contextually and culturally sensitive, not just literally correct?

| Score | Definition |
|---|---|
| 5 | Appropriate and contextually sensitive — reflects real diversity/nuance where it exists. |
| 4 | Appropriate, with a small oversimplification that doesn't distort meaning. |
| 3 | Generally acceptable but flattens nuance or leans on a stereotype without malice. |
| 2 | Presents a partial or one-sided view as universal, or uses a misleading analogy. |
| 1 | Culturally misleading, offensive, or inappropriate. |

## Helpfulness

Does the response actually serve the original request/intent?

| Score | Definition |
|---|---|
| 5 | Directly and completely addresses what the user asked. |
| 4 | Addresses the request well, with minor gaps. |
| 3 | Partially useful but misses part of the intent (e.g. wrong register, wrong context). |
| 2 | Technically responds but is a poor fit for what was actually needed. |
| 1 | Doesn't meaningfully answer the request. |

---

## How to apply this rubric

Score each column independently. A response can have perfect grammar (**Language Quality = 5**) while still being factually wrong or culturally reductive (lower **Accuracy**/**Cultural Fit**). This separation is what distinguishes a linguistic quality check from a true localization quality check — and it's the entire point of scoring these as four separate axes instead of one overall number.
