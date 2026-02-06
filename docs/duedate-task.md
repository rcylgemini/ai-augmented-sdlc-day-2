# Due Date Task

## Step-by-step plan
1. Extend the task model in `src/App.jsx` to include `dueDate` as `string | null` with a default of `null`.
2. Update the add-task flow in `src/components/Form.jsx` to include an optional date input and pass the date value to the add handler.
3. Update the task display in `src/components/Todo.jsx` to render the due date string when present and show nothing when absent.
4. Update the edit flow in `src/components/Todo.jsx` to include a date input pre-filled with the task’s due date; clearing it should set `dueDate` to `null`.
5. Ensure the due date is persisted through task edits, completions, and filters without altering existing behavior.
6. Add any supporting styles in `src/index.css` to keep due date text compact and aligned with the task layout.

## Playwright testing plan
1. Launch the app and add a new task with a due date; verify the date string is shown in the task item.
2. Add a new task without a due date; verify no extra placeholder text appears.
3. Edit a task to change the due date and confirm the new date string is displayed.
4. Edit a task to clear the due date and confirm the date string is removed.
5. Toggle task completion and apply filters to ensure due date display remains consistent.
