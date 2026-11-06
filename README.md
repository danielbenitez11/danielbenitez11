<h1 align="center">Daniel Benítez</h1>

<p align="center">
  <b>Scraping at scale, AI integration and the infrastructure that keeps both running.</b><br>
  Technical lead &middot; Andalusia, Spain &middot; remote, hybrid or on-site
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/daniel-benitez-garcia"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
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

**AI**
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat&logo=claude&logoColor=white)
![Multi-agent](https://img.shields.io/badge/Multi--agent_systems-555555?style=flat)

**Scraping**
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat&logo=selenium&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![Camoufox](https://img.shields.io/badge/Camoufox-FF7139?style=flat&logo=firefoxbrowser&logoColor=white)
![Proxies](https://img.shields.io/badge/Proxies-555555?style=flat)
![CAPTCHA](https://img.shields.io/badge/CAPTCHA_handling-555555?style=flat)

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat&logo=dotnet&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)

**Frameworks**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat&logo=django&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat&logo=spring&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat&logo=dotnet&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=flat&logo=laravel&logoColor=white)

**Databases**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat&logo=oracle&logoColor=white)

**Cloud and DevOps**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat&logo=hetzner&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)

**Security**
![Authentik](https://img.shields.io/badge/Authentik-FD4B2D?style=flat&logo=authentik&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=flat&logo=keycloak&logoColor=white)

**Methodologies**
![Scrum](https://img.shields.io/badge/Scrum-555555?style=flat)
![TDD](https://img.shields.io/badge/TDD-555555?style=flat)
![ODD](https://img.shields.io/badge/ODD-555555?style=flat)

**Other**
![UiPath](https://img.shields.io/badge/UiPath-FA4616?style=flat&logo=uipath&logoColor=white)
![Odoo](https://img.shields.io/badge/Odoo-714B67?style=flat&logo=odoo&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-21759B?style=flat&logo=wordpress&logoColor=white)
![Drupal](https://img.shields.io/badge/Drupal-0678BE?style=flat&logo=drupal&logoColor=white)
