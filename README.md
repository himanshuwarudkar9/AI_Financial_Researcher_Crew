# FinancialResearcher Crew

Welcome to the FinancialResearcher Crew project, powered by [crewAI](https://crewai.com). This AI-powered system performs comprehensive financial research on companies, generating detailed research reports. The multi-agent system leverages crewAI framework to enable agents to collaborate effectively on complex financial analysis tasks, gathering market intelligence and creating insightful reports.

![Uploading freepik_candid_i_with_natural_textures_and_highly_realisti_14738 (1).jpeg…]()


## Installation

Ensure you have Python >=3.10 <3.13 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```

### Creating a New Project

If you want to create a new crewAI project from scratch, you can use the following command:

```bash
crewai create crew <project_name>
```

This command will automatically generate the complete project structure with all necessary files and folders, including agents configuration, tasks configuration, and the main crew setup.

### Customizing

**Add your API keys into the `.env` file:**
- `OPENAI_API_KEY` - Your OpenAI API key (or configure your desired LLM)
- `SERPER_API_KEY` - Your Serper API key for web search capabilities (get it from [serper.dev](https://serper.dev))

**Configuration:**
- Modify [src/financial_researcher/config/agents.yaml](src/financial_researcher/config/agents.yaml) to define your agents
- Modify [src/financial_researcher/config/tasks.yaml](src/financial_researcher/config/tasks.yaml) to define your tasks
- Modify [src/financial_researcher/crew.py](src/financial_researcher/crew.py) to add your own logic, tools and specific args
- Modify [src/financial_researcher/main.py](src/financial_researcher/main.py) to customize the company name you want to research

**To change the company being researched:**
Open [src/main.py](src/main.py) and modify the input parameters to specify your desired company name.

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```

This command initializes the financial_researcher Crew, assembling the agents and assigning them tasks as defined in your configuration.

## Output

The research report will be saved in the `output/` folder as `report.md`. This comprehensive report contains the financial analysis and research findings for the specified company.

## How It Works

This project uses **SerperDevTool** for web search capabilities to gather the latest financial information, market data, and company insights from the web. The AI agents collaborate to:
1. Research the target company
2. Analyze financial data and market trends
3. Generate a comprehensive research report
4. Save the final output to `output/report.md`

## Understanding Your Crew

The financial_researcher Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives. The `config/agents.yaml` file outlines the capabilities and configurations of each agent in your crew.

## Support

For support, questions, or feedback regarding the FinancialResearcher Crew or crewAI.
- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
