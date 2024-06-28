# pythonproject
class Question:
    def __init__(self, prompt, answer):
        self.prompt = prompt
        self.answer = answer

question_list = [
    Question("What is the capital of India?\n(a) Mumbai\n(b) Delhi\n(c) Kolkata\n(d) Chennai\n", "b"),
    Question("Who painted the Mona Lisa?\n(a) Michelangelo\n(b) Leonardo da Vinci\n", "b"),
    Question("In which year was the Apple company founded?\n(a) 1976\n(b) 1984\n(c) 1998\n(d) 2001\n", "a")
]

def run_quiz(questions):
    score = 0
    for question in questions:
        user_answer = input(question.prompt).lower()
        if user_answer == question.answer:
            score += 1
    print("You got", score, "out of", len(questions), "questions correct!")

run_quiz(question_list)
