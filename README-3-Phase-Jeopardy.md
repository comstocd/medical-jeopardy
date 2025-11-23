# Medical Jeopardy - 3 Phase Edition

## Overview
This is an enhanced Medical Jeopardy game that follows the TV show format with three distinct phases:
1. **Jeopardy Round** - Standard questions with 200-1000 point values
2. **Double Jeopardy Round** - Harder questions with 400-2000 point values  
3. **Final Jeopardy** - Single question with wagering

## Files Required
- `medical-jeopardy-3-phase.html` - Main game file
- `gameboards-data.js` - Contains all question data from all gameboards

**IMPORTANT:** Both files must be in the same directory for the game to work.

## Available Gameboards

### Jeopardy Round Options:
- PGY-1 Gameboard (Basic level)
- PGY-2 Gameboard (Intermediate level)
- PGY-3 Gameboard (Advanced level)
- Regular Jeopardy Board 1
- Regular Jeopardy Board 2
- Regular Jeopardy Board 3
- Regular Jeopardy Board 4
- Regular Jeopardy Board (Original)

### Double Jeopardy Round Options:
- Double Jeopardy Board 1
- Double Jeopardy Board 2
- Double Jeopardy Board 3
- Double Jeopardy Board 4

## How to Use

### Setup:
1. Open `medical-jeopardy-3-phase.html` in a web browser
2. Enter team names in the score board
3. Select a gameboard for the Jeopardy Round
4. Select a gameboard for the Double Jeopardy Round
5. Click "Confirm Selection"

### Jeopardy Round:
1. Click "Start Jeopardy" to begin
2. Click any dollar amount to reveal a question
3. Click "Reveal Answer" to show the answer and teaching points
4. Use score controls to adjust team scores:
   - "+Current" adds the question value
   - "-$200" subtracts $200 (for wrong answers)
5. Continue until all questions are answered

### Double Jeopardy Round:
1. Click "Start Double Jeopardy" to begin the second round
2. Questions are worth double points (400-2000)
3. Same gameplay as Jeopardy Round

### Final Jeopardy:
1. Click "Start Final Jeopardy"
2. Each team enters their wager (maximum is their current score or $1000)
3. Click "Show Question" to reveal the Final Jeopardy question
4. Click "Reveal Answer" to show the answer
5. System will prompt whether each team answered correctly
6. Scores automatically adjust based on wagers
7. Click "End Game" to see final rankings

## Features

### Gameboard Switching
- Change gameboards at any time by clicking "⚙️ Settings"
- Select different boards for Jeopardy and Double Jeopardy rounds
- All gameboards loaded from `gameboards-data.js`

### Score Management
- Manual score adjustments for each team
- Automatic score calculation in Final Jeopardy
- Scores persist through all three phases

### Phase Navigation
- Clear phase indicator shows current round
- Phase buttons activate/deactivate appropriately
- Cannot skip to Final Jeopardy without completing prior rounds

### Game Controls
- Reset Game: Clears all scores and returns to setup
- Settings: Return to gameboard selection screen
- All questions track as "answered" to prevent duplicates

## Tips for Hosts

1. **Team Setup**: Enter team names before starting - they display in Final Jeopardy wagering
2. **Score Adjustments**: Use "+Current" for correct answers, "-$200" for incorrect
3. **Final Jeopardy Wagers**: System enforces maximum wager limits automatically
4. **Phase Progression**: You can advance to Double Jeopardy or Final Jeopardy at any time

## Technical Notes

- Fully client-side - no server required
- Works on iPad, desktop, and mobile browsers
- Touch-optimized interface
- All 11 gameboards (~260 questions) loaded at once
- Gameboards data file is ~300KB

## Customization

To add more gameboards:
1. Edit `gameboards-data.js`
2. Add new board following the existing JSON structure:
```javascript
"Your Board Name": {
  "Category Name": {
    200: {q: "question", a: "answer", followup: "teaching point"},
    400: {...},
    // etc
  }
}
```

## Troubleshooting

**Board selector shows no options:**
- Ensure `gameboards-data.js` is in the same directory
- Check browser console for JavaScript errors

**Questions don't appear:**
- Verify both files are in the same location
- Try hard refresh (Ctrl+Shift+R or Cmd+Shift+R)

**Scores not calculating:**
- Ensure team names are entered
- Check browser console for errors

## For iPad Use

1. Open in Safari
2. Tap Share button → Add to Home Screen
3. Launch from home screen for full-screen experience
4. Game works offline once loaded
