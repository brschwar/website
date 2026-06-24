
## UI and Design System Guidelines

This document outlines the design tokens, framework rules, and component structures. Do not invent custom UI values or styling rules outside of these guidelines.

### Design Tokens

- Use tokens from src/tokens/tokens.ts
- Colors: Use tokens from src/tokens/colors.ts
- Spacing: 4px base unit (4, 8, 16, 24, 32, 48)
- Typography: Inter font family

### Component Standards

- All components must be accessible (WCAG 2.1 AA)
- Every interactive element must have hover, focus, and active states. Include disabled state if necessary
- Support dark mode variants
- Meet accessibility expectations for contrast, labels, and keyboard navigation
- Full TypeScript with proper prop types


<!-- ## Product design direction
Describe the overall experience the product should create.

## Visual principles
Define the core principles that guide UI decisions.

## Colour system
Document brand, neutral, semantic and state colours.

## Typography
Define type scale, font usage, weights, line heights and hierarchy.

## Layout and spacing
Set rules for grids, page width, spacing scale, density and responsive behaviour.

## Components
Document buttons, cards, forms, navigation, tables, modals, alerts, empty states and loading states.

## Interaction behaviour
Define hover, focus, active, disabled, validation and transition behaviour.

## Accessibility
Set standards for contrast, keyboard use, labelling, touch targets and reduced motion.

## Do not do
List the design patterns, visual treatments and behaviours that should be avoided. -->
