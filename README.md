# Enterprise Dashboard Design System

A dark-themed design system built on **shadcn/ui** (new-york style), **Tailwind CSS v4**, and **Radix UI** primitives — extracted from a Next.js 16 financial dashboard.

## Overview

This design system provides:
- Complete dark-first theme via CSS custom properties
- 50+ pre-built accessible UI components (Radix UI backed)
- Chart components powered by Recharts
- Full collapsible sidebar system
- Form primitives with React Hook Form integration
- Utility functions and hooks

## Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| Next.js | 16 | Framework |
| React | 19 | UI Library |
| Tailwind CSS | v4 | Styling |
| shadcn/ui | new-york | Component system |
| Radix UI | Various | Accessible primitives |
| Recharts | 2.x | Chart components |
| Lucide React | 0.454+ | Icons |
| class-variance-authority | 0.7+ | Variant management |
| Geist | — | Typography (sans + mono) |

---

## Design Tokens

All tokens live in `app/globals.css` as CSS custom properties. The theme is **dark-first** — no light mode by default. A standard shadcn light/dark token file is included in `styles/globals.css` for reference.

### Core Color Tokens

| Token | Value | Usage |
|---|---|---|
| `--background` | `#0a0a0a` | Page background |
| `--foreground` | `#fafafa` | Primary text |
| `--card` | `#141414` | Card surfaces |
| `--card-foreground` | `#fafafa` | Card text |
| `--popover` | `#141414` | Popover/dropdown surfaces |
| `--primary` | `#fafafa` | Primary action color |
| `--primary-foreground` | `#0a0a0a` | Text on primary |
| `--secondary` | `#1f1f1f` | Secondary surfaces |
| `--muted` | `#262626` | Muted backgrounds |
| `--muted-foreground` | `#a1a1a1` | Muted text |
| `--accent` | `#1f1f1f` | Accent surfaces |
| `--destructive` | `#7f1d1d` | Error/destructive bg |
| `--destructive-foreground` | `#fca5a5` | Error text |
| `--border` | `#262626` | Borders |
| `--input` | `#262626` | Input borders |
| `--ring` | `#525252` | Focus rings |

### Chart Colors

| Token | Hex | Color |
|---|---|---|
| `--chart-1` | `#3b82f6` | Blue |
| `--chart-2` | `#22c55e` | Green |
| `--chart-3` | `#06b6d4` | Cyan |
| `--chart-4` | `#eab308` | Yellow |
| `--chart-5` | `#8b5cf6` | Purple |

### Sidebar Tokens

| Token | Value |
|---|---|
| `--sidebar` | `#111111` |
| `--sidebar-foreground` | `#fafafa` |
| `--sidebar-primary` | `#3b82f6` |
| `--sidebar-primary-foreground` | `#fafafa` |
| `--sidebar-accent` | `#1f1f1f` |
| `--sidebar-accent-foreground` | `#fafafa` |
| `--sidebar-border` | `#262626` |
| `--sidebar-ring` | `#525252` |

### Background Variants

| Token | Value | Usage |
|---|---|---|
| `--bg-secondary` | `#171717` | Elevated card backgrounds |
| `--bg-other` | `#1f1f1f` | Nested card backgrounds |

### Border Radius

| Token | Value |
|---|---|
| `--radius` | `0.5rem` |
| `--radius-sm` | `0.25rem` |
| `--radius-md` | `0.375rem` |
| `--radius-lg` | `0.5rem` |
| `--radius-xl` | `0.75rem` |

### Typography

| Role | Font Family |
|---|---|
| Sans | Geist, Geist Fallback |
| Mono | Geist Mono, Geist Mono Fallback |

### Dashboard Container Classes

Utility classes in `app/globals.css` for consistent dashboard panels:

| Class | Description |
|---|---|
| `.dashboard-container-elevated` | Rounded card with layered elevation shadow |
| `.dashboard-container` | Standard rounded card |
| `.dashboard-container-header` | Rounded top for card headers with bottom border |
| `.dashboard-container-flat` | Flat card, no shadow |
| `.dashboard-container-nested` | Nested card using `--bg-other` background |

---

## Components

All components live in `components/ui/` following the shadcn/ui **new-york** style.

### Layout & Navigation

