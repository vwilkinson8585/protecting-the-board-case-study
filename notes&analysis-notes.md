Sharp Play Detection — Case Study Notes
by Vincent Wilkinson Jr.

Purpose
- Review a small, fake dataset of NBA + NFL style entries.
- Spot sharp, coordinated, or high-risk behavior.
- Think through what I’d do on the Game Ops / Risk side.

Dataset
- 8 mock entries from fictional users.
- Columns: EntryID, UserID, Sport, Type, Stake, Time, Legs.
- Mix of normal behavior and intentional “spicy” patterns so I can show my thought process.

Pattern 1 — Coordinated Same-Entry Behavior (E001–E003)
What stood out:
- Three different users ran the exact same 5-leg Power entry within a two-minute window.
- Same players, same order, same everything.

Why it matters:
- Could be a tout pick that got blasted out.
- Could be a Discord/Telegram group moving together.
- Could be a small sharp group that found an edge before the line moved.

My approach:
- Flag the pattern.
- Check if any legs were mispriced.
- Review user histories to see if they usually travel as a group.
- Decide if this is harmless coordinated play or something that needs limits / closer monitoring.

Pattern 2 — Injury News Spike (E004–E005)
Context:
- At 12:17 PM a starting RB gets ruled OUT.
- Minutes later, multiple users hammer “Over” plays tied to that backfield.

Why it matters:
- Board is vulnerable between the news dropping and projections updating.
- Classic window where sharps attack stale numbers.

My approach:
- Freeze the related props for a quick review.
- Adjust projections and re-open at a safer number.
- Review entries from that 12:17–12:22 window.
- Tag users who constantly hunt injury-based edges.

Pattern 3 — Correlated NBA Stack (E006)
What I see:
- One entry stacks:
  - Vince Carter Over points
  - Jason Kidd Over assists
  - Richard Jefferson Over threes
  - Plus a defensive Under on Kenyon Martin

Why it’s risky:
- That’s basically a full game script. If the script hits, multiple legs hit together.
- User gets a boosted win probability without paying extra cost.

My approach:
- Review whether these legs should be allowed together.
- Track how often users build this type of correlated stack.
- Consider rule tweaks if correlation becomes too easy to abuse.

Pattern 4 — Market Lag / Mispriced Props (E007–E008)
Context:
- Market example:
  - Marshawn Lynch: 67.5 RY everywhere else, 59.5 on this board.
  - Michael Vick: 276.5 PY everywhere, 264.5 here.
- Two users instantly slam Overs on the off-market numbers.

Why it matters:
- Textbook sharp behavior: find lagging lines and hit them before they move.
- If this repeats, it’s a signal that these users (or their group) are watching multiple books closely.

My approach:
- Move the bad numbers quickly and log the adjustment.
- Cross-check against projections and other major books.
- Track users who repeat this behavior.
- Add notes for future monitoring or limits if needed.

Operational Recommendations (from the deck)
- Freeze props fast during injury events.
- Speed up market alignment vs. major books.
- Tag and track coordinated patterns.
- Add simple correlation alerts for stacked entries.
- Build behavior profiles (sharps, casuals, injury-edge hunters, market-lag hunters).
- Move lines quickly and confidently instead of waiting until after the damage.

Summary
- This project is my way of showing how I naturally break down entries, read behavior, and think about protecting the board.
- I enjoy catching the small details most people ignore and turning them into clear actions for the ops team.
