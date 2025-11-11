# Aerospace Quiz CLI

A small, self-contained **command-line quiz** about basic aerospace and rocket concepts.

The goal is to have a lightweight educational tool that:
- checks basic understanding of rocket engines and orbital mechanics,
- is easy to extend with new questions,
- can be used as a tiny building block in a larger learning or assessment pipeline.

---

## Project structure

```text
aerospace-quiz-cli/
├─ data/
│  └─ questions.json        # question bank: text, options, correct answer, explanation
├─ src/
│  ├─ __init__.py
│  └─ quiz.py               # main CLI quiz script
├─ tests/
│  ├─ __init__.py
│  └─ test_loader.py        # basic unit test for question loading
├─ README.md
├─ requirements.txt
└─ .gitignore



Installation

Create and activate a virtual environment (optional), then:

pip install -r requirements.txt


Usage

Run the quiz from the project root:

python -m src.quiz
# or
python src/quiz.py



You will see a series of multiple-choice questions:

enter 1, 2, 3 or 4 to answer,

or press q to quit early.

After the quiz, you get:

the number of correct answers,

your percentage score,

explanations for each question.


Question format

Questions are stored in data/questions.json as a simple list of objects:


{
  "id": 1,
  "category": "rockets",
  "question": "What is specific impulse (Isp) in rocket engines?",
  "options": [
    "Option A",
    "Option B",
    "Option C",
    "Option D"
  ],
  "correct_index": 1,
  "explanation": "Short explanation of why this answer is correct."
}


You can easily extend the quiz by adding more entries to this JSON file.


Possible extensions

add difficulty levels (basic / intermediate / advanced),

track scores by category (rockets, orbits, propulsion, materials),

export quiz results to a CSV or JSON log,

build a small web or GUI version on top of the same JSON question bank.

Even in this simple CLI form, the project shows how to combine
domain knowledge (aerospace) with clean Python code and basic testing.