| Component | File | Description |
|---|---|---|
| Sidebar | `sidebar.tsx` | Full sidebar system — provider, collapsible, mobile sheet |
| NavigationMenu | `navigation-menu.tsx` | Horizontal navigation menus |
| Breadcrumb | `breadcrumb.tsx` | Breadcrumb trails |
| Pagination | `pagination.tsx` | Page navigation |
| Separator | `separator.tsx` | Visual dividers (horizontal/vertical) |
| Resizable | `resizable.tsx` | Resizable panel groups |

### Overlays & Dialogs

| Component | File | Description |
|---|---|---|
| Dialog | `dialog.tsx` | Modal dialogs |
| AlertDialog | `alert-dialog.tsx` | Confirmation dialogs |
| Sheet | `sheet.tsx` | Slide-in panels (all 4 sides) |
| Drawer | `drawer.tsx` | Vaul-powered drawers |
| Popover | `popover.tsx` | Floating content panels |
| HoverCard | `hover-card.tsx` | Hover popover cards |
| Tooltip | `tooltip.tsx` | Tooltip overlays |
| Command | `command.tsx` | Command palette (standalone + dialog) |

### Forms & Inputs

| Component | File | Description |
|---|---|---|
| Form | `form.tsx` | React Hook Form integration |
| Field | `field.tsx` | Field/fieldset components with orientation variants |
| Input | `input.tsx` | Text input |
| Textarea | `textarea.tsx` | Multi-line text input |
| Select | `select.tsx` | Dropdown select |
| Checkbox | `checkbox.tsx` | Checkbox |
| RadioGroup | `radio-group.tsx` | Radio button group |
| Switch | `switch.tsx` | Toggle switch |
| Slider | `slider.tsx` | Range slider |
| Calendar | `calendar.tsx` | Date picker (react-day-picker v9) |
| InputOTP | `input-otp.tsx` | One-time password input |
| InputGroup | `input-group.tsx` | Input with prefix/suffix addons |
| ButtonGroup | `button-group.tsx` | Grouped/joined buttons |

### Data Display

| Component | File | Description |
|---|---|---|
| Chart | `chart.tsx` | Recharts wrapper with theme-aware config |
| Table | `table.tsx` | Data table |
| Card | `card.tsx` | Content cards |
| Badge | `badge.tsx` | Status badges |
| Avatar | `avatar.tsx` | User avatars with fallback |
| Progress | `progress.tsx` | Progress bars |
| Skeleton | `skeleton.tsx` | Loading placeholders |
| Spinner | `spinner.tsx` | Loading spinner |
| Empty | `empty.tsx` | Empty state components |
| Item | `item.tsx` | List item primitives |

### Buttons & Toggles

| Component | File | Variants |
|---|---|---|
| Button | `button.tsx` | default, destructive, outline, secondary, ghost, link |
| Toggle | `toggle.tsx` | default, outline |
| ToggleGroup | `toggle-group.tsx` | Grouped toggle buttons |

### Menus

| Component | File | Description |
|---|---|---|
| DropdownMenu | `dropdown-menu.tsx` | Dropdown menus |
| ContextMenu | `context-menu.tsx` | Right-click context menus |
| Menubar | `menubar.tsx` | Application menubar |

### Feedback

| Component | File | Description |
|---|---|---|
| Toast + Toaster | `toast.tsx`, `toaster.tsx` | Radix-based toast notifications |
| Sonner | `sonner.tsx` | Sonner toast integration |
| Alert | `alert.tsx` | Inline alert messages |

### Utility

| Component | File | Description |
|---|---|---|
| Accordion | `accordion.tsx` | Collapsible content panels |
| Tabs | `tabs.tsx` | Tab navigation |
| Collapsible | `collapsible.tsx` | Simple collapsible content |
| ScrollArea | `scroll-area.tsx` | Custom scrollbars |
| Carousel | `carousel.tsx` | Embla-powered carousels |
| AspectRatio | `aspect-ratio.tsx` | Aspect ratio containers |
| Kbd | `kbd.tsx` | Keyboard shortcut display |
| Label | `label.tsx` | Form labels |

### Hooks

| Hook | File | Description |
|---|---|---|
| `useIsMobile` | `hooks/use-mobile.ts` | Returns `true` below 768px breakpoint |
| `useToast` + `toast` | `hooks/use-toast.ts` | Toast state management |

---

## Getting Started

### 1. Fork this repository

