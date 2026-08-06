# AI Security Engineer Roadmap (2026)

A practical, free roadmap for learning how to secure machine-learning systems, LLM applications, RAG pipelines, and AI agents. It moves from security foundations to threat modeling, testing, controls, and production operations.

> **Safety note:** Use labs only on systems you own or have explicit permission to test. The goal is defensive engineering, not unauthorized access.

## What an AI Security Engineer does

An AI Security Engineer helps teams build and operate AI systems safely. The work combines:

- Application and cloud security
- Machine-learning fundamentals
- Threat modeling and secure design
- LLM evaluation and red teaming
- Identity, authorization, data protection, and monitoring
- Incident response for AI-specific failures

## How to use this roadmap

Study one phase at a time, build the suggested project, and publish evidence of your work. A realistic pace is **6–12 months** at 8–10 hours per week. Do not skip the hands-on milestones; security skill is demonstrated by the controls and tests you can build, not only by certificates.

---

## Phase 0 — Prerequisites (2–4 weeks)

### Learn

- Python: functions, classes, files, virtual environments, testing
- Linux: shell, processes, permissions, networking tools, logs
- HTTP and APIs: methods, headers, cookies, JSON, authentication
- Git: branches, pull requests, and reviewing diffs
- Core security: CIA triad, least privilege, defense in depth, threat modeling

### Free resources

