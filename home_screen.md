## Readly Home Screen 

# Writing the Jira story to a markdown file
content = """# [PROJ-456] Build “Home” Feed Screen (Medium-Style)

## Description
As a **reader**,  
I want a polished, vertically-scrolling “Home” feed—complete with category tabs and article cards, plus bottom navigation—so that I can seamlessly browse and discover content on my mobile device.

## Acceptance Criteria
1. **Overall Layout**
   - Screen background: dark (#21262D), text/icons: light cream (#EDE8DA).
   - **Top bar**:
     - Left: “Home” label (16 sp, medium).
     - Right: bell icon for notifications.
   - **Tabs**:
     - Under the top bar: horizontal tabs (“For you”, “Following”, “TypeScript”, “Python”), scrollable if they overflow.
     - Active tab indicated by a 2 px cream underline.
   - **Bottom nav**: three evenly spaced icons (Home, Search, Saved); active icon tinted cream.

2. **Article Cards**
   - Displayed immediately below the tabs in a vertical list.
   - Each card:
     - Full width minus 16 dp side margins.
     - Separated by 1 dp dividers (#575F6A).
     - Contents:
       - Headline (white, up to two lines, ellipsized).
       - Subtext (14 sp, 60% opacity, one line).
       - Thumbnail on the right (80 × 60 dp, 6 dp corner radius).

3. **Scrolling & Pagination**
   - Infinite scroll: load 10 additional cards when the user reaches the bottom.
   - Show a loading spinner at the bottom while fetching.
   - On fetch error: inline “Retry” button.

4. **Interactions**
   - **Card tap** → opens article detail screen.
   - **Tab tap** → reloads feed for that category.
   - **Bell icon tap** → opens notification center.
   - **Bottom-nav tap** → navigates to respective screens.

5. **Empty & Error States**
   - **No articles**: show “No content here yet” centered.
   - **Initial load failure**: full-screen error placeholder with “Try Again” button.

## Definition of Done
- Matches approved Figma mocks ([link](https://www.figma.com/design/VKP5bGQLbaFaA0pf6RdeHv/Readly?node-id=0-1&t=JtaHQzflA7TfVLiX-1)). 
- Verified on Android (API 21+) and iOS (12+).
- Unit tests for components; integration tests for scroll, tabs, and nav.
- Code reviewed and merged; scrolling performance ≥ 60 fps.



