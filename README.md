# Amazon Connect IVR Support Line

A basic cloud contact center built with **Amazon Connect**. Callers hear a menu and are routed to a **Billing** or **Support** queue, where an agent answers using the browser softphone (Contact Control Panel).

![Call flow](docs/call-flow.svg)

## Features
- Greeting and DTMF menu (press 1 for Billing, 2 for Support)
- Two queues with a shared routing profile
- Invalid and timeout handling: menu replays, then disconnects after retries
- Agent handoff through the Contact Control Panel (CCP)

## Tech
Amazon Connect (contact flows, queues, routing profiles, users), AWS Console, CloudWatch Logs

## Repository contents
| Path | What it is |
|------|-----------|
| `docs/setup-guide.md` | Step-by-step configuration |
| `docs/test-cases.md` | Test scenarios and results |
| `docs/call-flow.svg` | Call flow diagram |
| `screenshots/` | Flow designer, queues, routing profile, test call |

## Screenshots
<!-- Replace with your own once built, e.g. ![Contact flow](screenshots/contact-flow.png) -->
_Add: contact flow, queues, routing profile, CCP during a test call._

## Test results
See [docs/test-cases.md](docs/test-cases.md).

## Troubleshooting notes
_Add one real issue you hit and how you fixed it (for example: agent not set to Available, queue missing from the routing profile, or the flow not attached to the phone number)._

## What I learned
_Add 2-3 lines in your own words._

## Next steps
- Business hours and hours-of-operation checks
- Voicemail or callback option
- AWS Lambda + DynamoDB customer lookup
