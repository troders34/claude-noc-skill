# Output

Write all questions, answer options, key answers, and explanations in English.

## Choosing the output format
Decide the format from the user's request:
- If the request contains "PDF" or "in PDF" (any capitalization), produce a PDF file.
- If the request contains "Markdown" or "md file" (any capitalization), produce a Markdown (.md) file.
- If the request contains both, produce both files.
- If the request contains neither, produce a Markdown file by default.

## Result structure
1. Questions and answer options first, numbered in order.
2. After the last question, a section titled "Answer Key and Explanations" with the key answer and explanation for each question, listed by question number.
3. Follow the Key answer / Explanation layout shown in format.md.
