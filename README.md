<p align="center">
  <b>Scraping at scale, AI integration and the infrastructure that keeps both running.</b><br>
  Technical lead &middot; Andalusia, Spain &middot; remote, hybrid or on-site
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/daniel-benitez-garcia"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:danielbenitez0306@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## About

I lead core projects and AI integration. I design agentic systems with local LLMs and MCP, large-scale scraping platforms in Python and JavaScript, and the core infrastructure behind them, including SSO. I have cut infrastructure costs by more than 85% and I lead development teams with Scrum, focused on quality, automation and robust processes.

I am ambitious, demanding about the quality of my own work, and I enjoy working in a team to take each project beyond what was planned.

## Work I have shipped

Most of it lives in private company repositories. These are the case studies, with the engineering that matters and none of the internals.

<details open>
<summary><b>Large-scale availability scraping platform</b></summary>

- **Problem:** pull live ticket availability from 16 different tourism sources, each with its own calendar, anti-bot layer and failure modes, and feed a booking API.
- **Built:** a common scraper contract (one result format, 3 attempts, guaranteed cleanup), post-processing that normalises hours and closed days, and per-source strategy chosen by what the site actually enforces: plain HTTP, session transfer from a browser, or a full browser.
- **Result:** a reliable pipeline where a blocked source is reported as blocked instead of being silently published as "closed".
</details>

<details>
<summary><b>Anti-bot diagnosis, measured instead of guessed</b></summary>

- **Problem:** recurring blocks from enterprise WAFs that looked random.
- **Found, with evidence:** blocks tied to the session cookie and carried over by persistent browser profiles; a bare 429 that was a WAF verdict, not a rate limit; a device fingerprint banned while the IP stayed clean; country filters that silently passed everything because the exit IP was geolocated from the wrong side of the proxy.
- **Built:** detection by response body (never status alone), fail-fast on challenge states, and diagnostic capture of page, HTML and request statuses.
- **Status:** being extracted into an open, anonymised research repository.
</details>

<details>
<summary><b>Infrastructure consolidation and reliability</b></summary>

- Migrated 35 AWS servers to a single Hetzner host with a custom trigger system: **-85% cost**.
- Debugged the failures that do not show up in dashboards: a load average that looked saturated but was full utilisation of 2 cores, orphaned Chrome processes found by a PPID check, browser profiles leaking inside a snap sandbox, and zombie processes nobody reaped.
- Replaced 18 UiPath bots on Windows Server with an in-house RPA on Ubuntu.
- Rolled out corporate SSO with Authentik across all core applications.
</details>

<details>
<summary><b>AI tooling around the codebase</b></summary>

- Automatic **scraper auditing and repair** with LLMs, MCP servers and per-project skills.
- A **multi-agent system on local LLMs** (Qwen, Ollama) driven by Organic Driven Development and TDD.
- A FastAPI service hub for report analysis, Chrome profile management and device monitoring.
- GitHub governance with Actions and Claude Code / git hooks, which almost eliminated production incidents.
</details>

<details>
<summary><b>Earlier: autonomous driving</b></summary>

- Perception and control software for a driverless vehicle in Python and C++, autonomous navigation algorithms and LIDAR 3D mapping, with ARUS at the University of Seville.
</details>

## Impact in numbers

| | |
|---|---|
| **-85%** | infrastructure cost after consolidating 35 AWS servers into one Hetzner host |
| **96%** | scraper success rate on a custom scheduler |
| **~EUR 50k / year** | estimated saving from replacing 18 UiPath bots with an in-house RPA |

## Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,js,cpp,java,cs,php,fastapi,django,nodejs,react,spring,dotnet,laravel,postgres,mysql,mongodb,aws,linux,githubactions,selenium,wordpress&perline=7" alt="Core technologies">
</p>

| Area | Technologies |
|---|---|
| **AI** | `LangChain` `MCP` `Ollama` `Claude Code` `Multi-agent systems` |
| **Scraping** | `Selenium` `Playwright` `Camoufox` `Proxies` `CAPTCHA handling` |
| **Languages** | `Python` `JavaScript` `C++` `Java` `C#` `PHP` |
| **Frameworks** | `FastAPI` `Django` `Node.js` `React` `Spring` `.NET` `Laravel` |
| **Databases** | `PostgreSQL` `MySQL` `MariaDB` `MongoDB` `Oracle` |
| **Cloud and DevOps** | `AWS` `Hetzner` `Linux` `GitHub Actions` `Celery` |
| **Security** | `SSO` `Authentik` `Keycloak` |
| **Methodologies** | `Scrum` `TDD` `ODD` |
| **Other** | `UiPath` `Odoo` `WordPress` `Drupal` |
