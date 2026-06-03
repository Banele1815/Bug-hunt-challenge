# TaskFlow Bug Report

## Bug 1: Add button triggers on hover instead of click
- **File:** app.js
- **Location:** addBtn event listener
- **Issue:** Task is added when mouse hovers over button instead of clicking
- **Cause:** Wrong event used (`mouseover` instead of `click`)
- **Fix:** Replaced `mouseover` with `click`

---

## Bug 2: Toggle task does not update correctly
- **File:** app.js
- **Location:** toggleTask() function
- **Issue:** Task completion state does not update properly
- **Cause:** Variable shadowing / incorrect map logic
- **Fix:** Corrected parameter naming and comparison logic

---

## Bug 3: Active filter shows wrong tasks
- **File:** app.js
- **Location:** getFilteredTasks()
- **Issue:** Active filter shows completed tasks
- **Cause:** Wrong condition (`completed === true` instead of `false`)
- **Fix:** Changed filter logic to show incomplete tasks

---

## Bug 4: Delete button does not remove correct task
- **File:** app.js
- **Location:** delete button event listener
- **Issue:** Clicking delete does nothing or deletes wrong item
- **Cause:** Using `event.target.id` (not set)
- **Fix:** Used `task.id` directly

---

## Bug 5: Filter logic duplication / incorrect separation
- **File:** app.js
- **Location:** getFilteredTasks()
- **Issue:** Filter logic is inconsistent between active/completed
- **Cause:** Duplicate or incorrect filtering conditions
- **Fix:** Corrected filter conditions to properly separate active (completed === false) and completed (completed === true) tasks
