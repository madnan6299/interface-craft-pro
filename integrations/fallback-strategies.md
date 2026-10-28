# Fallback Strategies

## If a reference site is down
Use the local design foundations, visual hierarchy, interaction patterns, accessibility, and motion guides. Do not block delivery waiting for inspiration sites.

## If a package is missing
First determine whether the requested effect needs a dependency. Prefer CSS or the existing framework for simple behavior. Add a dependency only when its benefits justify bundle size, compatibility, licensing, and maintenance costs.

## If documentation is unavailable
Do not guess APIs. Inspect the installed package version, types, examples already in the repository, and lockfile. If uncertainty remains, implement a simpler known-safe option or ask for a decision.

## If a third-party component cannot be reused
Recreate the general interaction pattern using original markup and styles, accessible semantics, and the project's design system. Do not copy proprietary source or assets.

## If browser automation is unavailable
Run available static checks and tests, inspect code paths, and clearly list the unperformed manual checks. Never claim visual QA occurred without viewing the rendered result.

## If time is limited
Fix blockers and high-impact usability issues first. Defer decorative motion, nonessential dependencies, and low-impact polish.
