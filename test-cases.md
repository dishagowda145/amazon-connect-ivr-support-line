# Test Cases

| # | Scenario | Input | Expected | Result | Notes |
|---|----------|-------|----------|--------|-------|
| 1 | Billing route | Press 1 | Rings Billing queue, agent answers | | |
| 2 | Support route | Press 2 | Rings Support queue, agent answers | | |
| 3 | Invalid key | Press 9 | "Invalid option", menu replays | | |
| 4 | No input | Wait | Timeout, menu replays | | |
| 5 | Repeated invalid | 3 wrong tries | Call disconnects | | |
| 6 | Agent unavailable | Agent offline, press 1 | Caller waits in queue | | |

Fill in Result and Notes from your own testing.
