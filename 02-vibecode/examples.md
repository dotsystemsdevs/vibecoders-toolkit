# Examples

Real prompts and conversations from shipping 3 Android apps in 3 weeks.

---

## Example 1: Building a todo app home screen

### Context
Day 1 of building a todo app. Need to create the main screen where users see their tasks.

### The prompt

```
Create the home screen for a React Native todo app using Expo.

Layout:
- Header at top with app title "Slothy" and settings icon (gear) in top-right
- Below header: text input for new todo with placeholder "What are you putting off?"
- Add button next to input (blue, rounded)
- Below input: scrollable list of todos
- Each todo item: checkbox on left, todo text in middle, delete icon (X) on right
- Completed todos: gray text with strikethrough
- Uncompleted todos: black text

Styling:
- Background: white
- Primary color: #4A90E2 (blue)
- Font: System default
- Padding: 16px around content
- Todo items: 56px height, border bottom 1px gray

Functionality:
- Add button creates new todo, adds to top of list
- Checkbox toggles completed state
- Delete icon removes todo
- Empty input = button disabled
- After adding todo, clear input and focus it again

Use React hooks (useState). Store todos in state as array of objects: {id: string, text: string, completed: boolean}.
```

### What AI generated

Working code with all requirements. We reviewed and found 1 issue: delete wasn't asking for confirmation.

### Follow-up prompt

```
Add confirmation before deleting a todo. Show Alert with title "Delete todo?", message with the todo text, and two buttons: "Cancel" and "Delete". Only delete if user taps Delete.
```

### Result

Worked perfectly. Committed. Total time: 12 minutes.

---

## Example 2: Adding local storage

### Context
Day 2. App works but todos disappear when you close it. Need persistence.

### The prompt

```
Add AsyncStorage to persist todos in the React Native app.

Requirements:
- Save todos to AsyncStorage after every add/delete/toggle
- Load todos on app start (useEffect)
- Storage key: "todos"
- Value: JSON stringified array
- Handle errors:
  - If load fails: console.log error, start with empty array
  - If save fails: show Alert "Failed to save" and console.log error

Use @react-native-async-storage/async-storage package.

Update these functions to save after changing state:
- addTodo (after adding)
- toggleTodo (after toggling)
- deleteTodo (after deleting)

Add loadTodos function that runs on component mount.
```

### What AI generated

Complete implementation with try/catch blocks. We tested by:
1. Adding todos
2. Closing app
3. Reopening app
4. Todos were there

### Issue we caught

AI forgot to add the package to package.json. We added manually:

```bash
expo install @react-native-async-storage/async-storage
```

### Result

Worked after installing package. Committed. Total time: 15 minutes.

---

## Example 3: Adding push notifications

### Context
Day 3. Want to remind users about their todos.

### The prompt

```
Add push notifications to remind users about uncompleted todos.

Requirements:
- Request notification permission on app start (if not already granted)
- Schedule daily notification at 6 PM
- Notification title: "Don't forget!"
- Notification body: "You have X uncompleted todos" (X = count)
- If no uncompleted todos, don't send notification
- Cancel old notification before scheduling new one
- Reschedule every time user adds/deletes/toggles todo

Use expo-notifications package.

Add these functions:
- requestPermissions() - ask for notification permission
- scheduleNotification(todoCount) - schedule daily 6 PM notification
- cancelNotification() - cancel existing notification

Call scheduleNotification after every todo change.
```

### What AI generated

90% correct code. Issues we found:

1. Time was hardcoded to 18:00 in UTC, not local time
2. Didn't handle case where user denies permission
3. Notification fired immediately for testing, not at 6 PM

### Follow-up prompts

**Prompt 2:**
```
Fix the time to use local timezone. The trigger should fire at 6 PM user's local time every day, not UTC.
```

**Prompt 3:**
```
If user denies notification permission, save this in AsyncStorage key "notification_permission_denied" and don't ask again. Show Alert "Notifications disabled" once.
```

### Result

After 2 iterations, worked perfectly. Tested by setting time to 1 minute in future. Total time: 28 minutes.

---

## Example 4: Building a login form (with security issues)

### Context
Considering adding user accounts to one of our apps. Testing how AI handles authentication.

### The prompt

```
Create a login screen for React Native app.

Layout:
- Email TextInput (keyboard: email-address)
- Password TextInput (secureTextEntry: true)
- Login button below
- "Forgot password?" link at bottom

Validation:
- Email must be valid format (use regex)
- Password must be at least 6 characters
- Show error text below field if invalid
- Disable button until both valid

Styling:
- Match existing app: primary blue #2196F3
- Inputs: white background, gray border
- Button: blue with white text
- Error text: red

Make API call to POST /api/login with {email, password}.
Handle responses:
- 200: save token to AsyncStorage, navigate to Home
- 401: show "Invalid credentials"
- 500: show "Server error"
```

### What AI generated

**Working login form BUT with critical security issues:**

1. **Password sent in plain text** (should be hashed)
2. **No HTTPS enforcement** (credentials sent unencrypted)
3. **Token stored in AsyncStorage** (not secure, should use SecureStore)
4. **No rate limiting** (brute force attack possible)
5. **Error messages too specific** ("Email not found" vs "Invalid credentials" reveals which emails exist)

### What we learned

**AI will generate authentication code that LOOKS correct but has security holes.**

### What we did

Stopped. Decided not to add backend to this app. If we need auth, we'll hire a developer to review it.

### Cost of this decision

- **Time saved by not building backend:** ~40 hours
- **Risk avoided:** Data breach, user accounts compromised
- **Better approach:** Build offline-only MVPs, validate product first, then hire for secure backend

