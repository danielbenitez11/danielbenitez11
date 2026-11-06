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

<div align="center">

| | |
|---|---|
| **-85%** | infrastructure cost after consolidating 35 AWS servers into one Hetzner host |
| **96%** | scraper success rate on a custom scheduler |
| **~EUR 50k / year** | estimated saving from replacing 18 UiPath bots with an in-house RPA |

</div>

## Tech Stack

<p align="center">
  <b>AI &amp; Agent Systems</b><br><br>
  <img src="https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=claude&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain">
  <img src="https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama">
  <img src="https://img.shields.io/badge/MCP-000000?style=for-the-badge&logo=modelcontextprotocol&logoColor=white" alt="MCP">
</p>

<p align="center">
  <b>Scraping &amp; Automation</b><br><br>
  <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white" alt="Selenium">
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge" alt="Playwright">
  <img src="https://img.shields.io/badge/Camoufox-FF7139?style=for-the-badge&logo=firefoxbrowser&logoColor=white" alt="Camoufox">
  <img src="https://img.shields.io/badge/UiPath-FA4616?style=for-the-badge&logo=uipath&logoColor=white" alt="UiPath">
</p>

<p align="center">
  <b>Languages</b><br><br>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt="C#">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP">
</p>

<p align="center">
  <b>Backend &amp; Frameworks</b><br><br>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring">
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET">
  <img src="https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel">
</p>

<p align="center">
  <b>Databases</b><br><br>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="MariaDB">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/Oracle-F80000?style=for-the-badge" alt="Oracle">
</p>

<p align="center">
  <b>Cloud &amp; DevOps</b><br><br>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge" alt="AWS">
  <img src="https://img.shields.io/badge/Hetzner-D50C2D?style=for-the-badge&logo=hetzner&logoColor=white" alt="Hetzner">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions">
  <img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white" alt="Celery">
</p>

<p align="center">
  <b>Security</b><br><br>
  <img src="https://img.shields.io/badge/SSO-555555?style=for-the-badge" alt="SSO">
  <img src="https://img.shields.io/badge/Authentik-FD4B2D?style=for-the-badge&logo=authentik&logoColor=white" alt="Authentik">
  <img src="https://img.shields.io/badge/Keycloak-4D4D4D?style=for-the-badge&logo=keycloak&logoColor=white" alt="Keycloak">
</p>

<p align="center">
  <b>CMS &amp; Business Platforms</b><br><br>
  <img src="https://img.shields.io/badge/Odoo-714B67?style=for-the-badge&logo=odoo&logoColor=white" alt="Odoo">
  <img src="https://img.shields.io/badge/WordPress-21759B?style=for-the-badge&logo=wordpress&logoColor=white" alt="WordPress">
  <img src="https://img.shields.io/badge/Drupal-0678BE?style=for-the-badge&logo=drupal&logoColor=white" alt="Drupal">
</p>

<p align="center">
  <b>Methodologies</b><br><br>
  <img src="https://img.shields.io/badge/Scrum-555555?style=for-the-badge" alt="Scrum">
  <img src="https://img.shields.io/badge/TDD-555555?style=for-the-badge" alt="TDD">
  <img src="https://img.shields.io/badge/ODD-555555?style=for-the-badge" alt="ODD">
</p>
