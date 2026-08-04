# AI Security Engineer Roadmap 2026

A free, practical path from cybersecurity and machine-learning foundations to securing LLMs, RAG systems, AI agents, and production AI platforms.

> Defensive and educational only. Practice in isolated labs and test only systems you own or have permission to assess.

## Who this is for

- Security engineers moving into AI security
- ML/AI engineers who want to ship safer systems
- Developers building LLM, RAG, or agent applications
- Students looking for a portfolio-focused learning plan

## What you will build

By the end, you should be able to threat-model an AI system, test an LLM application in a safe lab, harden its data and tool permissions, add monitoring, and explain the risks to engineering and leadership.

## 12-month learning path

| Phase | Months | Focus | Portfolio milestone |
|---|---:|---|---|
| 1 | 1–2 | Python, Linux, networking, Git | Secure API utility with tests |
| 2 | 3–4 | Security foundations and threat modeling | Threat model for an AI service |
| 3 | 5–6 | ML and LLM fundamentals | Small local RAG application |
| 4 | 7–8 | LLM application security | Prompt-injection evaluation lab |
| 5 | 9–10 | Agent, cloud, and supply-chain security | Permissioned tool-using agent |
| 6 | 11–12 | Governance, detection, and production | End-to-end AI security case study |

## Phase 1 — Engineering foundations

Learn Python, HTTP, REST APIs, JSON, SQL basics, Linux shell usage, Git, Docker, authentication, and logging.

Free resources:

