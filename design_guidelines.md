# Health & Wellness Platform Design Guidelines

## Design Approach

**Reference-Based Approach** drawing inspiration from leading health and wellness platforms (Headspace, Calm, Ada Health) that balance trust, accessibility, and emotional support with functional data management.

**Core Principles:**
- Trust and credibility through clean, professional aesthetics
- Emotional comfort via calming color palette and gentle interactions
- Accessibility-first design for diverse user needs
- Clear information hierarchy for medical data

---

## Color Palette

### Light Mode
**Primary Colors:**
- Primary Blue: `217 91% 60%` - Medical trust and professionalism
- Primary Blue Hover: `217 91% 55%`
- Secondary Slate: `215 20% 65%` - Supporting elements

**Status Colors:**
- Success Green: `160 84% 39%` - Positive feedback, completed actions
- Warning Amber: `38 92% 50%` - Important alerts, reminders
- Error Red: `0 84% 60%` - Critical alerts, emergency actions

**Neutral Palette:**
- Background: `210 40% 98%` - Main app background
- Surface: `0 0% 100%` - Cards, modals, elevated surfaces
- Border: `215 20% 90%` - Subtle dividers
- Text Primary: `215 25% 17%` - Main content
- Text Secondary: `215 16% 47%` - Supporting text

### Dark Mode
**Primary Colors:**
- Primary Blue: `217 91% 65%` - Increased luminance for visibility
- Secondary Slate: `215 20% 50%`

**Status Colors:**
- Success Green: `160 60% 50%` - Adjusted for dark backgrounds
- Warning Amber: `38 85% 55%`
- Error Red: `0 72% 65%`

**Neutral Palette:**
- Background: `222 47% 11%` - Deep navy base
- Surface: `217 33% 17%` - Cards and surfaces
- Border: `215 20% 25%`
- Text Primary: `210 40% 98%`
- Text Secondary: `215 20% 65%`

---

## Typography

**Font Stack:**
- Primary: 'Inter', -apple-system, system-ui, sans-serif
- Monospace: 'JetBrains Mono', 'Courier New', monospace (for medical data)

**Hierarchy:**
- Display: text-5xl font-bold tracking-tight (Hero headings)
- H1: text-3xl font-semibold (Page titles)
- H2: text-2xl font-semibold (Section headers)
- H3: text-xl font-medium (Card titles)
- Body: text-base font-normal (Main content)
- Caption: text-sm font-normal (Metadata, timestamps)
- Small: text-xs font-medium (Tags, labels)

---

## Layout System

**Spacing Scale:**
Use Tailwind units of `2, 3, 4, 6, 8, 12, 16` for consistent rhythm
- Micro spacing: `p-2, gap-3`
- Component spacing: `p-4, p-6, gap-4`
- Section spacing: `p-8, py-12`
- Page margins: `px-4 md:px-8 lg:px-16`

**Grid Patterns:**
- Dashboard cards: `grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6`
- Report list: `grid-cols-1 lg:grid-cols-2 gap-4`
- Settings layout: Two-column max-w-5xl centered

---

## Component Library

### Cards & Surfaces
- Default cards: `bg-white dark:bg-surface rounded-xl shadow-sm border border-border p-6`
- Interactive cards: Add `hover:shadow-md transition-shadow cursor-pointer`
- Status cards: Left border accent (`border-l-4 border-l-success`)

### Navigation
- Top navbar: Fixed, translucent backdrop-blur with border-b
- Sidebar (desktop): `w-64` collapsible with icon-only compact mode
- Bottom nav (mobile): `fixed bottom-0` with 4-5 primary actions
- Breadcrumbs: For deep navigation in reports/journal

### Forms & Inputs
- Input fields: `rounded-lg border border-border bg-white dark:bg-surface px-4 py-3`
- Focus states: `ring-2 ring-primary ring-offset-2`
- Floating labels: Smooth transition on focus
- Toggle switches: iOS-style for settings/privacy controls
- File upload: Drag-drop zones with dashed borders and upload icon

### Data Display
- Mood chart: Soft gradient area chart with rounded corners
- Fitness stats: Large numeric display with unit labels and trend indicators
- Medical reports: List view with preview thumbnails, tags, and status badges
- Journal timeline: Vertical timeline with date markers and entry cards

### Buttons
- Primary: `bg-primary text-white rounded-lg px-6 py-3 font-medium`
- Secondary: `bg-secondary/10 text-secondary rounded-lg px-6 py-3`
- Outline on images: `bg-white/20 backdrop-blur-md border border-white/30 text-white` (no custom hover states)
- Icon buttons: `rounded-full p-3` with hover background

### Modals & Overlays
- Modal backdrop: `bg-black/50 backdrop-blur-sm`
- Modal content: `bg-white dark:bg-surface rounded-2xl shadow-2xl max-w-2xl`
- Sheet (mobile): Slide up from bottom with drag handle
- Tooltips: `bg-gray-900 text-white text-sm rounded-lg px-3 py-2`

### AI Chat Interface
- Chat bubbles: User messages align right with primary color, AI messages left with surface color
- Typing indicator: Animated dots in secondary color
- Mode toggle: Pill-style segmented control (Informational/Supportive)
- Voice input: Pulsing microphone icon with audio visualization

### Emergency SOS
- Large red button: `bg-error text-white rounded-2xl p-8 text-2xl font-bold`
- Emergency contacts: Quick-dial cards with contact photos and call/message actions
- Location sharing: Map view with user pin and preset contact list

---

## Iconography
Use **Heroicons** (outline style for navigation, solid for actions) via CDN

---

## Images

**Hero Image (Welcome/Onboarding):**
- Calming gradient-mesh background with abstract wellness imagery
- Soft focus meditation/health concept photo with overlay gradient
- Position: Full viewport height with content overlay, centered vertically

**Profile/Avatar Images:**
- Circular avatars (w-12 h-12 for lists, w-24 h-24 for profiles)
- Fallback: Initials with gradient background

**Illustration Strategy:**
- Use abstract health illustrations for empty states (no medical reports, no journal entries)
- Medical report previews: Thumbnail images with document icon overlay
- Mood tracker: Emoji-style mood indicators with pastel circular backgrounds

---

## Animations & Interactions
- Page transitions: Subtle fade and slide (150ms duration)
- Loading states: Skeleton screens with shimmer effect
- Success feedback: Checkmark animation with scale bounce
- Mood selection: Gentle scale and color transition on tap
- Chart rendering: Progressive draw animation (500ms)
- No excessive animations - prioritize performance and accessibility

---

## Accessibility Features
- Minimum touch target: 44x44px for all interactive elements
- Color contrast: WCAG AA compliance minimum
- Font size controls: User-adjustable in settings (sm, base, lg, xl)
- Voice input indicators: Visual feedback for speech recognition
- Screen reader labels: Comprehensive aria-labels on all interactive elements
- Reduced motion: Respect prefers-reduced-motion media query
- High contrast mode toggle in settings

---

## Responsive Breakpoints
- Mobile: < 768px (single column, bottom nav)
- Tablet: 768px - 1024px (2-column grids, side nav optional)
- Desktop: > 1024px (3-column grids, persistent sidebar)
