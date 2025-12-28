# CountOn – Discipline Clock

A minimalist hourly discipline tracker designed to help you build consistency and accountability through the power of hourly planning and review.

## Features

- **Hourly Tracking**: Track your productivity and discipline hour by hour from 6 AM to 10 PM
- **Real-time Countdown**: See live countdown timers for the current hour
- **Daily Planning**: Set goals and plans for each hour
- **Status Tracking**: Mark hours as "Did" or "Not" to track completion
- **Daily Score**: Get a percentage-based score showing your completion rate
- **Date Navigation**: Easy navigation between previous, current, and future dates
- **Persistent Storage**: All your data is saved locally using browser localStorage
- **Dark Theme**: Clean, minimalist dark interface inspired by modern design principles
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## How It Works

1. **Plan**: For each hour (6 AM - 10 PM), write down what you plan to accomplish
2. **Track**: As each hour completes, mark whether you succeeded ("Did") or failed ("Not")
3. **Review**: Check your daily completion percentage to measure your discipline
4. **Improve**: Use historical data to identify patterns and improve consistency

## Usage

### Starting the App
Simply open `index.html` in your web browser. The app runs entirely in the browser with no backend required.

### Navigation
- **Yesterday/Tomorrow buttons**: Navigate between dates
- **Today button**: Jump back to the current date
- **Daily Score**: Displays your completion percentage at the top

### Hour Actions
- **Active Hour**: The current hour (live countdown shown)
  - Edit your plan in the textarea
  - Click "Did" if you completed your plan
  - Click "Not" if you didn't complete your plan
  
- **Past Hours**: Hours that have passed
  - Automatically marked as "Not" if no status was set
  - Shows completion status
  
- **Future Hours**: Hours not yet started
  - You can plan ahead by editing the textarea
  - Buttons disabled until the hour becomes active

## Features Explained

### Auto-Marking
If the current hour passes without any action, the system automatically marks it as "Missed" to maintain accountability.

### Live Countdown
The active hour displays a real-time countdown (MM:SS format) showing time remaining in the hour.

### Persistent Data
All hour plans and statuses are saved to browser localStorage with a unique key per date, allowing your data to persist between sessions.

## Technology Stack

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS variables and animations
- **Vanilla JavaScript**: No dependencies required
- **localStorage API**: Client-side data persistence

## Browser Compatibility

Works in all modern browsers that support:
- ES6 JavaScript
- localStorage API
- CSS Grid and Flexbox

## Motivation

CountOn is built on the principle that **discipline is a hourly practice**. Instead of vague daily goals, this app helps you:
- Break your day into manageable hourly blocks
- Measure discipline in real-time
- Build a streak of consistent productivity
- Develop accountability through immediate feedback

## File Structure

```
CountOn/
├── index.html          # Main application file (HTML + CSS + JS)
└── README.md          # This file
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Bhanuteja12-coder/CountOn.git
   ```

2. Navigate to the project:
   ```bash
   cd CountOn
   ```

3. Open in your browser:
   ```bash
   # On Windows
   start index.html
   
   # On macOS
   open index.html
   
   # On Linux
   xdg-open index.html
   ```

## Customization

You can easily customize the app by modifying the CSS variables at the top of `index.html`:

```css
:root{
    --bg:#020617;           /* Background color */
    --border:#1e293b;       /* Border color */
    --green:#22c55e;        /* Success/active color */
    --red:#ef4444;          /* Failure/negative color */
    --muted:#64748b;        /* Muted text color */
}
```

You can also adjust the tracking hours by changing the `START` and `END` variables in the JavaScript section.

## Tips for Success

1. **Be Honest**: Mark accurately whether you completed your plans or not
2. **Plan Realistically**: Don't overcommit in your hourly plans
3. **Review Daily**: Check your score at the end of each day
4. **Build Streaks**: Aim for consistent high scores over multiple days
5. **Adjust**: If your score is always 0% or 100%, adjust your planning difficulty

## License

This project is open source and available under the MIT License.

## Support

If you have questions or suggestions, feel free to open an issue on GitHub.

---

**Remember**: CountOn isn't about being perfect; it's about being consistent. Start today and build the discipline you deserve.