---

## Example 5: Export to Excel

### Context
Building an income tracker. Users want to export their data to Excel.

### The prompt

```
Add "Export to Excel" button to the income tracker app (React Native).

Requirements:
- Button at top of screen, icon: download
- On press, generate .xlsx file with all income/expense entries
- File columns: Date | Description | Amount | Type (Income/Expense)
- Date format: YYYY-MM-DD
- Amount: number with 2 decimals
- Save file to device and show share sheet (user can save to Files or email)

Use these packages:
- xlsx for generating Excel file
- expo-sharing for share sheet
- expo-file-system for file operations

Data structure (from state):
entries = [{id, date, description, amount, type}, ...]

File name: income_tracker_export_{timestamp}.xlsx
```

### What AI generated

Complete implementation. Issues we found:

1. **File saved to cache directory** (gets deleted by system) — should save to document directory
2. **No loading indicator** (export takes 2-3 seconds for large data)
3. **Crash if user has 0 entries** (tried to export empty array)

### Follow-up prompts

**Prompt 2:**
```
Save file to document directory instead of cache. Use FileSystem.documentDirectory.
```

**Prompt 3:**
```
Add loading indicator (ActivityIndicator) while generating file. Show "Generating..." text below.
```

**Prompt 4:**
```
If entries array is empty, show Alert "No data to export" and return early. Don't try to generate file.
```

### Result

After 3 iterations, worked perfectly. Tested with:
- 0 entries (showed alert)
- 5 entries (exported correctly)
- 100 entries (took 3 seconds, loading indicator showed)

Committed. Total time: 35 minutes.

---

## Example 6: Fixing a production bug

### Context
User reported: "App crashes when I open Settings". We shipped this 2 days ago to 30 users.

### The prompt

```
Debug this crash in React Native Settings screen.

Error from crash log:
"TypeError: Cannot read property 'name' of undefined"

Code (Settings.tsx):
[pasted the full component code]

User flow that triggers crash:
1. Open app
2. Tap Settings icon
3. App crashes immediately

Help me find the bug and fix it.
```

### What AI found

Settings screen tried to read `user.name` but `user` object was undefined (we weren't handling the case where user hasn't set their name yet).

### AI's fix

```javascript
// Before (crashes):
<Text>{user.name}</Text>

// After (handles undefined):
<Text>{user?.name || 'Set your name'}</Text>
```

### What we learned

AI is good at debugging when you give it:
1. The error message
2. The code
3. The steps to reproduce

### Result

Fixed in 5 minutes. Pushed update to Play Store. Total time from report to fix: 20 minutes.

---

## Example 7: When AI gets it completely wrong

### Context
Building a statistics screen for golf ball tracker. Want to show chart of balls lost over time.

### The (overly vague) prompt

```
Add a chart to show balls lost over time.
```

### What AI generated

Used a charting library we didn't have installed. Generated code with syntax we didn't recognize. Chart showed random data, not our real data. Labels were in Spanish for some reason.

### What went wrong

**Prompt was too vague.** AI made too many assumptions:
- Which charting library?
- Which data format?
- Which type of chart?
- What time range?

### Better prompt (attempt 2)

```
Add a line chart to the Stats screen showing balls lost per round.

Requirements:
- Use react-native-chart-kit library
- Chart type: LineChart
- Data source: rounds array from state (structure: [{id, date, ballsLost}, ...])
- X-axis: round number (1, 2, 3, ...)
- Y-axis: balls lost (0-20)
- Show last 10 rounds only
- Chart width: screen width minus 32px padding
- Chart height: 220px
- Line color: red
- Background: gradient from light gray to white
- If less than 2 rounds, show text "Play at least 2 rounds to see chart"

Use LineChart component from react-native-chart-kit. Format data as:
{
  labels: ['1', '2', '3', ...],
  datasets: [{data: [5, 3, 8, ...]}]
}
```

### Result

AI generated exactly what we needed. Worked first try. Total time: 8 minutes.

### Lesson

**Vague prompts waste time.** The 2 minutes you save writing a short prompt costs 20 minutes of debugging bad code.

---

## Key patterns from these examples

### What works

1. **Specific prompts with exact requirements**
2. **Include data structures and format**
3. **Mention packages/libraries to use**
4. **Describe edge cases to handle**
5. **Give styling details (colors, sizes, layout)**

### What doesn't work

1. **Vague prompts ("make it better")**
2. **Asking AI to choose architecture**
3. **Trusting AI with security**
4. **Expecting AI to understand business logic**

### Time breakdown from all examples

| Example | First attempt | Iterations | Total | Would take manually |
|---------|---------------|------------|-------|---------------------|
| Todo home screen | 10 min | 2 min | 12 min | 45 min |
| AsyncStorage | 12 min | 3 min | 15 min | 30 min |
| Notifications | 15 min | 13 min | 28 min | 60 min |
| Excel export | 20 min | 15 min | 35 min | 90 min |
| Bug fix | 5 min | 0 | 5 min | 20 min |
| Chart | 3 min | 5 min | 8 min | 40 min |

**Average speed increase: 3-4x faster than manual coding**

**But:** Only because we reviewed carefully and caught bugs before shipping.

---

## Bottom line

Real vibecoding is:
- Writing detailed prompts (2-5 minutes)
- Reviewing generated code carefully (5-10 minutes)
- Testing thoroughly (3-5 minutes)
- Iterating when needed (0-15 minutes)

**It's not magic. It's a tool that makes you faster if you use it right.**
