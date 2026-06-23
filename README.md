# Awesome Oracle Agentic Skills & MCP Servers

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)

A curated, product-line-organized registry of agentic skills, MCP servers, and coding-agent integrations for **all** Oracle products.

The goal is to be the definitive place to discover and install resources that let AI agents and coding assistants work with Oracle Cloud, databases, applications, and cloud services.

**Inclusion criteria:** Resources must be agent-facing or coding-assistant oriented — MCP servers, agentic skills, provider extensions, or reference implementations with a clear agent interface. General SDK docs and tutorials are out of scope. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the full quality bar.

---

## Contents

- [AI / LLM / Inference](#ai--llm--inference)
  - [OCI Generative AI](#oci-generative-ai)
  - [Oracle AI Database / Select AI](#oracle-ai-database--select-ai)
  - [OCI AI Agent Platform](#oci-ai-agent-platform)
- [Oracle Database / Autonomous Database](#oracle-database--autonomous-database)
- [Oracle APEX](#oracle-apex)
- [Oracle MySQL HeatWave](#oracle-mysql-heatwave)
- [Oracle Analytics Cloud](#oracle-analytics-cloud)
- [Oracle Kubernetes Engine (OKE)](#oracle-kubernetes-engine-oke)
- [Cloud / Orchestration / OCI Core Services](#cloud--orchestration--oci-core-services)
- [Oracle Fusion Applications](#oracle-fusion-applications)
- [Oracle Integration / Data Integrator](#oracle-integration--data-integrator)
- [Oracle Cloud Observability / Management](#oracle-cloud-observability--management)
- [Agent / IDE Integrations](#agent--ide-integrations)
- [OpenCode / Agent Skills](#opencode--agent-skills)
- [Notes](#notes)
- [Contributing](#contributing)
- [License](#license)

---

## AI / LLM / Inference

### OCI Generative AI

[OCI Generative AI](https://www.oracle.com/cloud/cloud-native/generative-ai-service/) provides managed LLMs, embeddings, and fine-tuning on Oracle Cloud Infrastructure.

- **[OCI Generative AI](https://www.oracle.com/cloud/cloud-native/generative-ai-service/)** `Official` — Managed large language models and embedding APIs on OCI.
- **[OCI Generative AI Documentation](https://docs.oracle.com/en-us/iaas/Content/generative-ai/home.htm)** `Official` — API reference, SDKs, and model deployment guides.
- **[Build an AI Agent with MCP for Invoice Resolution](https://docs.oracle.com/en/learn/oci-aiagent-mcp-server/index.html)** `Official` — Tutorial for building an OCI Generative AI agent that calls a custom MCP server.
- **[Walkthrough for Building Agents in OCI Generative AI](https://docs.oracle.com/en-us/iaas/Content/generative-ai/building-agents-walkthrough.htm)** `Official` — Guide to agents, tools, memory, and the OCI Responses API.
- **[MCP Calling in OCI Generative AI](https://docs.oracle.com/en-us/iaas/Content/generative-ai/mcp.htm)** `Official` — Documentation for calling remote MCP servers directly from OCI Generative AI.

### Oracle AI Database / Select AI

[Oracle AI Database](https://www.oracle.com/database/ai/) brings vector search, AI models, and Select AI natively into Oracle Database.

- **[Oracle AI Database](https://www.oracle.com/database/ai/)** `Official` — AI vector search, Select AI, and in-database machine learning.
- **[Select AI Documentation](https://docs.oracle.com/en/database/oracle/oracle-database/23/arpls/dbms_cloud_ai.html)** `Official` — PL/SQL reference for natural-language-to-SQL and AI agent tools.
- **[An Agent Skill that uses Kafka Java APIs for Oracle AI Database](https://blogs.oracle.com/developers/an-agent-skill-that-uses-kafka-java-apis-for-oracle-ai-database)** `Official` — Oracle agent skill for OKafka development with coding agents.
- **[Using Agent Skills to develop with Oracle AI Database](https://medium.com/oracledevs/using-agent-skills-to-develop-with-oracle-ai-database-5cdb497499d7)** `Official` — Walkthrough of installing and using Oracle DB agent skills.

### OCI AI Agent Platform

[OCI AI Agent Platform](https://www.oracle.com/cloud/cloud-native/ai-agent-platform/) is a managed service for building, deploying, and orchestrating AI agents.

- **[OCI AI Agent Platform](https://www.oracle.com/cloud/cloud-native/ai-agent-platform/)** `Official` — Managed platform for building and deploying AI agents on OCI.
- **[OCI AI Agent Platform Documentation](https://docs.oracle.com/en-us/iaas/Content/generative-ai-agents/overview.htm)** `Official` — Concepts, quickstart, and ADK reference.
- **[Add a Function Tool to an Agent using the ADK](https://docs.oracle.com/en-us/iaas/Content/generative-ai-agents/add-tool-adk.htm)** `Official` — Tutorial for registering local Python tools with OCI AI agents.
- **[Deploy Agentic AI using OCI AI Agent Platform](https://docs.oracle.com/en/solutions/deploy-agentic-ai-agent-platform/index.html)** `Official` — Reference architecture for a Fusion/Autonomous DB agent solution.

---

## Oracle Database / Autonomous Database

Resources for agentic interaction with Oracle Database, Oracle Autonomous Database, and the built-in Autonomous AI Database MCP server.

- **[Oracle SQLcl MCP Server](https://docs.oracle.com/en/database/oracle/sql-developer-command-line/25.4/sqcug/sqlcl-mcp-server.html)** `Official` — Built-in MCP server in SQLcl for local Oracle Database access.
  - Install: ships with [Oracle SQLcl](https://www.oracle.com/database/sqldeveloper/technologies/sqlcl/) or the SQL Developer VS Code extension.
- **[Oracle Database Tools MCP Server](https://www.oracle.com/mcp/)** `Official` — Cloud-native MCP server for Oracle AI Databases in OCI.
- **[Autonomous AI Database MCP Server](https://docs.oracle.com/en-us/iaas/autonomous-database-serverless/doc/mcp-server.html)** `Official` — Managed, per-database MCP endpoint built into Autonomous AI Database.
- **[oracle/mcp - Database Tools MCP Server](https://github.com/oracle/mcp/tree/main/src/dbtools-mcp-server)** `Official` — Reference Python MCP server for OCI database resources and SQL execution.
  - Install: clone `oracle/mcp`, configure OCI, run with `uv`.
- **[Oracle DB Toolkit MCP Server](https://github.com/oracle/mcp/tree/main/src/oracle-db-toolkit)** `Official` — Java-based MCP server with YAML-defined tools, vector search, and JDBC log analysis.
- **[oracle-db-skills](https://github.com/krisrice/oracle-db-skills)** `Community` — 100+ practical skills for Oracle Database agent workflows (SQLcl, containers, migrations).
  - Install: `$skill-installer https://github.com/krisrice/oracle-db-skills` (Codex) or clone to `~/.claude/skills/`.
- **[gemini-cli-extensions/oracledb](https://github.com/gemini-cli-extensions/oracledb)** `Community` — Agent skills for managing Oracle Database via Gemini CLI, Claude Code, and Codex.

---

## Oracle APEX

Resources that let agents build, inspect, and interact with Oracle APEX applications.

- **[Oracle APEX MCP Server](https://github.com/silviosotelo/oracle-apex-mcp-server)** `Community` — MCP server with 25 tools for Oracle Database and APEX metadata.
  - Install: `git clone https://github.com/silviosotelo/oracle-apex-mcp-server && cd oracle-apex-mcp-server && npm install && npm run install:claude`
- **[Building an MCP Server for APEX REST APIs](https://blog.viscosityna.com/the-code-corner/part-ii-building-the-mcp-server-connecting-oracle-apex-rest-apis-to-your-ai)** `Community` — Three-part tutorial on building an APEX HR MCP server.
- **[Oracle APEX](https://apex.oracle.com/)** `Official` — Low-code application development platform.
- **[Oracle APEX Documentation](https://docs.oracle.com/en/cloud/paas/apex/)** `Official` — Official docs for building and extending APEX apps.

---

## Oracle MySQL HeatWave

MCP servers and agentic resources for MySQL HeatWave and MySQL AI.

- **[MySQL HeatWave MCP Server](https://github.com/oracle/mcp/tree/main/src/mysql-mcp-server)** `Official` — Python MCP server for MySQL AI and HeatWave ML/GenAI.
  - Install: clone `oracle/mcp`, follow the MySQL server README.
- **[MySQL HeatWave and MySQL AI integration with MCP](https://blogs.oracle.com/mysql/mysql-heatwave-and-mysql-ai-integration-with-model-context-protocol)** `Official` — Blog overview of HeatWave MCP tools and RAG workflows.
- **[Using MySQL HeatWave as a knowledge base with OCI AI Agent Platform](https://blogs.oracle.com/mysql/using-mysql-heatwave-as-a-knowledge-base-with-the-oci-ai-agent-platform)** `Official` — Tutorial for wiring HeatWave vector stores into OCI agents.
- **[MySQL HeatWave](https://www.oracle.com/mysql/heatwave/)** `Official` — Unified OLTP, analytics, ML, and GenAI service for MySQL.

---

## Oracle Analytics Cloud

Resources for agentic analytics and natural-language querying of Oracle Analytics Cloud.

- **[Oracle Analytics Cloud MCP Server](https://docs.oracle.com/en/cloud/paas/analytics-cloud/acsdv/oracle-analytics-cloud-mcp-server-preview.html)** `Official` — Preview MCP server for discovering, describing, and querying OAC content.
- **[Oracle Analytics Cloud MCP Server: Bridging Enterprise Analytics and AI](https://blogs.oracle.com/analytics/oracle-analytics-cloud-mcp-server-bridging-enterprise-analytics-and-ai)** `Official` — Announcement and use cases for the OAC MCP server.
- **[Oracle Analytics Cloud](https://www.oracle.com/business-analytics/analytics-cloud/)** `Official` — Enterprise analytics and business intelligence platform.
- **[Oracle Analytics Cloud Documentation](https://docs.oracle.com/en/cloud/paas/analytics-cloud/index.html)** `Official` — Official docs for OAC development and administration.

---

## Oracle Kubernetes Engine (OKE)

MCP servers and agentic resources for managing OKE clusters and workloads.

- **[oke-mcp-server](https://github.com/ronsevetoci/oke-mcp-server)** `Community` — MCP server to inspect, query, and troubleshoot OKE clusters.
  - Install: `uvx oke-mcp-server --transport stdio`
- **[Deploying an MCP Server on OCI Kubernetes Engine](https://blogs.oracle.com/ai-and-datascience/deploying-an-mcp-server-on-oci-kubernetes-engine-oke)** `Official` — Blog guide for running MCP workloads on OKE.
- **[Oracle Container Engine for Kubernetes (OKE)](https://www.oracle.com/cloud/cloud-native/kubernetes-engine/)** `Official` — Managed Kubernetes service on OCI.
- **[OKE Documentation](https://docs.oracle.com/en-us/iaas/Content/ContEng/home.htm)** `Official` — Cluster operations, add-ons, and workload management docs.

---

## Cloud / Orchestration / OCI Core Services

MCP servers and skills for OCI compute, networking, storage, identity, and core services.

- **[oracle/mcp](https://github.com/oracle/mcp)** `Official` — Reference MCP servers for OCI Compute, Networking, Storage, Identity, Logging, Monitoring, and more.
  - Install: clone, configure OCI, run individual servers with `uvx`.
- **[OCI Agent Skills](https://github.com/acedergren/oci-agent-skills)** `Community` — Expert OpenCode/Claude Code skills for OCI compute, networking, databases, IAM, and FinOps.
- **[OCI API MCP Server](https://github.com/oracle/mcp/tree/main/src/oci-api-mcp-server)** `Official` — Generic OCI API invocation MCP server.
- **[Oracle Cloud Infrastructure](https://www.oracle.com/cloud/)** `Official` — Oracle Cloud Infrastructure home page.

---

## Oracle Fusion Applications

Resources for building and extending AI agents in Oracle Fusion Applications.

- **[Oracle AI Agent Studio for Fusion Apps](https://blogs.oracle.com/fusioninsider/new-oracle-ai-agent-studio-for-fusion-apps)** `Official` — Agent design studio for Fusion ERP, HCM, SCM, and CX.
- **[Oracle AI Agent Studio Documentation](https://docs.oracle.com/en/cloud/saas/fusion-ai/aiaas/get-started.html)** `Official` — Get-started guide for building Fusion agents.
- **[Integrate Oracle Fusion AI Agent Studio with Autonomous DB MCP Server](https://www.ateam-oracle.com/integrate-oracle-fusion-ai-agent-studio-with-autonomous-db-mcp-server)** `Community` — A-Team blog on connecting Fusion AI Agent Studio to Autonomous DB MCP.
- **[Oracle Fusion Applications](https://www.oracle.com/applications/)** `Official` — Cloud ERP, HCM, SCM, and CX suites.

---

## Oracle Integration / Data Integrator

Resources that expose Oracle Integration and data integration services to agents through MCP.

- **[Oracle Integration as an MCP Server](https://docs.oracle.com/en/cloud/paas/application-integration/int-get-started/oracle-integration-mcp-server.html)** `Official` — Expose OIC integrations as MCP tools.
- **[Use Integrations as Tools in an MCP Server](https://docs.oracle.com/en/cloud/paas/application-integration/aiagents/use-integrations-tools-mcp-server.html)** `Official` — Step-by-step guide to enable MCP for an OIC project.
- **[Agentic AI in Oracle Integration](https://blogs.oracle.com/integration/agentic-ai-in-oic-overview-and-introduction)** `Official` — Overview of AI agents and MCP in OIC.
- **[Oracle Data Integrator Documentation](https://docs.oracle.com/en/middleware/fusion-middleware/data-integrator/)** `Official` — Official docs for Oracle Data Integrator agents and workflows.

---

## Oracle Cloud Observability / Management

MCP servers and agentic resources for monitoring, security, and managing OCI operations.

- **[OCI Cloud Guard MCP Server](https://github.com/oracle/mcp/tree/main/src/oci-cloud-guard-mcp-server)** `Official` — MCP server for listing and updating OCI Cloud Guard security problems.
  - Install: `uvx oracle.oci-cloud-guard-mcp-server`
- **[OCI Monitoring MCP Server](https://github.com/oracle/mcp/tree/main/src/oci-monitoring-mcp-server)** `Official` — MCP server for metrics, alarms, and monitoring queries.
- **[Oracle Cloud Observability and Management Platform](https://www.oracle.com/manageability/)** `Official` — Full-stack monitoring and management for OCI and multicloud.
- **[Oracle Cloud Guard](https://www.oracle.com/cloud/security/cloud-guard/)** `Official` — Cloud-native security posture and threat detection service.

---

## Agent / IDE Integrations

Coding agents and IDEs with native or community Oracle support.

- **[Claude Code + Oracle](https://github.com/silviosotelo/oracle-apex-mcp-server)** `Community` — Use Claude Code with the Oracle APEX MCP server for database operations.
  - Install: configure `oracle-apex-mcp-server` in Claude Code MCP settings.
- **[Continue.dev OCI Generative AI Provider](https://docs.continue.dev/customize/model-providers/more/oci)** `Community`/`Official` — Continue provider for OCI Generative AI endpoints.
- **[Oracle SQL Developer Extension for VS Code](https://www.oracle.com/database/sqldeveloper/technologies/vscode-extension/)** `Official` — VS Code extension that bundles SQLcl and its MCP server for Copilot.
- **[Configure MCP Server in AI Agent Application](https://docs.oracle.com/en-us/iaas/autonomous-database-serverless/doc/configure-mcp-server-ai-agent-application.html)** `Official` — Oracle docs for wiring Autonomous DB MCP into Claude Desktop, Cline, and other clients.

---

## OpenCode / Agent Skills

OpenCode-compatible and installable agent skill collections that target Oracle products.

- **[oracle-db-skills](https://github.com/krisrice/oracle-db-skills)** `Community` — 100+ standalone skills for Oracle Database agent workflows.
  - Install: `$skill-installer https://github.com/krisrice/oracle-db-skills` or clone to `~/.claude/skills/`.
- **[oci-agent-skills](https://github.com/acedergren/oci-agent-skills)** `Community` — OCI agent skills for compute, networking, databases, IAM, and FinOps.
  - Install: clone into `~/.config/opencode/skills/oci-agent-skills/` or equivalent agent skills directory.
- **[oracle/skills](https://github.com/oracle/skills)** `Official` — Oracle-wide skills organized by domain (db, oci, apex, fusion, graal).
  - Install: `npx skills add oracle/skills/db` or clone to agent skills directory.
- **[gemini-cli-extensions/oracledb](https://github.com/gemini-cli-extensions/oracledb)** `Community` — Cross-agent skills for Oracle Database query, schema exploration, and monitoring.

---

## Notes

- **MCP server availability:** Oracle's official MCP ecosystem is rapidly expanding. Many OCI service MCP servers live in the [oracle/mcp](https://github.com/oracle/mcp) repository as reference implementations; they are intended for exploration and prototyping unless otherwise noted as production-ready.
- **Community entries:** Some entries are community-maintained. Please verify compatibility and security posture before connecting them to production data.
- **Placeholder-like official docs:** Where a dedicated MCP server does not yet exist, official Oracle documentation and tutorials are listed so agents can still learn the product and invoke APIs correctly.
- **Updates welcome:** If you find a new Oracle MCP server or skill, see [CONTRIBUTING.md](./CONTRIBUTING.md) and open a pull request.

---

## Contributing

Read [CONTRIBUTING.md](./CONTRIBUTING.md) for the quality bar, entry format, and PR process.

---

## License

This list is released into the public domain under [CC0-1.0](./LICENSE).

## Need implementation help?

Enterprise AI Atlas is maintained by [Vibe Coding Agency](https://vibecodingagency.com). If your team needs support designing, building, or deploying production AI systems covered in this atlas, [get in touch](https://vibecodingagency.com).
