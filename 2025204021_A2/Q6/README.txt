Q6 - Event Tracking System
==========================

OBJECTIVE:
Create a JavaScript function that captures all click events and page views across the page, 
tracking interactions with HTML tags and CSS objects. Logs should be formatted with:
- Timestamp of click/view
- Type of event (click/view/focus/change)
- Event object (dropdown/image/text/button/link/etc.)

FILES:
- event_tracker.html - Main event tracking implementation with demo page

FEATURES IMPLEMENTED:

1. COMPREHENSIVE EVENT TRACKING
   - Captures all click events on any element
   - Tracks page views (on DOMContentLoaded and initial load)
   - Monitors focus events on form elements
   - Tracks change events on inputs, selects, and textareas

2. INTELLIGENT ELEMENT IDENTIFICATION
   - Identifies element types: buttons, links, inputs, dropdowns, images, text, etc.
   - Classifies button types (primary/success/warning/danger)
   - Distinguishes input types (text/email/checkbox/radio/number)
   - Recognizes custom elements (image-item, dropdown-menu)

3. LOGGING SYSTEM
   - Console logging with format: "Timestamp | EventType | EventObject"
   - Visual event log panel with color-coded entries
   - ISO 8601 timestamp format
   - Real-time statistics tracking (clicks, views, focus, changes)

4. DEMO PAGE ELEMENTS
   Includes representative elements from Q1-Q5:
   - Buttons (multiple variants)
   - Form inputs (text, email, number, textarea)
   - Dropdowns/Select menus
   - Checkboxes and radio buttons
   - Links and navigation
   - Images and media placeholders
   - Text content (paragraphs, headings)
   - Hover dropdown menu

5. ADDITIONAL FEATURES
   - Clear log button
   - Export log to text file
   - Live event statistics dashboard
   - Color-coded log entries by event type
   - Scrollable log with newest entries on top

USAGE:
1. Open event_tracker.html in a web browser
2. Interact with any element on the page
3. View real-time events in the Event Log Console
4. Check browser console for formatted log output
5. Use "Clear Log" to reset or "Export Log" to save events

LOG FORMAT:
Timestamp: YYYY-MM-DD HH:MM:SS.mmm
Event Type: click | view | focus | change
Event Object: button-primary | link | text-input | dropdown | image | text | etc.

Example log entries:
2025-10-02 14:23:45.123 | click | button-primary
2025-10-02 14:23:46.456 | focus | text-input
2025-10-02 14:23:47.789 | change | dropdown
2025-10-02 14:23:48.012 | click | link
2025-10-02 14:23:49.345 | view | page

TECHNICAL IMPLEMENTATION:
- Global event listeners on document
- Event delegation for efficient tracking
- Smart element type detection via tagName, type, className, and role attributes
- Non-intrusive tracking (doesn't interfere with page functionality)
- Reusable tracking script can be injected into Q1-Q5 pages

BROWSER COMPATIBILITY:
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Uses ES6+ JavaScript features
- No external dependencies

NOTES:
- All functionality is contained in a single HTML file
- Consistent with Q3-Q5 light/clean CSS theme
- Includes both visual UI and programmatic logging
- Can be adapted to track additional event types if needed
