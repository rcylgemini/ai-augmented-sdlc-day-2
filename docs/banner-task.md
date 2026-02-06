# Banner Task

## Step-by-step plan
1. Add a banner region to `src/App.jsx` above the main content with title, subtitle, and info item.
2. Choose the info item as total task count derived from the tasks array in `src/App.jsx`.
3. Create semantic structure for the banner using appropriate HTML elements (for example `header`, `h1`, `p`, and a small info badge).
4. Add banner layout and typography styles in `src/index.css` consistent with the app layout.
5. Ensure the banner renders on all screens and does not interfere with existing focus management.

## Playwright testing plan
1. Launch the app and verify the banner is visible at the top of the page.
2. Assert the banner includes the title text and subtitle text.
3. Add and delete tasks, then verify the total task count displayed in the banner updates accordingly.
4. Resize the viewport to a narrow mobile width and confirm the banner remains visible and readable.
