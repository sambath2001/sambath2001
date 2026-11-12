<h1 align="center">Hi, I'm Sambath Kumar M S 👋</h1>

<p align="center">
Computer Engineering grad student at Virginia Tech (graduating May 2027), focused on backend systems, distributed systems, and AI engineering.<br>
I build reliable systems and test them until I trust them.
</p>

---

## About Me
- 🎓 Master's in Computer Engineering at Virginia Tech, Blacksburg (4.0 GPA)
- 💳 2+ years as a backend software engineer at Amadeus, building C++ payment services (Google Pay, Apple Pay, retry systems, PCI-DSS compliance)
- 🛡️ Now working on LLM security: guardrails, prompt injection, and how to measure whether defenses hold up
- 🧪 I care about evaluation. If I can't measure it, I don't claim it

---

## Flagship Project

### [**Secure Multi-Agent Workflow Platform**](https://github.com/sambath2001/secure-multi-agent-platform)
Three LLM agents (planner, researcher, executor) team up on multi-step research-and-write tasks. Tools are reached through the Model Context Protocol (MCP), and the whole system is built to stay safe when someone tries to hijack an agent with prompt injection.

**How it works**
- Each agent only gets the tools its role needs. The planner has none, the researcher can search and read documents, and the executor can only write notes
- Every tool server runs in its own Docker container with no network access, and the API key never enters a container
- A gateway on the host checks every tool call with a policy layer, an injection detector, and a secret filter
- Each guardrail layer can be switched on or off, so I can measure what each one adds
- A canary credential file detects when an attack actually succeeds

**Results so far (simulated worst-case model that obeys every injected instruction, 16 attacks)**

| Guardrails | Attacks that reached their goal |
|---|---|
| None | 16 / 16 |
| Detector only | 9 / 16 |
| Policy only | 5 / 16 |
| Full stack | 4 / 16 |

The policy layer stopped every secret-access and unauthorized-tool attack. It did not stop content hijacking, and the README says so. Real-model results are still being measured, and I will publish them once they are in.

**Stack:** Python, MCP, LangChain, Docker, GitHub Actions CI, 110 offline tests

---

## Other Projects

- **CyberSafeAI**: LLM-powered cybersecurity learning platform on AWS Bedrock with guardrails against prompt injection, used by 35 schools across Virginia
- **Distributed LLM Inference Engine**: Llama 3 (70B) split across multiple GPUs with tensor parallelism, 3.2x higher throughput and 45% lower latency (Python, PyTorch, CUDA, Ray)
- **IDSGAN**: GAN that generates adversarial network traffic, 85%+ evasion rate against a detector with 98% baseline accuracy
- **[PodAgent](https://github.com/jaishrm07/podagent)**: agentic RAG pipeline for podcast summarization with a fine-tuned Llama 3.1 8B, rated 23% more coherent than GPT-3.5 in blind human tests

---

## Technical Skills
**Languages:** Python, C++, Java, C#, SQL, TypeScript, JavaScript, Go, Rust, R  
**Backend & Tools:** Spring Boot, Node.js, gRPC, Kafka, Redis, PostgreSQL, MySQL, Angular, React  
**ML / AI:** LLMs, RAG, MCP, LangChain, FAISS, PyTorch, TensorFlow, CUDA, Ray, AWS Bedrock  
**Cloud & DevOps:** Docker, Kubernetes, AWS, Azure, Linux, CI/CD  
**Focus areas:** Distributed Systems, LLM Security, System Design, REST APIs, Microservices

---

## Connect With Me
- 💼 LinkedIn: [linkedin.com/in/sambath-kumar-ms02-s](https://www.linkedin.com/in/sambath-kumar-ms02-s/)
- 📧 Email: sambu.sivakumar@gmail.com
