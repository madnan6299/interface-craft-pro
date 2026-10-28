# SaaS and ERP Dashboard Patterns

## Orient the user
Make the active module, current company/workspace, page title, and key context visible. Navigation should reflect the product's information architecture rather than a random list of features.

## Operational data
- Prioritize the tasks users perform most often.
- Give totals units, currency, timeframe, and scope when those affect interpretation.
- Distinguish zero data, missing data, loading, permission denial, and API failure.
- Keep filters and sort state visible and explain when totals reflect filtered results.
- Avoid presenting demo figures as live business data.

## Tables and workflows
- Keep row actions predictable and preserve selection when users move between relevant steps.
- Use bulk actions carefully and report the affected record count before destructive operations.
- Provide empty states that explain the next useful action.
- Preserve keyboard access and a responsive strategy for wide tables.
- Avoid replacing a functional workflow with a dashboard card just to look modern.

## Multi-tenant and permissions
Respect active company/workspace scope, role permissions, and record visibility. Do not leak cross-company information through summary cards, autocomplete, exports, or client-side filtering. Server-side authorization remains authoritative.

## Material-inspired shell
For hosting panels, admin consoles, and enterprise dashboards, structure the screen into clearly differentiated layers: optional account/system notice, product top bar, primary navigation, contextual sidebar, and main work area. Use a neutral canvas, raised white surfaces, subtle outlines, consistent spacing/radii, readable typography, and one restrained primary action color. Keep banners concise and subordinate to the task. Use a consistent icon family, pair ambiguous icons with labels, and provide selected/hover/focus/disabled states. Do not turn every section into a card or add decorative gradients without a product reason. See `material-inspired-enterprise-ui.md` for detailed rules.

## Visual quality
Dense enterprise interfaces can still feel polished through clear alignment, typography, spacing, restrained color, predictable controls, and fast feedback. Do not apply consumer-app spacing blindly to data-heavy workflows.
