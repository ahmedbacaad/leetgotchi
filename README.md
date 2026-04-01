# LeetGotchi 🐣

A Tamagotchi that only survives if you honestly solve one LeetCode problem a day.

## Setup (2 minutes)

```bash
cd leetgotchi
pip install -r requirements.txt
export ANTHROPIC_API_KEY=your_key_here   # get free at console.anthropic.com
python app.py
```

Then open http://localhost:5000

## How it works

1. Open the app — see your pet's status
2. Click "Start Today's Problem"
3. Enter the LeetCode problem title + link
4. Hit START — timer begins
5. Fill in all 5 sections (explain, approach, solution, complexity, reflection)
6. After 30 minutes, submit for AI judgment
7. Claude evaluates your honesty and asks a follow-up question
8. Score ≥ 60 → pet survives and gains health
9. Score < 60 → pet loses health
10. Miss a day → pet gets sick

## Anti-cheat system

- Timer must run (can't fake it)
- All text fields have minimum length requirements
- Claude AI evaluates if explanations show real understanding
- Follow-up question probes your actual knowledge
- Suspicious score tracked per session

## Pet stages

egg → baby (1 day) → teen (3 days) → adult (7 days) → dragon (14 days) → legend (30 days)

## Stack

- Flask + SQLite (backend)
- Vanilla HTML/CSS/JS (frontend)
- Anthropic Claude API (AI honesty evaluation)
- Pixel art UI with retro CRT aesthetic
