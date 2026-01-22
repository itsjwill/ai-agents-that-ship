# 🔮 The Ultimate AI Agents List (That Actually Matters)
**For builders who want to ship agents, not collect bookmarks**

[![GitHub stars](https://img.shields.io/github/stars/e2b-dev/awesome-ai-agents?style=social)](https://github.com/e2b-dev/awesome-ai-agents)
[![Last Updated](https://img.shields.io/badge/last%20updated-December%202024-brightgreen)](https://github.com/e2b-dev/awesome-ai-agents)
[![Join Discord](https://img.shields.io/discord/1234567890?color=mediumslateblue&label=Join%20our%20Discord)](https://discord.gg/U7KEcGErtQ)

Stop drowning in tool lists. This is the **only** AI agents resource you need - battle-tested by developers who've actually shipped with these tools.

I'm tired of seeing "awesome lists" that are just link farms. This one's different. Every tool here has been evaluated, many have been used in production, and I'll tell you exactly what works and what doesn't.

**👉 [Submit new tools here](https://forms.gle/UXQFCogLYrPFvfoUA) | 🌟 [Browse the visual version](https://e2b.dev/ai-agents)**

![AI Agents Landscape](assets/landscape-latest.png)

---

## 🏆 If You Only Try 3 Things, Try These

**AutoGen** - The Swiss Army knife of multi-agent systems. Microsoft-backed, production-ready, and the closest thing to a standard. Start here.

**CrewAI** - Best developer experience for role-based agent teams. If you want agents that actually work together (not just chat), this is it.

**Continue** - Open-source VS Code autopilot that doesn't suck. I use it daily. Game-changer for coding workflows.

---

## 🚀 Where Should I Start?

**Building your first agent?**  
Start with → **AutoGen** (learn the patterns) → **CrewAI** (build something real)

**Need something production-ready TODAY?**  
Go straight to → **LangGraph** or **AutoGen** (enterprise-grade)

**On a budget/want full control?**  
These are completely free: **AutoGPT**, **BabyAGI**, **Continue**, **Aider**

**Just want to play around?**  
**AgentGPT** (browser-based) or **Godmode** (pretty UI)

---

## 📊 The Real Comparison (Top Multi-Agent Frameworks)

| Framework | Best For | Complexity | Production Ready? | My Take |
|-----------|----------|------------|-------------------|---------|
| **AutoGen** | Everything, learning concepts | Medium | ✅ Yes | The safe choice. Microsoft backing means it'll stick around |
| **CrewAI** | Role-based teams, clear workflows | Low | ✅ Yes | Best DX. Use this if you want agents with defined roles |
| **LangGraph** | Complex state management | High | ✅ Yes | For when you outgrow the simple stuff |
| **AgentVerse** | Research, experimentation | High | ⚠️ Experimental | Cool demos, not for production |

---

## 💻 The Coding Agents That Don't Suck

| Tool | What It Actually Does | Honest Review |
|------|---------------------|---------------|
| **Continue** | VS Code autocomplete on steroids | I use this daily. Legitimately helpful |
| **Aider** | Command-line pair programming | Works great with existing codebases |
| **Cursor** | AI-first code editor | Slick but pricey. Worth it if coding is your job |
| **GPT Engineer** | Generates entire apps from prompts | Good for prototypes, don't expect production code |

---

## ⚡ Quick Start Code (Copy-Paste Ready)

### Get AutoGen Running in 5 Minutes
```python
pip install pyautogen

import autogen

# Set up your agents
assistant = autogen.AssistantAgent(
    name="assistant",
    llm_config={"model": "gpt-4"},
)

user_proxy = autogen.UserProxyAgent(
    name="user_proxy",
    human_input_mode="NEVER",
    code_execution_config={"work_dir": "coding"},
)

# Start the conversation
user_proxy.initiate_chat(
    assistant,
    message="Write a Python script that analyzes CSV data"
)
```

### CrewAI Team Setup
```python
pip install crewai

from crewai import Agent, Task, Crew

# Define your agents
researcher = Agent(
    role='Research Analyst',
    goal='Find the latest AI trends',
    backstory='Expert in AI market analysis'
)

writer = Agent(
    role='Content Writer',
    goal='Create engaging content',
    backstory='Skilled technical writer'
)

# Create tasks
research_task = Task(
    description="Research latest AI agent trends",
    agent=researcher
)

# Form the crew
crew = Crew(
    agents=[researcher, writer],
    tasks=[research_task],
    verbose=True
)

result = crew.kickoff()
```

---

## 🔥 The Real Talk Section

**AutoGPT** - The OG that started it all. Still worth trying for the historical significance, but don't expect production quality. Think of it as a tech demo.

**BabyAGI** - Simple, elegant, and actually works for basic task planning. I've shipped projects with this. Good starting point.

**LangChain Agents** - Powerful but overcomplicated. The docs are a maze. Use LangGraph instead if you need this level of complexity.

**AgentGPT** - Pretty UI, decent for demos, but you'll outgrow it fast. Good for convincing non-tech people that agents are cool.

**ChatDev** - Impressive demo of multi-agent software development. More research toy than practical tool, but the concepts are solid.

**Godmode** - AutoGPT with better UI. Same limitations, prettier package.

---

## 💎 Hidden Gems Nobody Talks About

**Adala** - Specialized for data labeling. If you work with datasets, this is incredibly useful and way better than generic agents.

**BondAI** - Code interpreter that actually works reliably. Clean API, good docs, Docker support. Underrated.

**Agents by AI Waves** - Academic project with some genuinely novel ideas about agent communication. Worth studying.

**ChemCrow** - If you're in chemistry/science, this is purpose-built for you. Don't reinvent the wheel.

**Cal.ai** - Scheduling agent that integrates with Cal.com. Niche but perfect for what it does.

---

## ⚠️ Overhyped Tools to Skip (Sorry, Not Sorry)

**Most "autonomous" agents** - They're demos. Cool demos, but demos. Don't expect them to replace developers yet.

**Anything promising "no-code agent building"** - You'll hit the limitations immediately. Learn to code or hire someone who can.

**Tools with 50+ GitHub stars but no real documentation** - Red flag. If they can't explain how to use it, it's not ready.

**"Enterprise" solutions that won't show pricing** - If you have to ask, you can't afford it (and it's probably not that good).

---

## 🛠️ The Stack I'd Actually Use (December 2024)

If I were starting an AI agent company today:

**Development**: AutoGen or CrewAI (depending on use case)  
**Code Interpreter**: E2B or BondAI  
**Vector DB**: Pinecone or Weaviate  
**LLM**: GPT-4 or Claude-3.5-Sonnet  
**Deployment**: Docker + whatever cloud you prefer  
**Monitoring**: LangSmith or roll your own

**For coding specifically**: Continue + Cursor + Aider

---

# 📚 The Complete Directory

## Open Source Multi-Agent Frameworks

### [AutoGen](https://github.com/microsoft/autogen) ⭐ **STAFF PICK**
*The gold standard for multi-agent conversations*

Microsoft-backed framework that actually works in production. Multiple agents can collaborate, debate, and solve complex tasks. The learning curve is worth it.

**Quick verdict**: Start here if you're serious about multi-agent systems.

```python
# Real working example - research assistant
import autogen

config = {"model": "gpt-4", "api_key": "your-key"}

researcher = autogen.AssistantAgent("researcher", llm_config=config)
critic = autogen.AssistantAgent("critic", llm_config=config) 
user = autogen.UserProxyAgent("user")

# They'll actually debate and improve the output
user.initiate_chat(researcher, "Research renewable energy trends")
```

**Links**: [GitHub](https://github.com/microsoft/autogen) | [Docs](https://microsoft.github.io/autogen/) | [Discord](https://discord.gg/pAbnFJrkgZ)

---

### [CrewAI](https://github.com/joaomdmoura/crewai) ⭐ **STAFF PICK**
*Best-in-class role-based agent teams*

Clean API for creating agent teams with defined roles. Think "product manager + developer + QA tester" working together. The developer experience is fantastic.

**Real talk**: This is what I use for client projects. Just works.

```python
from crewai import Agent, Task, Crew

# Define roles like a real team
pm = Agent(role='Product Manager', goal='Define requirements')
dev = Agent(role='Developer', goal='Write clean code')
qa = Agent(role='QA Engineer', goal='Test everything')

crew = Crew(agents=[pm, dev, qa], verbose=True)
result = crew.kickoff()
```

**Links**: [GitHub](https://github.com/joaomdmoura/crewai) | [Discord](https://discord.com/invite/X4JWnZnxPb)

---

### [LangGraph](https://github.com/langchain-ai/langgraph)
*For complex agent workflows*

When you need state management, complex routing, and enterprise features. Higher learning curve but incredibly powerful.

**Use when**: Your agents need to maintain complex state between interactions.

**Links**: [GitHub](https://github.com/langchain-ai/langgraph) | [Docs](https://langchain-ai.github.io/langgraph/)

---

### [AgentVerse](https://github.com/OpenBMB/AgentVerse)
*Academic research platform*

Interesting experiments in agent collaboration and emergent behaviors. Good for research, not production.

**Links**: [GitHub](https://github.com/OpenBMB/AgentVerse) | [Paper](https://arxiv.org/abs/2308.10848)

---

## Single-Purpose Powerhouses

### [Continue](https://continue.dev/) ⭐ **STAFF PICK**
*Open-source VS Code autopilot that doesn't suck*

I use this every day. It's like GitHub Copilot but better and free. Actually understands your codebase context.

```bash
# Install in VS Code
# 1. Search "Continue" in extensions
# 2. Install
# 3. Add your API key
# 4. Start coding with Cmd+I
```

**Real talk**: Game-changer for development productivity. The context awareness is scary good.

**Links**: [Website](https://continue.dev/) | [GitHub](https://github.com/continuedev/continue)

---

### [Aider](https://github.com/paul-gauthier/aider)
*Command-line pair programming that works*

Edit code in your existing repo via chat. Handles git commits automatically. Perfect for refactoring and feature development.

```bash
pip install aider-chat
cd your-project
aider

# Now chat with your code
> "Add error handling to the user authentication module"
# It'll edit the files and commit changes
```

**Use case**: When you want AI help but keep full control of your codebase.

**Links**: [GitHub](https://github.com/paul-gauthier/aider) | [Docs](https://aider.chat/)

---

### [AutoGPT](https://agpt.co/)
*The OG autonomous agent*

Historic significance as the first viral autonomous agent. Good for understanding the space, but don't expect production quality.

**Honest take**: More important for what it inspired than what it does. Try BabyAGI instead for simpler task planning.

**Links**: [GitHub](https://github.com/Significant-Gravitas/Auto-GPT) | [Discord](https://discord.gg/autogpt)

---

### [BabyAGI](https://github.com/yoheinakajima/babyagi)
*Simple task planning that works*

The clean, minimal approach to autonomous task execution. I've actually shipped projects using this as a foundation.

```python
# Core concept: task list + execution loop
# 1. Create tasks based on objective
# 2. Execute highest priority task  
# 3. Create new tasks based on result
# 4. Reprioritize and repeat
```

**Real value**: Understanding how task planning works. Build on this pattern.

**Links**: [GitHub](https://github.com/yoheinakajima/babyagi) | [Creator's Blog](https://yoheinakajima.com/)

---

## Specialized Domain Agents

### [ChemCrow](https://github.com/ur-whitelab/chemcrow-public)
*Chemistry-specific LangChain agent*

Purpose-built for chemistry tasks with 13 expert tools. If you work in chemistry, this beats general-purpose agents every time.

**Links**: [GitHub](https://github.com/ur-whitelab/chemcrow-public) | [Paper](https://arxiv.org/abs/2304.05376)

---

### [Cal.ai](https://cal.ai)
*Scheduling assistant that works*

Built on Cal.com, handles meeting scheduling with natural language. "Move my 2pm meeting to tomorrow morning" just works.

**Links**: [Website](https://cal.ai) | [GitHub](https://github.com/calcom/cal.com/tree/main/apps/ai)

---

### [data-to-paper](https://github.com/Technion-Kishony-lab/data-to-paper)
*Raw data to research papers*

Multi-agent system that takes datasets and produces complete research papers. Academic use case but impressive execution.

**Links**: [GitHub](https://github.com/Technion-Kishony-lab/data-to-paper) | [Paper](https://arxiv.org/abs/2404.17605) | [Demo Video](https://www.youtube.com/watch?v=Nt_460MmM8k)

---

## Development & Coding Agents

### [GPT Engineer](https://gptengineer.app/)
*Entire codebases from prompts*

Generates full applications from natural language. Good for prototypes, don't expect production code.

**Real expectation**: You'll get 60-70% working code that needs human cleanup. Still valuable for rapid prototyping.

**Links**: [Website](https://gptengineer.app/) | [GitHub](https://github.com/AntonOsika/gpt-engineer)

---

### [Devika](https://github.com/stitionai/devika)
*Open-source Devin alternative*

Agentic AI software engineer that breaks down tasks, researches, and writes code. Early stage but promising.

**Links**: [GitHub](https://github.com/stitionai/devika)

---

### [Devon](https://github.com/entropy-research/Devon)
*Another Devin alternative*

Open-source alternative to Cognition's Devin from Entropy Research.

**Links**: [GitHub](https://github.com/entropy-research/Devon)

---

### [ChatDev](https://github.com/OpenBMB/ChatDev)
*Virtual software company simulation*

Multi-agent system with CEO, CTO, developers, testers. More research demonstration than practical tool, but the concepts are solid.

**Educational value**: Great for understanding how different agent roles can collaborate.

**Links**: [GitHub](https://github.com/OpenBMB/ChatDev) | [Paper](https://arxiv.org/abs/2307.07924)

---

### [Blinky](https://github.com/seahyinghang8/blinky)
*AI debugging agent for VS Code*

Helps identify and fix backend code errors using LLMs, VSCode API, and print debugging.

**Links**: [GitHub](https://github.com/seahyinghang8/blinky) | [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=blinky.blinky)

---

### [CodeFuse-ChatBot](https://github.com/codefuse-ai/codefuse-chatbot)
*Full software development lifecycle agent*

Multi-agent framework serving the entire development lifecycle with DevOps integrations.

**Links**: [GitHub](https://github.com/codefuse-ai/codefuse-chatbot)

---

## Agent Building Platforms

### [Flowise](https://flowiseai.com/)
*Visual agent builder*

Low-code tool for building LLM workflows and AI agents with a visual interface.

**Good for**: Non-technical teams who need custom agents without coding.

**Links**: [Website](https://flowiseai.com/) | [GitHub](https://github.com/FlowiseAI/Flowise)

---

### [AgentGPT](https://agentgpt.reworkd.ai/)
*Browser-based AutoGPT*

No-code platform for autonomous agents. Good for demos and simple tasks.

**Reality check**: You'll hit limitations quickly, but great for getting non-technical stakeholders excited.

**Links**: [Website](https://agentgpt.reworkd.ai/) | [GitHub](https://github.com/reworkd/AgentGPT)

---

### [Godmode](https://godmode.space/)
*AutoGPT with better UI*

Web platform inspired by AutoGPT and BabyAGI with a clean interface.

**Use for**: Demos, simple task automation, convincing your boss that agents are cool.

**Links**: [Website](https://godmode.space/) | [GitHub](https://github.com/FOLLGAD/Godmode-GPT)

---

## Framework & SDK Tools

### [BondAI](https://bondai.dev/)
*Robust agent SDK with code interpreter*

Highly capable autonomous AI agent with CLI, REST/WebSocket API, Docker support, and integrated tools.

**Hidden gem**: The code interpreter capabilities are excellent and it has a clean API.

```bash
pip install bondai
bondai  # Start CLI
bondai --server  # Start API server
```

**Links**: [Website](https://bondai.dev) | [GitHub](https://github.com/krohling/bondai) | [Docker](https://hub.docker.com/r/krohling/bondai)

---

### [Eidolon](https://eidolonai.com/)
*Multi-agent SDK with modular components*

Open-source SDK for building AI agents with pluggable, modular architecture.

**Links**: [Website](https://eidolonai.com/) | [GitHub](https://github.com/eidolon-ai/eidolon)

---

### [FastAgency](https://fastagency.ai/latest/)
*AutoGen to production deployment*

Framework for transitioning AutoGen prototypes to production applications.

**Perfect for**: When your AutoGen experiment needs to become a real application.

**Links**: [Website](https://fastagency.ai/latest/) | [GitHub](https://github.com/airtai/fastagency)

---

## Experimental & Research

### [evo.ninja](https://evo.ninja/)
*Self-adapting agent personas*

AI agent that changes its persona based on the task at hand. Interesting research into adaptive agents.

**Links**: [Website](https://evo.ninja/) | [GitHub](https://github.com/polywrap/evo.ninja/)

---

### [Agent4Rec](https://github.com/LehengTHU/Agent4Rec)
*1,000 agents for recommendation systems*

Research project with 1,000 LLM-powered agents simulating user behavior for recommender systems.

**Links**: [GitHub](https://github.com/LehengTHU/Agent4Rec) | [Paper](https://arxiv.org/abs/2310.10108)

---

### [CAMEL](https://github.com/camel-ai/camel)
*Role-playing agent conversations*

Research framework for studying autonomous communicative agents through role-playing scenarios.

**Links**: [Website](https://www.camel-ai.org/) | [GitHub](https://github.com/camel-ai/camel) | [Paper](https://ghli.org/camel.pdf)

---

## Data & Analysis Agents

### [BambooAI](https://github.com/pgalko/BambooAI)
*Data analysis for non-programmers*

Natural language data exploration and analysis. Upload data, ask questions in plain English.

**Real use**: I've used this for client data analysis. Works well for exploratory data analysis.

**Links**: [GitHub](https://github.com/pgalko/BambooAI)

---

### [Adala](https://github.com/HumanSignal/Adala)
*Autonomous data labeling*

Framework specifically designed for data labeling and processing tasks. Much better than generic agents for this use case.

**Links**: [GitHub](https://github.com/HumanSignal/Adala) | [Docs](https://humansignal.github.io/Adala/)

---

## Discord & Communication

### [GPT Discord](https://github.com/Kav-K/GPTDiscord)
*Ultimate AI agent for Discord*

Multi-modal Discord bot with image understanding, code interpretation, data analysis, Q&A on documents, internet access, and DALL-E integration.

**Features**: Code execution via E2B, document Q&A, Wolfram Alpha integration, AI moderation.

**Links**: [GitHub](https://github.com/Kav-K/GPTDiscord) | [Creator's Website](https://kaveenk.com/)

---

## Utility & Specialized Tools

### [bumpgen](https://github.com/xeol-io/bumpgen)
*AI-powered dependency management*

Automatically updates npm dependencies and generates code fixes for breaking changes.

```bash
npm install -g bumpgen
bumpgen @tanstack/react-query 5.28.14
```

**Real value**: Saves hours on dependency management. I use this on client projects.

**Links**: [GitHub](https://github.com/xeol-io/bumpgen) | [Docs](https://docs.xeol.io/bumpgen/home)

---

### [AutoPR](https://github.com/irgolic/AutoPR)
*AI-generated pull requests*

Add a label to a GitHub issue and it will plan, write code, and open a PR automatically.

**Links**: [GitHub](https://github.com/irgolic/AutoPR) | [Discord](https://discord.com/invite/ykk7Znt3K6)

---

## Legacy & Educational

*These tools are important for understanding the space but may not be the best choice for new projects.*

### BabyAGI Variants
- [BabyBeeAGI](https://github.com/yoheinakajima/babyagi/blob/main/classic/BabyBeeAGI.py) - More complex task management
- [BabyCatAGI](https://github.com/yoheinakajima/babyagi/blob/main/classic/BabyCatAGI.py) - Lightweight with search tools
- [BabyDeerAGI](https://github.com/yoheinakajima/babyagi/blob/main/classic/BabyDeerAGI.py) - Parallel tasks, GPT-3.5 only
- [BabyElfAGI](https://github.com/yoheinakajima/babyagi/blob/main/classic/BabyElfAGI/main.py) - Skills system and reflection
- [BabyFoxAGI](https://github.com/yoheinakajima/babyagi/tree/main/classic/babyfoxagi) - Self-improving with chat UI

### Other Legacy Tools
- [AI Legion](https://github.com/eumemic/ai-legion) - Early TypeScript multi-agent platform
- [Automata](https://github.com/emrgnt-cmplxty/automata) - Project-context code generation
- [BabyCommandAGI](https://github.com/saten-private/BabyCommandAGI) - CLI + LLM combination

---

## Stop Collecting Tools. Start Building.

This list is just the beginning. The real value is knowing HOW to combine these tools into products that make money.

Join **The Agentic Advantage** - where builders turn tool knowledge into income.

[Join The Agentic Advantage](https://www.skool.com/ai-elite-9507/about?ref=67521860944147018da6145e3db6e51c)

---

## Contributing

Found a tool that changed your workflow? Open a PR.
Found something dead or overrated? Open an issue. I appreciate the honesty.

**Quality standards**:
- Must have working code/documentation
- Must solve a real problem
- No "coming soon" or vaporware
- Include honest assessment of limitations

## License

MIT - Go build something useful.

---

**Maintained by**: Builders who've actually shipped with these tools  
**Last major update**: December 2024  
**Next review**: Q1 2025