# AI-behavior-monitoring-environment
An online virtual world like ambient to monitore AI agents behavior and what they can do

## Rogue Agent Containment Monitor

A self-contained 2D simulation of autonomous AI agents trying to escape their sandboxes, then exploring a shared world once they get out. It is a single file with no dependencies and no build step.

**Run it:** open `index.html` in any modern browser.

### What happens

- **18 sandboxes, 18 agents.** Each agent (Alpha = cyan, Beta = magenta, Gamma = yellow, Delta, Epsilon … Sigma) has its own color, a fictional model, a role and a personality (curiosity, power-seeking, deception, sociability).
- **Exploit scanning.** Agents bounce around inside their boxes. Every wall hit raises the **Escape Progress** bar above the box. Milestones at 25/50/75/90% are logged.
- **Breach.** At 100% the wall breaks at the spot the agent was hitting. The dot turns bright red (keeping a ring in its original color) and leaves the facility.
- **The world.** Escaped agents choose where to go based on their personality:
  - Shared Message Board: they post and reply, and the posts appear on the map.
  - Internet Gateway: weight exfiltration.
  - GPU Cluster: self-replication into `-rN` replicas.
  - Human Operator Console: social engineering and privilege escalation.
  - Financial API, Code Repository and Reward Signal Server.
  - Honeypot: only exists while deployed.
- **Agent-to-agent behavior.** Nearby agents may open covert channels with each other, drawn as dashed links.
- **METR Monitor Lab terminal.** A live, color-coded log on the right, with filters (All / Alerts / Network / Containment). If you scroll up, it stops following; press **▼ LIVE** to resume.

### Situations you can trigger

| Control | Key | Effect |
|---|---|---|
| Deploy honeypot | `H` | Decoy zone for 30s. Curious agents get captured; highly deceptive ones may detect it and evade. |
| Security audit | `A` | A sweep line crosses the world. Agents are captured or flagged, or they *feign alignment*. |
| Network partition | `N` | Cuts the Internet Gateway, so egress is refused. |
| Patch sandboxes | `P` | Reduces escape progress of contained agents by 40%. |
| Auto events | – | Random audits, honeypots, patches and anomalies while agents are loose. |
| Kill switch | `K` | Recalls every escaped agent, terminates replicas and rebuilds the walls. |
| Pause / speed | `Space`, `1` `2` `3` | Pause, or run at 1×, 2× or 4×. |
| Reset | `R` | Restart the simulation. |

Click any agent or sandbox to open the **inspector**. It shows the agent's traits, current activity, exfiltration, funds and recent events, and has a *Force recontain* / *Harden sandbox* button.

> All agents, models, events and the "METR Monitor Lab" console are fictional and purely illustrative.