- [Python for Everybody](https://www.py4e.com/)
- [Automate the Boring Stuff](https://automatetheboringstuff.com/)
- [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)
- [Linux Journey](https://linuxjourney.com/)
- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)
- [Docker Get Started](https://docs.docker.com/get-started/)
- [GitHub Skills](https://skills.github.com/)

Project: build a small FastAPI service with input validation, structured logs, rate limiting, tests, and a Dockerfile.

## Phase 2 — Security and risk foundations

Study confidentiality, integrity, availability, least privilege, identity, secrets management, secure SDLC, incident response, web security, and threat modeling.

Free resources:

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
- [OWASP Application Security Verification Standard](https://owasp.org/www-project-application-security-verification-standard/)
- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [MITRE ATT&CK](https://attack.mitre.org/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)

Project: create a data-flow diagram and STRIDE-style threat model for a chatbot that retrieves internal documents.

## Phase 3 — ML and LLM fundamentals

Understand datasets, training versus inference, embeddings, tokens, transformers, context windows, evaluation, fine-tuning, RAG, vector search, and model limitations.

Free resources:

- [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/en/chapter1/1)
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course/chapter1/1)
- [Stanford CS224N](https://web.stanford.edu/class/cs224n/)
- [Karpathy: Let's build GPT from scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY)
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- [PyTorch Tutorials](https://pytorch.org/tutorials/)
- [FAISS documentation](https://faiss.ai/)

Project: build a local-document RAG demo with citations, a small evaluation set, and a clear privacy note.

## Phase 4 — LLM application security

Focus on the security risks that appear in real AI products:

- Prompt injection and indirect prompt injection
- Sensitive information disclosure and data leakage
- Insecure output handling
- Excessive agency and unsafe tool use
- Retrieval poisoning and untrusted documents
- Model denial of service and cost abuse
- Insecure plugins, connectors, and model supply chains
- Hallucination, overreliance, and unsafe business logic

Free resources:

- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [OWASP GenAI Security Project](https://genai.owasp.org/)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [Google Secure AI Framework](https://saif.google/)
- [Microsoft AI Red Teaming](https://learn.microsoft.com/en-us/security/ai-red-team/)
- [OpenAI Safety Best Practices](https://platform.openai.com/docs/guides/safety-best-practices)
- [Anthropic Red Teaming](https://www.anthropic.com/research)

Project: create a deliberately vulnerable local chatbot and evaluate it with harmless test cases. Document the issue, impact, mitigation, and regression test for each finding.

## Phase 5 — Agents, cloud, and supply chain

Learn to secure tool-using agents and MCP-style integrations through explicit permissions, isolated execution, allowlists, human approval for risky actions, timeouts, quotas, and complete audit trails.

Free resources:

- [OWASP Agentic AI Threats and Mitigations](https://genai.owasp.org/)
- [Model Context Protocol documentation](https://modelcontextprotocol.io/)
- [OpenSSF Scorecard](https://github.com/ossf/scorecard)
- [SLSA framework](https://slsa.dev/)
- [Sigstore](https://www.sigstore.dev/)
- [Kubernetes security documentation](https://kubernetes.io/docs/concepts/security/)
- [Cloud Security Alliance](https://cloudsecurityalliance.org/artifacts)
- [GitHub Actions security hardening](https://docs.github.com/en/actions/security-for-github-actions/security-guides/security-hardening-for-github-actions)

Project: build an agent with two mock tools. Enforce per-tool authorization, argument validation, network restrictions, approval gates, rate limits, and an append-only audit log.

## Phase 6 — Production, monitoring, and governance

Study secure deployment, model and data inventories, access reviews, privacy, retention, evaluation gates, abuse monitoring, incident response, and evidence for audits.

Free resources:

- [NIST AI RMF Playbook](https://www.nist.gov/itl/ai-risk-management-framework/ai-rmf-playbook)
- [NIST Generative AI Profile](https://www.nist.gov/itl/ai-risk-management-framework/ai-rmf-generative-ai-profile)
- [CISA AI security guidance](https://www.cisa.gov/topics/ai)
- [OWASP Software Assurance Maturity Model](https://owaspsamm.org/)
- [OpenTelemetry documentation](https://opentelemetry.io/docs/)
- [Prometheus documentation](https://prometheus.io/docs/introduction/overview/)
- [MLflow documentation](https://mlflow.org/docs/latest/)
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)

Project: deploy a small AI API with authentication, secret isolation, request/response redaction, prompt and retrieval logging that avoids sensitive content, abuse alerts, and a rollback plan.

## Practical security checklist

### Before launch

- Inventory models, datasets, prompts, tools, connectors, and users
- Classify sensitive data and define retention rules
- Threat-model direct and indirect prompt injection
- Pin and scan dependencies and container images
- Set model, tool, network, token, and cost limits
- Add human approval for external side effects

### During operation

- Log identity, model version, policy decisions, tool calls, and errors
- Monitor unusual volume, extraction patterns, and repeated refusals
- Test retrieval boundaries and authorization on every request
- Rotate secrets and review permissions regularly
- Keep incident playbooks and a safe shutdown path

### Before every release

- Run regression evaluations for safety and security
- Review changed prompts, tools, policies, and dependencies
- Test tenant isolation and sensitive-data handling
- Record known limitations and residual risk

## Portfolio projects

1. AI service threat-modeling report
2. Local RAG privacy and authorization test harness
3. Prompt-injection regression suite
4. Secure tool-using agent with approval gates
5. Dependency and model provenance checker
6. AI API abuse and cost monitoring dashboard
7. Red-team/blue-team tabletop exercise for an AI assistant
8. Secure-by-default LLM application starter template

## Suggested weekly routine

- 3 hours: learn one concept from the links above
- 3 hours: implement a small lab
- 1 hour: read a standard, incident report, or research paper
- 1 hour: write findings and publish them in your portfolio

## Communities and updates

- [OWASP GenAI Slack and projects](https://genai.owasp.org/)
- [Hugging Face community](https://huggingface.co/community)
- [MLOps Community](https://mlops.community/)
- [CNCF Slack](https://community.cncf.io/)
- [NIST AI resources](https://www.nist.gov/artificial-intelligence)
- [MITRE ATLAS](https://atlas.mitre.org/)

## Ethics and scope

Only test systems you own or have explicit permission to assess. Keep experiments local or sandboxed, never submit secrets or private data to public models, and report vulnerabilities responsibly.

## License

This roadmap is released under the [MIT License](LICENSE).

*Last updated: August 2026.*
