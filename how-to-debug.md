# How to Debug

### Things to talk about

- Intro into sentry and how it works
- Intro into scout?
- How to judge importance of alerts, and how to get to a solution
- How to look at errors, how they link to specific debug duck requests.
- How to check AWS logs, split between applications
- Common SSO, email, general platform
- How to write logs
- How to use a debugger, watching variables

## Logging

### Python

logging module

```python

import logging

_LOG  = logging.getLogger(__name__)
```
