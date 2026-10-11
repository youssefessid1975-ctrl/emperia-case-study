# EMPERIA

**Making high-end gaming more accessible — starting with gamer discovery and a pre-launch product.**

Founder: **Seif Essid** · Consumer cloud gaming · Early-stage project

## The project in 60 seconds

I grew up in Tunisia wanting to play competitively, but could not afford a capable gaming PC. Gaming cafés gave me access, with limits on when and how much I could play. That experience led me to investigate a broader question: **can someone choose the gaming experience they want without first understanding or buying the hardware behind it?**

EMPERIA's proposed answer is browser-based gaming with an experience-driven setup: describe the game, resolution, frame-rate target and budget, then match that request to a suitable cloud machine and network location.

The work so far centers on gamer discovery, product definition, and a documented pre-launch website with email verification, referrals and creator attribution. **The cloud gaming service and network optimizer remain proposed capabilities; this case study does not claim an operational streaming platform.**

## The problem I investigated

Conversations with gamers surfaced several different problems behind the phrase “cloud gaming is laggy”: input delay, compression artifacts, the connection to the streaming machine, and the machine's connection to the multiplayer server. Other concerns included access to games, session limits and persistent setups.

These were informal conversations, not a representative survey. They helped frame hypotheses to test rather than establish market-wide conclusions.

The resulting product question is more specific than finding a powerful GPU: **which available setup gives this player an acceptable experience for this game and budget?**

## My approach

1. Start with an understandable request, such as “I want to play at 1440p with a high frame rate within my budget.”
2. Translate it into constraints that can be checked against hardware, availability and measured network conditions.
3. Present feasible options with explicit tradeoffs and uncertainty.
4. Evaluate the player-to-cloud connection and the cloud-to-game-server connection separately.
5. Use early community participation to identify what should be built and tested first.

The exact performance targets and prices shown in product concepts are illustrations, not benchmark results or available offers.

## What exists, and what remains to build

| Area | Current evidence |
| --- | --- |
| Gamer discovery and founder reasoning | Founder-reported informal conversations and product decisions |
| Pre-launch website | Existing setup documentation describes a Next.js application with Supabase and Resend |
| Email verification | An actual HTML template is included in this repository |
| Referrals and creator attribution | Documented workflows; the current application code and live behavior have not been independently checked for this case study |
| GPU selection and network optimization | Proposed product architecture; no measured optimization result is claimed |
| Browser game streaming | Proposed capability; no playable cloud service is included here |
| Payments and creator payouts | Future integration in the available setup documentation |

## Decisions that matter

**Count a verified account separately from an email submission.** The documented onboarding flow grants membership and referral rewards after verification. This makes acquisition reporting more meaningful and avoids treating every submitted email as an acquired user.

**Use one invite-code field.** Gamer and creator codes serve different attribution purposes, but the user should not have to understand the underlying categories. The documented design detects the code type and prevents ambiguous ownership.

**Keep creator attribution distinct from payment.** An attributed signup is not a paying customer. The existing guide explicitly leaves financial metrics unavailable until payment integration exists.

**Measure the full experience.** A low ping to a cloud machine does not by itself establish a good multiplayer experience. The proposed evaluation also considers the game-server connection, jitter, loss, encoding and decoding, and frame pacing.

## My role

My contribution focuses on the problem, informal customer discovery, product requirements, user experience, and pre-launch distribution. I use AI-assisted development to turn those requirements into prototypes and collaborate on technical implementation. This case study does not imply that I personally wrote every line of application code.

## What the next experiment should establish

Compare candidate cloud regions for a fixed game, player connection and client device. Record both network legs and the observable streaming experience under repeatable conditions. Test whether choosing a different region actually improves the experience enough to justify its cost. No result from that experiment is claimed here.

## Inspect this project

- [Architecture and tradeoffs](docs/architecture.md)
- [Evidence, limitations and roadmap](docs/evidence-and-limitations.md)
- [Existing verification-email template](examples/verify-email.html)

This repository is a readable product case study. It contains no application runtime, paid-service requirement or fabricated demo screenshots.
