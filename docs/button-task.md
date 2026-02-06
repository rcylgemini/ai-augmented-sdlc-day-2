# Button Styling Task

## Step-by-step plan
1. Review current button styles and class usage in `src/index.css` and components that render buttons (`src/components/Form.jsx`, `src/components/Todo.jsx`, `src/components/FilterButton.jsx`).
2. Define CSS variables or class names for primary, destructive, and neutral button styles in `src/index.css`.
3. Update button class names in `src/components/Form.jsx` for the Add and Save actions to use the primary style.
4. Update button class names in `src/components/Todo.jsx` for Delete to use the destructive style and for Cancel to use the neutral style.
5. Ensure filter buttons apply a selected class and hover states via `src/components/FilterButton.jsx` and `src/index.css`.
6. Verify hover states and selected states visually across all button types.

## Playwright testing plan
1. Launch the app and navigate to the main page.
2. Create a task and verify the Add button has the primary class and hover state via computed style.
3. Enter edit mode on a task and verify the Save button uses the same primary class and hover state.
4. Verify Delete buttons use the destructive class and show hover styling.
5. Click each filter and verify the selected filter button receives the selected class and styling.
