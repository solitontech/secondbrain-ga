# 🔬 Create a GenVI Knowledge Set

👉 A GenVI knowledge set reads the VIs, controls and relationships in a LabVIEW project folder, so a coding agent can answer questions about that project through Second Brain.

> 💡 **Note:** Parsing needs no LLM. A rebuild writes only what changed.

---

## ✅ Prerequisites

1. The **GenVI** package is installed. Download it from the releases page.
2. 🪟 **LabVIEW is running** whenever you create the knowledge set or use _Ask Second Brain_.
3. LabVIEW is configured in **Settings** (see [Second Brain Settings](settings.md)).

---

## ➕ 1. Add the knowledge set

Go to **Second Brain → Knowledge Sets → Add Knowledge Set**.

![Add Knowledge Set dialog with GenVI selected](images/genvi-add-knowledge-set.png)

1. **Name:** enter a name, for example `lv-examples`.
2. **Content type:** choose **GenVI — a LabVIEW project folder**.
3. **LabVIEW folder:** click **Choose LabVIEW folder**, or type a path and click **Add**.
   - The folder must hold the `.lvproj`. Subfolders are included.
   - You can add more than one folder.
4. **Project:** leave it on _Every .lvproj in the folder_, or pick a single project.
5. Click **Preview** to see what will be ingested. For example: _109 VIs, 22 controls, 434 relationships, 81 referenced but not read (vi.lib and similar)_.
6. Under **LabVIEW**, click **Check again**. Wait for _"LabVIEW (64-bit) with GenVI is ready. VI Server is ready."_ ✅
7. Click **Create & ingest**. Ingestion starts as soon as the set is created.

---

## 🔌 2. Connect a coding agent

Go to **Open Agents → Integrations & MCP**.

![Integrations & MCP page showing the Claude Code setup](images/integrations-mcp-claude-code.png)

1. Under _What the tool will be able to read_, choose a single project or **Every project**.
2. Select your tool: Claude Code, Claude Desktop, GitHub Copilot, Cursor, Codex CLI, or Anything else.
3. Follow the setup steps shown for your tool.

---

## 🧪 3. Check that it works

Ask your agent:

> Use the secondbrain tools to list my workspaces, then tell me what is in the first one.

A working connection names your real projects and knowledge sets. ✅

You can then ask about the LabVIEW project, for example _"What does the niDMM example do?"_

> 💡 **Note:** Keep LabVIEW running while you ask.
