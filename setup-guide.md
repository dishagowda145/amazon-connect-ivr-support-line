# Setup Guide

1. **Create instance:** AWS Console > Amazon Connect > Create instance. Use "Store users within Amazon Connect", set an access URL, create an admin. Check current pricing/free tier first.
2. **Phone number:** Channels > Phone numbers > Claim a number (availability varies by region).
3. **Queues:** Routing > Queues > add `Billing` and `Support` (default hours of operation).
4. **Agent and routing profile:** Users > add an agent (security profile Agent). Routing profiles > add `BillingSupportProfile` with Voice channel and both queues. Assign it to the agent.
5. **Contact flow `Main-IVR`:** Play prompt (greeting) > Get customer input (DTMF) > option 1: Set working queue Billing > Transfer to queue; option 2: Set working queue Support > Transfer to queue; error/timeout: Play prompt "Invalid option" > back to input, then Disconnect. Save and Publish.
6. **Attach:** Phone numbers > your number > Contact flow `Main-IVR`.
7. **Test:** open the CCP, set status Available, call the number, press 1, 2, an invalid key, and wait for timeout.
8. **Troubleshoot:** enable flow logging and check CloudWatch Logs; verify agent status, routing profile queues, and the number's flow.
9. **Clean up:** release the number and delete the instance when finished to avoid charges.
