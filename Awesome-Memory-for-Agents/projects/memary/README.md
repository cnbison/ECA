# Memary

**收录日期:** 未知

**GitHub:** [https://github.com/kingjulio8238/Memary](https://github.com/kingjulio8238/Memary)
**Website:** [https://kingjulio8238.github.io/memarydocs/](https://kingjulio8238.github.io/memarydocs/)

## 简述

（README 表格中未提供简述，请参考下方 README 摘录）

## GitHub README 摘要

> Agents promote human-type reasoning and are a great advancement towards building AGI and understanding ourselves as humans. Memory is a key component of how humans approach tasks and should be weighted the same when building AI agents. **memary emulates human memory to advance these agents.**

## README 摘录（GitHub）

```markdown
<p align="center">
  <img alt="memary_logo" src="diagrams/memary-logo-latest.png">
</p>

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=linkedin&labelColor=blue)](https://www.linkedin.com/company/memary/)
[![Follow](https://img.shields.io/badge/Follow_on_X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/memary_labs)
[![Documentation](https://img.shields.io/badge/Documentation-memary-428BCA?style=flat&logo=open-book)](https://kingjulio8238.github.io/memarydocs/)
[![Demo](https://img.shields.io/badge/Watch-Demo-red?logo=youtube)](https://youtu.be/GnUU3_xK6bg)
[![PyPI](https://img.shields.io/pypi/v/memary.svg?style=flat&color=orange)](https://pypi.org/project/memary/)
[![Downloads](https://img.shields.io/pypi/dm/memary.svg?style=flat&label=Downloads)](https://pypi.org/project/memary/)
[![Last Commit](https://img.shields.io/github/last-commit/kingjulio8238/memary.svg?style=flat&color=blue)](https://github.com/kingjulio8238/memary)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


## Manage Your Agent Memories

Agents promote human-type reasoning and are a great advancement towards building AGI and understanding ourselves as humans. Memory is a key component of how humans approach tasks and should be weighted the same when building AI agents. **memary emulates human memory to advance these agents.**

## Quickstart 🏁

### Install memary 
1. With pip:
   
Make sure you are running python version <= 3.11.9, then run 
```
pip install memary
```

2. Locally:
   
i. Create a virtual environment with the python version set as specified above 

ii. Install python dependencies: 
```
pip install -r requirements.txt
```
### Specify Models Used 
At the time of writing, memary assumes installation of local models and we currently support all models available through **Ollama**:

- LLM running locally using Ollama (`Llama 3 8B/40B` as suggested defaults) **OR** `gpt-3.5-turbo`
- Vision model running locally using Ollama (`LLaVA` as suggested default) **OR** `gpt-4-vision-preview`

memary will default to the locally run models unless explicitly specified. Additionally, memary allows developers to **easily switch between downloaded models**. 

### Run memary
**Steps**
1. [Optional] If running models locally using Ollama, follow this the instructions in this [repo](https://github.com/ollama/ollama).

2. Ensure that a `.env` exists with any necessary credentials.

   <details>
     <summary>.env</summary>
  
   ```
   OPENAI_API_KEY="YOUR_API_KEY"
   PERPLEXITY_API_KEY="YOUR_API_KEY"
   GOOGLEMAPS_API_KEY="YOUR_API_KEY"
   ALPHA_VANTAGE_API_KEY="YOUR_API_KEY"
   
   Database usage (see API info):
   FALKORDB_URL="falkor://[[username]:[password]]@[falkor_host_url]:port"
   or
   NEO4J_PW="YOUR_NEO4J_PW"
   NEO4J_URL="YOUR_NEO4J_URL"
   ```
  
   </details>
   

3. Fetch API credentials:
   <details>
     <summary>API Info</summary>

    - [**OpenAI key**](https://openai.com/index/openai-api)
    - [**FalkorDB**](https://app.falkordb.cloud/)
      - Login &rarr; Click 'Subscribe` &rarr; Create a free instance on the Dashboard &rarr; use the credentials (username, passward, falkor_host_url and port).  
    - [**Neo4j**](https://neo4j.com/cloud/platform/aura-graph-database/?ref=nav-get-started-cta)
      - Click 'Start for free` &rarr; Create a free instance &rarr; Open auto-downloaded txt file and use the credentials
    - [**Perplexity key**](https://www.perplexity.ai/settings/api)
    - [**Google Maps**](https://console.cloud.google.com/apis/credentials)
      - Keys are generated in the 'Credentials' page of the 'APIs & Services' tab of Google Cloud Console
    - [Alpha Vantage](https://www.alphavantage.co/support/#api-key)
      - Recommended to use https://10minutemail.com/ to generate a temporary email to use
    
    </details>

4.  Update user persona which can be found in `streamlit_app/data/user_persona.txt` using the user persona template which can be found in `streamlit_app/data/user_persona_template.txt`. Instructions have been provided - replace the curly brackets with relevant information. 

5. [Optional] Update system persona, if needed, which can be found in `streamlit_app/data/system_persona.txt`.

6. [Optional] Multi Graphs - Users who are using FalkorDB can generate multiple graphs and switch between their IDs, which correspond to different agents. This enables seamless transitions and management of different agents' memory and knowledge contexts.

7. Run:

```
cd streamlit_app
streamlit run app.py
```

## Basic Usage
```python
from memary.agent.chat_agent import ChatAgent

system_persona_txt = "data/system_persona.txt"
user_persona_txt = "data/user_persona.txt"
past_chat_json = "data/past_chat.json"
memory_stream_json = "data/memory_stream.json"
entity_knowledge_store_json = "data/entity_knowledge_store.json"
chat_agent = ChatAgent(
    "Personal Agent",
    memory_stream_json,
    entity_knowledge_store_json,
    system_persona_txt,
    user_persona_txt,
    past_chat_json,
)
```
Pass in subset of `['search', 'vision', 'locate', 'stocks']` as `include_from_defaults` for different set of default tools upon initialization.

### Multi-Graph
When using FalkorDB database, you can create multi-agents. Here is an example of how to set up personal agents for different users:

```python
# User A personal agent
chat_agent_user_a = ChatAgent(
    "Personal Agent",
    memory_stream_json_user_a,
    entity_knowledge_store_json_user_a,
    system_persona_txt_user_a,
    user_persona_txt_user_a,
    past_chat_json_user_a,
    user_id='user_a_id'
)

# User B personal agent
chat_agent_user_b = ChatAgent(
    "Personal Agent",
    memory_stream_json_user_b,
    entity_knowledge_store_json_user_b,
    system_persona_txt_user_b,
    user_persona_txt_user_b,
    past_chat_json_user_b,
    user_id='user_b_id'
)
```

### Adding Custom Tools
```python
def multiply(a: int, b: int) -> int:
    """Multiply two integers an

... (更多内容请访问上面 GitHub 链接)
```

