# Edward Radford

I build AI systems that go into real businesses and actually get used.

My main work is a multi-tenant operations platform for a sign manufacturer, sole engineer: an LLM
agent pipeline over 61 tools, plugged into the Xero and Dropbox they already had. That codebase is
the client's and is not public, so take the rest as background rather than as something you can
check from here — it carries 2,910 automated tests, and tenant isolation is enforced in Postgres
rather than in application code. The repos below are the part you can read.

Before I wrote any of that I spent four years at the same company fitting signs, running its IT and
quoting jobs with its customers. That turns out to be the useful half: the hard part of putting
software into a small business is never capability, it is getting busy people to change how they
work.

### What is here

**[companies-house-mcp](https://github.com/EdwardRadford/companies-house-mcp)** — start here. An
MCP server that gives a model read-only access to the UK Companies House register. Seven tools, not
the API's thirty, and the README is mostly about why: every tool's schema sits in the model's
context whether it is used or not, and overlapping tools are where models pick badly. Written and
tested against the published spec first, then run against the live register — there is a table of
the six things the real API did differently and what each one would have cost. Worst of them: ask
for the charges of a company that does not exist and the API returns 200 and an empty list, so the
server would have told a model the company had no debt secured against it. 127 tests, no network
and no API key needed to run them, CI on every push.

**[foldready-engine](https://github.com/EdwardRadford/foldready-engine)** — a WebKit rendering
engine that checks a site across three foldable-phone viewports and reports what breaks. Simulates
the fold as a resize without a reload, because that is what the hardware does. The SSRF guard on
the URL input now has tests; writing them found two ranges it was letting through.

**[yowzer-hub-selected](https://github.com/EdwardRadford/yowzer-hub-selected)** — selected source
from the platform above. The operator contract, the 61-tool registry and the schema. Published to
be read: it explains how an autonomous system is made legible to the person carrying the risk.

**[flightpath](https://github.com/EdwardRadford/flightpath)** — an AI study companion for UK
student pilots, built in Flutter while I was doing the training myself.

### Currently

Contracting, and open to forward deployed, solutions and applied AI engineering roles. London or
remote, happy to travel.

Milton Keynes, UK · [edwardradford.co.uk](https://edwardradford.co.uk) · contact@edwardradford.co.uk