Click **Fork** at the top right, then clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/designSystem-enterpriseDashboard.git
cd designSystem-enterpriseDashboard
```

### 2. Install dependencies

```bash
pnpm install
# or: npm install / yarn install
```

### 3. Set up Tailwind CSS v4

Tailwind v4 is CSS-first — no `tailwind.config.js` needed. Just import it in your global CSS:

```css
@import 'tailwindcss';
@import 'tw-animate-css';
```

Install the PostCSS plugin:

```bash
pnpm add -D @tailwindcss/postcss tailwindcss tw-animate-css
```

Add to `postcss.config.mjs`:

```js
export default {
  plugins: {
    '@tailwindcss/postcss': {},
  },
}
```

### 4. Configure path aliases

In `tsconfig.json`:

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["./*"]
    }
  }
}
```

### 5. Copy the design tokens

Copy `app/globals.css` into your project's global stylesheet. The `@theme inline` block maps all CSS variables to Tailwind color utilities automatically — no extra config needed.

If you want a light/dark theme toggle, use `styles/globals.css` instead — it includes both `:root` (light) and `.dark` (dark) class blocks using oklch color values.

### 6. shadcn/ui configuration

`components.json` is already configured for new-york style with neutral base color. To add new shadcn components to your project:

```bash
npx shadcn@latest add <component-name>
```

### 7. Use components

```tsx
import { Button } from '@/components/ui/button'
import { Card, CardContent, CardHeader, CardTitle } from '@/components/ui/card'
import { Badge } from '@/components/ui/badge'

export function MyCard() {
  return (
    <Card>
      <CardHeader>
        <CardTitle>Portfolio Overview</CardTitle>
      </CardHeader>
      <CardContent className="flex gap-2">
        <Badge variant="secondary">+12.4%</Badge>
        <Button>View Details</Button>
      </CardContent>
    </Card>
  )
}
```

### 8. Use the Chart component

```tsx
import { ChartContainer, ChartTooltip, ChartTooltipContent } from '@/components/ui/chart'
import { LineChart, Line } from 'recharts'

const config = {
  revenue: { label: 'Revenue', color: 'var(--chart-1)' },
}

export function RevenueChart({ data }) {
  return (
    <ChartContainer config={config} className="h-64">
      <LineChart data={data}>
        <Line dataKey="revenue" stroke="var(--color-revenue)" />
        <ChartTooltip content={<ChartTooltipContent />} />
      </LineChart>
    </ChartContainer>
  )
}
```

### 9. Use the Sidebar

```tsx
import {
  SidebarProvider,
  Sidebar,
  SidebarContent,
  SidebarMenu,
  SidebarMenuItem,
  SidebarMenuButton,
} from '@/components/ui/sidebar'
import { LayoutDashboard } from 'lucide-react'

export function AppLayout({ children }) {
  return (
    <SidebarProvider>
      <Sidebar>
        <SidebarContent>
          <SidebarMenu>
            <SidebarMenuItem>
              <SidebarMenuButton isActive>
                <LayoutDashboard />
                <span>Dashboard</span>
              </SidebarMenuButton>
            </SidebarMenuItem>
          </SidebarMenu>
        </SidebarContent>
      </Sidebar>
      <main>{children}</main>
    </SidebarProvider>
  )
}
```

---

## Customizing the Theme

All tokens are in `app/globals.css`. To swap the accent color across charts and sidebar:

```css
:root {
  --sidebar-primary: #6366f1;  /* Indigo */
  --chart-1: #6366f1;
}
```

To add a light mode, add a `.light` class block with lighter hex values. Reference `styles/globals.css` for the full oklch-based light theme from shadcn defaults.

---

## File Structure

```
├── app/
│   └── globals.css          # Primary dark theme tokens + dashboard classes
├── styles/
│   └── globals.css          # Alternate light/dark theme (shadcn default, oklch)
├── components/
│   └── ui/                  # 50+ shadcn/ui components
│       ├── accordion.tsx
│       ├── alert.tsx
│       ├── button.tsx
│       ├── chart.tsx
│       ├── sidebar.tsx
│       └── ...              # (all components listed above)
├── hooks/
│   ├── use-mobile.ts        # Mobile breakpoint hook (768px)
│   └── use-toast.ts         # Toast state management
├── lib/
│   └── utils.ts             # cn() — clsx + tailwind-merge
└── components.json          # shadcn/ui CLI configuration
```

---

## License

MIT