- [Python for Everybody](https://www.py4e.com/)
- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/)
- [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)
- [Linux Journey](https://linuxjourney.com/)
- [MDN HTTP overview](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [OWASP Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
- [Git documentation](https://git-scm.com/doc)

### Milestone
Build a small Python API that authenticates users, validates input, logs security events, and has tests for authorization failures.

---

## Phase 1 — ML and LLM foundations (4–6 weeks)

### Learn

- Datasets, training, validation, overfitting, and model evaluation
- Tokens, embeddings, context windows, and transformers
- Inference parameters and why model output is probabilistic
- Classification metrics: precision, recall, F1, ROC-AUC
- Fine-tuning, adapters, quantization, and model cards
- The difference between a model, an AI application, an agent, and a tool

### Free resources

- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course)
- [fast.ai Practical Deep Learning](https://course.fast.ai/)
- [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/en/chapter1/1)
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course/chapter1/1)
- [PyTorch Tutorials](https://pytorch.org/tutorials/)
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)
- [Made With ML](https://madewithml.com/)
- [Hugging Face Model Cards](https://huggingface.co/docs/hub/model-cards)

### Milestone
Create a small text-classification model and document its intended use, limitations, data provenance, evaluation results, and known failure modes.

---

## Phase 2 — AI threat landscape and risk management (3–4 weeks)

### Learn

Study the threats, then map each threat to a preventative control, a detection, and a response playbook.

- Prompt injection and indirect prompt injection
- Sensitive information disclosure
- Improper output handling and insecure tool use
- Excessive agency and confused-deputy behavior
- Data and model poisoning
- Supply-chain and third-party model risk
- Model theft, denial of service, and unbounded consumption
- Insecure plugins, connectors, and agent protocols
- Privacy, copyright, bias, and safety risks

### Free resources

- [OWASP GenAI Security Project](https://genai.owasp.org/)
- [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST Generative AI Profile](https://www.nist.gov/itl/ai-risk-management-framework/generative-artificial-intelligence-profile)
- [Google Secure AI Framework (SAIF)](https://saif.google/)
- [Microsoft AI Security Best Practices](https://learn.microsoft.com/en-us/security/engineering/threat-modeling-aiml)
- [CISA Guidelines for Secure AI](https://www.cisa.gov/topics/cyber-threats-and-advisories/artificial-intelligence)
- [Cloud Security Alliance AI Safety Initiative](https://cloudsecurityalliance.org/artifacts/securing-generative-ai)

### Milestone
Create a threat model for a RAG chatbot. Include assets, trust boundaries, abuse cases, attack paths, mitigations, logging, and residual risk.

---

## Phase 3 — Secure LLM application engineering (6–8 weeks)

### Learn

- Strong separation of system instructions, user input, retrieved content, and tool results
- Input validation, output encoding, schema validation, and content moderation
- Secrets management and prevention of secrets in prompts, logs, and repositories
- Retrieval permission filtering, tenant isolation, and document provenance
- Least-privilege tool permissions and human approval for high-impact actions
- Rate limits, budgets, timeouts, retries, circuit breakers, and abuse controls
- Secure dependency and model loading practices
- Privacy-preserving retention and deletion workflows

### Free documentation and tools

- [OWASP LLM application cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Application_Cybersecurity_Cheat_Sheet.html)
- [OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/)
- [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
- [OWASP Software Component Verification Standard](https://owasp.org/www-project-software-component-verification-standard/)
- [Microsoft PyRIT](https://github.com/Azure/PyRIT)
- [NVIDIA NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
- [Guardrails AI documentation](https://www.guardrailsai.com/docs)
- [Presidio for data protection](https://microsoft.github.io/presidio/)
- [Semgrep rules and documentation](https://semgrep.dev/docs/)
- [OpenSSF Scorecard](https://github.com/ossf/scorecard)
- [SLSA supply-chain framework](https://slsa.dev/)

### Milestone
Build a local RAG demo with:

- Per-user document authorization
- PII redaction before model calls
- Structured output validation
- Tool allowlists and approval gates
- Request and security-event logging
- Tests for prompt injection and cross-user data access

---

## Phase 4 — AI red teaming and evaluation (4–6 weeks)

### Learn

- Test planning: define a system, threat model, test cases, and pass/fail criteria
- Automated and manual adversarial testing
- Direct and indirect prompt-injection tests
- Jailbreak and refusal-quality evaluation
- Data leakage, hallucination, toxicity, and unsafe tool-call tests
- Regression suites for prompts, models, policies, and retrieval changes
- Risk-based prioritization: likelihood × impact × exploitability
- Responsible disclosure and safe reporting

### Free resources and tools

- [garak LLM vulnerability scanner](https://github.com/NVIDIA/garak)
- [Microsoft PyRIT](https://github.com/Azure/PyRIT)
- [Google Model Armor concepts](https://cloud.google.com/security/products/security-command-center/model-armor)
- [Inspect AI](https://inspect.aisi.org.uk/)
- [promptfoo](https://www.promptfoo.dev/)
- [DeepEval](https://github.com/confident-ai/deepeval)
- [Giskard LLM testing](https://docs.giskard.ai/)
- [MITRE ATLAS techniques](https://atlas.mitre.org/matrices/)
- [OWASP AI Testing Guide](https://owasp.org/www-project-ai-testing-guide/)

### Milestone
Create an evaluation harness that runs at least 30 safe test cases against your application, records model/version/prompt metadata, and blocks a release when a critical security test fails.

---

## Phase 5 — Cloud, platform, and MLOps security (6–8 weeks)

### Learn

- IAM, workload identity, network segmentation, and private service access
- Container and Kubernetes security
- CI/CD security and software supply-chain controls
- Data lineage, dataset access, and artifact integrity
- Model registry permissions and deployment approvals
- Observability, anomaly detection, cost abuse, and incident response
- Backup, rollback, key rotation, and secure model retirement

### Free resources

- [Kubernetes Security documentation](https://kubernetes.io/docs/concepts/security/)
- [Kubernetes Threat Matrix](https://kubernetes.io/docs/concepts/security/)
- [Docker security documentation](https://docs.docker.com/engine/security/)
- [OWASP Kubernetes Top Ten](https://owasp.org/www-project-kubernetes-top-ten/)
- [CNCF Cloud Native Security Whitepaper](https://github.com/cncf/tag-security/tree/main/security-whitepaper)
- [MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp)
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)
- [MLflow documentation](https://mlflow.org/docs/latest/)
- [DVC documentation](https://dvc.org/doc)
- [GitHub Actions security hardening](https://docs.github.com/en/actions/security-guides/security-hardening-for-github-actions)
- [Trivy vulnerability scanner](https://github.com/aquasecurity/trivy)

### Milestone
Deploy your demo in a container with a CI pipeline that runs dependency scanning, secret scanning, unit tests, adversarial evaluation, and an image scan before deployment.

---

## Phase 6 — Production operations and governance (ongoing)

### Build operational habits

- Maintain an AI system inventory and an owner for every system
- Keep a model card, data sheet, threat model, and change history
- Define severity levels and response times for AI incidents
- Monitor access, tool calls, retrieval failures, refusals, PII events, and cost anomalies
- Review prompts, policies, tools, and dependencies like production code
- Run tabletop exercises for data leakage, unsafe actions, and compromised dependencies
- Document human escalation and kill-switch procedures

### Free references

- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [NIST Privacy Framework](https://www.nist.gov/privacy-framework)
- [ISO/IEC 42001 overview](https://www.iso.org/standard/81230.html)
- [Cloud Security Alliance AI Controls Matrix](https://cloudsecurityalliance.org/artifacts/ai-controls-matrix)
- [OWASP SAMM](https://owaspsamm.org/)
- [Incident Response Consortium resources](https://www.cisa.gov/topics/cyber-threats-and-advisories/incident-response)

### Milestone
Write an AI incident-response playbook with detection signals, containment steps, evidence collection, communication owners, recovery, and lessons learned.

---

## Portfolio projects

Build these in order of difficulty:

1. **PromptGuard:** static checks for prompt templates and agent configuration.
2. **Secure RAG demo:** tenant isolation, PII redaction, citations, and audit logs.
3. **LLM evaluation harness:** regression tests for injection, leakage, and unsafe output.
4. **Agent permission gateway:** tool allowlists, scoped credentials, approvals, rate limits, and kill switch.
5. **AI supply-chain monitor:** verify model hashes, scan dependencies, and produce an inventory.
6. **AI security observability dashboard:** track tool calls, policy violations, latency, cost, and alerts.

For every project, publish the architecture, threat model, test results, limitations, and a responsible-use note.

## Suggested weekly routine

- **2 hours:** learn one security or ML concept
- **3 hours:** implement a small control or test
- **2 hours:** attack your own lab safely and write findings
- **1 hour:** document what changed and review a current paper, advisory, or framework

## Career and interview preparation

Be ready to explain:

- Why prompt injection is not solved by a single system prompt
- How to prevent a RAG system from crossing tenant boundaries
- How an agent should handle a tool that can delete data
- What belongs in an AI threat model
- How to design an LLM security regression test
- How to balance false positives, usability, latency, and risk
- How to respond when a model leaks sensitive information

Practice with [OWASP WebGoat](https://owasp.org/www-project-webgoat/), [PortSwigger Web Security Academy](https://portswigger.net/web-security), [TryHackMe](https://tryhackme.com/), and local deliberately vulnerable applications. Stay within authorized labs.

## Communities and updates

- [OWASP GenAI Security Project](https://genai.owasp.org/)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [Hugging Face community](https://huggingface.co/)
- [MLOps Community](https://mlops.community/)
- [OpenSSF](https://openssf.org/)
- [AI Village](https://aivillage.org/)
- [NIST AI resources](https://www.nist.gov/artificial-intelligence)

## Link-checking note

AI security changes quickly. Links in this guide point to official documentation or established open-source projects where possible. Check the project license and current documentation before using a tool in production.

## License

This roadmap is released under the MIT License. See [LICENSE](LICENSE).

*Last updated: August 2026.*
