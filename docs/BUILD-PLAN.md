# Build Plan
Here's a practical breakdown for incremental dark/light mode implementation:

**Step 1 – CSS variables & themes (5 min)**
Define your color palette as CSS custom properties on `:root` (light default) and a `[data-theme="dark"]` selector. Cover backgrounds, text, borders, and accent colors. Test by manually adding `data-theme="dark"` to your `<html>` tag in dev tools.

**Step 2 – Toggle button & JS (5 min)**
Add a simple button (sun/moon icon or just text) that toggles the `data-theme` attribute on `<html>` between `"light"` and `"dark"`. Confirm clicking it swaps all your themed colors live.

**Step 3 – Persist preference (5 min)**
Save the chosen theme to `localStorage` on toggle. On page load, read it back and apply before the page renders (put the script in `<head>` to avoid a flash of wrong theme).

**Step 4 – Respect system preference (5 min)**
Use `prefers-color-scheme` media query as the fallback when there's no saved preference. Add a `matchMedia` listener so if the user changes their OS setting mid-session, your site reacts.

**Step 5 – Polish & edge cases (5–10 min)**
Swap your toggle icon/label to reflect current state, add a smooth `transition` on `background-color` and `color`, and audit any components using hardcoded colors that need converting to your CSS variables.
