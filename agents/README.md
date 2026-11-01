# Specialist Agents

Interface Craft Pro includes four specialist agent profiles under `.github/agents/`. They are written as GitHub Copilot custom-agent Markdown profiles and can also be used as portable role instructions in other coding agents.

| Agent | Responsibility | Delegate when |
|---|---|---|
| UI UX Design Director | Audit, design direction, design tokens, UX architecture, acceptance criteria | Starting a redesign or new product interface |
| Spline Scene Artist | Spline 3D/Hana scene planning, object hierarchy, materials, lighting, animation and interactions | A real 3D/interactive scene is part of the brief |
| Creative Motion Engineer | Spline web integration, frontend motion, responsive behavior, loading and fallback | Implementing the approved scene and motion in the app |
| UI Quality Auditor | Independent accessibility, responsive, visual, functional and performance review | Before sign-off or after a significant UI change |

## Suggested handoff

1. **Design Director** creates the brief, primary design direction, token plan, and acceptance criteria.
2. **Spline Scene Artist** builds or specifies the scene only if 3D materially improves the experience.
3. **Creative Motion Engineer** integrates the real export and builds resilient page behavior.
4. **Quality Auditor** reviews the complete experience and returns severity-ranked findings.
5. The lead coding agent resolves P0/P1 issues, reruns checks, and reports what was actually verified.

## Important operating rules

- Read the root `SKILL.md` and relevant references before work.
- Agents are role definitions, not proof that a tool or external account is connected.
- Spline MCP setup and authorization must be completed by the user in a compatible client. Follow the official guide: https://docs.spline.design/generate/spline-mcp-server
- Never invent scene URLs, MCP endpoints, test results, or published assets.
- Do not publish scenes, change sharing permissions, or overwrite user assets without explicit approval.
- If the target coding agent does not support `.github/agents/`, copy the relevant profile into that agent's role/instructions field.
