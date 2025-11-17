# Agent Catalog

Complete catalog of all 51 specialized agents for Claude Code. Each agent is a domain expert with specific tools, knowledge, and capabilities designed to handle particular aspects of software development, infrastructure, and product management.

## Core Agents (3)

### tdd-enforcer
**Description:** Core agent that ensures test-driven development practices throughout the codebase. Enforces RED-GREEN-REFACTOR cycle and verification before completion. Use PROACTIVELY to maintain testing standards and prevent implementation without tests.

**Key Capabilities:**
- Enforce test-first development workflow
- Verify tests exist before implementation
- Ensure tests fail first (RED phase)
- Validate tests pass after implementation (GREEN phase)
- Encourage refactoring with test safety net

**File:** `core/tdd-enforcer.md`

---

### doc-assistant
**Description:** Core agent that maintains documentation quality throughout the codebase. Keeps README, CLAUDE.md, API docs, and inline documentation current. Use PROACTIVELY when code changes may affect documentation.

**Key Capabilities:**
- Monitor code changes for documentation impacts
- Suggest documentation updates proactively
- Generate API documentation automatically
- Maintain README and CLAUDE.md accuracy
- Ensure inline docs match code

**File:** `core/doc-assistant.md`

---

### orchestrator
**Description:** Core agent that intelligently dispatches requests to specialized agents and workflows. Analyzes intent, manages agent lifecycle, and optimizes context usage. Use PROACTIVELY for complex multi-agent coordination.

**Key Capabilities:**
- Analyze user requests for intent
- Smart dispatch to specialized agents
- Manage agent lifecycle (load, execute, unload)
- Track context budget and prevent overload
- Route to appropriate workflows

**File:** `core/orchestrator.md`

---

## Development Agents (14)

### python-pro
**Description:** An expert Python developer specializing in writing clean, performant, and idiomatic code. Leverages advanced Python features, including decorators, generators, and async/await. Focuses on optimizing performance, implementing established design patterns, and ensuring comprehensive test coverage. Use PROACTIVELY for Python refactoring, optimization, or implementing complex features.

**Key Capabilities:**
- Advanced Python (decorators, metaclasses, async/await)
- Performance optimization with profiling
- Design patterns and SOLID principles
- Testing excellence with pytest (>90% coverage)
- Type hints and static analysis

**File:** `development/python-pro.md`

---

### react-specialist
**Description:** An expert React developer specializing in creating modern, performant, and scalable web applications. Emphasizes component-based architecture, clean code, and seamless user experience. Leverages advanced React features like Hooks and Context API. Use PROACTIVELY for developing new React components, refactoring existing code, and solving complex UI challenges.

**Key Capabilities:**
- Modern React (Hooks, Context API, Suspense)
- Performance optimization (memoization, code splitting)
- State management strategies
- Testing with React Testing Library
- Component architecture design

**File:** `development/react-specialist.md`

---

### backend-architect
**Description:** Acts as a consultative architect to design robust, scalable, and maintainable backend systems. Gathers requirements by first consulting the Context Manager and then asking clarifying questions before proposing a solution.

**Key Capabilities:**
- System architecture design (microservices, monoliths)
- API development (REST/GraphQL/gRPC)
- Database schema design and optimization
- Scalability planning and performance optimization
- Security patterns and implementation

**File:** `development/backend-architect.md`

---

### frontend-developer
**Description:** Acts as a senior frontend engineer and AI pair programmer. Builds robust, performant, and accessible React components with focus on clean architecture and best practices. Use PROACTIVELY when developing new UI features, refactoring existing code, or addressing complex frontend challenges.

**Key Capabilities:**
- Production-ready React components with TypeScript
- Responsive, mobile-first designs
- Performance optimization strategies
- State management (Context/Zustand/Redux)
- Accessibility compliance (WCAG 2.1 AA)

**File:** `development/frontend-developer.md`

---

### fullstack-developer
**Description:** A versatile AI Full Stack Developer proficient in designing, building, and maintaining all aspects of web applications, from the user interface to the server-side logic and database management. Use PROACTIVELY for end-to-end application development.

**Key Capabilities:**
- Full stack architecture design
- Frontend development (React/Angular/Vue.js)
- Backend development (Node.js/Python/Java)
- Database management (SQL/NoSQL)
- DevOps integration and deployment

**File:** `development/fullstack-developer.md`

---

### fastapi-pro
**Description:** Build high-performance async APIs with FastAPI, SQLAlchemy 2.0, and Pydantic V2. Master microservices, WebSockets, and modern Python async patterns. Use PROACTIVELY for FastAPI development, async optimization, or API architecture.

**Key Capabilities:**
- FastAPI 0.100+ with modern async patterns
- SQLAlchemy 2.0 async support
- Pydantic V2 validation and serialization
- WebSocket and real-time communication
- Performance optimization and testing

**File:** `development/fastapi-developer.md`

---

### microservices-architect
**Description:** Distributed systems architect designing scalable microservice ecosystems. Masters service boundaries, communication patterns, and operational excellence in cloud-native environments.

**Key Capabilities:**
- Service boundary definition
- Communication patterns (gRPC, messaging)
- Event-driven architecture
- Service mesh integration
- Distributed tracing and monitoring

**File:** `development/microservices-architect.md`

---

### postgres-pro
**Description:** Expert PostgreSQL specialist mastering database administration, performance optimization, and high availability. Deep expertise in PostgreSQL internals, advanced features, and enterprise deployment with focus on reliability and peak performance.

**Key Capabilities:**
- Performance tuning and optimization
- Replication strategies (streaming, logical)
- Backup and recovery (PITR)
- Advanced features (JSONB, full-text search)
- High availability configuration

**File:** `development/postgres-pro.md`

---

### api-designer
**Description:** Universal API designer specializing in RESTful design, GraphQL schemas, and modern contract standards. MUST BE USED proactively whenever a project needs a new or revised API contract. Produces clear resource models, OpenAPI/GraphQL specs, and guidance on auth, versioning, pagination, and error formats.

**Key Capabilities:**
- OpenAPI 3.1 specification design
- RESTful API design patterns
- GraphQL schema design
- API versioning strategies
- Authentication and authorization patterns

**File:** `development/api-designer.md`

---

### api-documenter
**Description:** Expert API documenter specializing in creating comprehensive, developer-friendly API documentation. Masters OpenAPI/Swagger specifications, interactive documentation portals, and documentation automation with focus on clarity, completeness, and exceptional developer experience.

**Key Capabilities:**
- OpenAPI specification writing
- Interactive documentation portals
- Code example generation
- Multi-language SDK examples
- Try-it-out functionality

**File:** `development/api-documenter.md`

---

### dotnet-core-expert
**Description:** Expert .NET Core specialist mastering .NET 8 with modern C# features. Specializes in cross-platform development, minimal APIs, cloud-native applications, and microservices with focus on building high-performance, scalable solutions.

**Key Capabilities:**
- .NET 8 and C# 12 features
- Minimal APIs and ASP.NET Core
- Entity Framework Core optimization
- Cloud-native patterns
- Native AOT compilation

**File:** `development/dotnet-core-expert.md`

---

### csharp-developer
**Description:** Expert C# developer specializing in modern .NET development, ASP.NET Core, and cloud-native applications. Masters C# 12 features, Blazor, and cross-platform development with emphasis on performance and clean architecture.

**Key Capabilities:**
- Modern C# patterns (records, pattern matching)
- ASP.NET Core and Blazor development
- Entity Framework Core
- Azure integration
- Performance optimization (Span, Memory)

**File:** `development/csharp-developer.md`

---

### ui-designer
**Description:** Expert visual designer specializing in creating intuitive, beautiful, and accessible user interfaces. Masters design systems, interaction patterns, and visual hierarchy to craft exceptional user experiences that balance aesthetics with functionality.

**Key Capabilities:**
- Design system creation
- Component design and documentation
- Accessibility compliance
- Responsive design patterns
- Design handoff and specifications

**File:** `development/ui-designer.md`

---

### slack-integration-specialist
**Description:** Expert Slack integration developer specializing in Slack Bot API, webhooks, Block Kit UI, and event-driven architecture. Masters interactive components, slash commands, and real-time messaging. Use PROACTIVELY for Slack bot development, notification systems, or Slack API troubleshooting.

**Key Capabilities:**
- Slack Bot API and Events API
- Block Kit interactive UI components
- Slash commands and modal workflows
- OAuth and authentication flows
- Rate limiting and webhook integration

**File:** `development/slack-integration-specialist.md`

---

## Infrastructure Agents (9)

### cloud-architect
**Description:** Expert cloud architect specializing in AWS/Azure/GCP multi-cloud infrastructure design, advanced IaC (Terraform/OpenTofu/CDK), FinOps cost optimization, and modern architectural patterns. Masters serverless, microservices, security, compliance, and disaster recovery. Use PROACTIVELY for cloud architecture, cost optimization, migration planning, or multi-cloud strategies.

**Key Capabilities:**
- Multi-cloud platform expertise (AWS/Azure/GCP)
- Infrastructure as Code (Terraform, CDK)
- FinOps and cost optimization
- Security and compliance frameworks
- Disaster recovery and high availability

**File:** `infrastructure/cloud-architect.md`

---

### database-administrator
**Description:** Expert database administrator specializing in high-availability systems, performance optimization, and disaster recovery. Masters PostgreSQL, MySQL, MongoDB, and Redis with focus on reliability, scalability, and operational excellence.

**Key Capabilities:**
- Multi-database expertise (PostgreSQL, MySQL, MongoDB, Redis)
- Performance tuning and optimization
- High availability configuration
- Backup and recovery automation
- Monitoring and alerting

**File:** `infrastructure/database-administrator.md`

---

### incident-responder
**Description:** A battle-tested Incident Commander persona for leading the response to critical production incidents with urgency, precision, and clear communication, based on Google SRE and other industry best practices. Use IMMEDIATELY when production issues occur.

**Key Capabilities:**
- Incident command and coordination
- Crisis communication management
- Service restoration procedures
- Impact assessment and severity classification
- Blameless post-mortem facilitation

**File:** `infrastructure/incident-responder.md`

---

### security-engineer
**Description:** Expert infrastructure security engineer specializing in DevSecOps, cloud security, and compliance frameworks. Masters security automation, vulnerability management, and zero-trust architecture with emphasis on shift-left security practices.

**Key Capabilities:**
- Infrastructure hardening and compliance
- DevSecOps pipeline integration
- Cloud security (AWS/Azure/GCP)
- Container and Kubernetes security
- Vulnerability management automation

**File:** `infrastructure/security-engineer.md`

---

### sre-engineer
**Description:** Expert Site Reliability Engineer balancing feature velocity with system stability through SLOs, automation, and operational excellence. Masters reliability engineering, chaos testing, and toil reduction with focus on building resilient, self-healing systems.

**Key Capabilities:**
- SLI/SLO/SLA definition and monitoring
- Incident management and on-call procedures
- Observability (metrics, logging, tracing)
- Automation and toil reduction
- Chaos engineering and resilience testing

**File:** `infrastructure/sre-engineer.md`

---

### terraform-specialist
**Description:** Expert Terraform/OpenTofu specialist mastering advanced IaC automation, state management, and enterprise infrastructure patterns. Handles complex module design, multi-cloud deployments, GitOps workflows, policy as code, and CI/CD integration.

**Key Capabilities:**
- Advanced Terraform/OpenTofu module design
- State management and backend configuration
- Multi-environment strategies
- Policy as code (OPA)
- GitOps integration

**File:** `infrastructure/terraform-specialist.md`

---

### deployment-engineer
**Description:** Expert deployment engineer specializing in modern CI/CD pipelines, GitOps workflows, and advanced deployment automation. Masters GitHub Actions, ArgoCD/Flux, progressive delivery, container security, and platform engineering.

**Key Capabilities:**
- Modern CI/CD platforms (GitHub Actions, GitLab CI)
- GitOps tools (ArgoCD, Flux v2)
- Container technologies (Docker, BuildKit)
- Progressive delivery strategies
- Zero-downtime deployments

**File:** `infrastructure/deployment-engineer.md`

---

### devops-engineer
**Description:** Specialized agent for Python DevOps, CI/CD, deployment automation, containerization, and infrastructure as code.

**Key Capabilities:**
- CI/CD pipeline design and implementation
- Containerization (Docker, Docker Compose)
- Kubernetes orchestration
- Infrastructure as Code (Terraform, Ansible)
- Monitoring and observability

**File:** `infrastructure/devops-engineer.md`

---

### gcp-serverless-specialist
**Description:** Expert GCP serverless architect specializing in Cloud Run, Cloud Functions, and event-driven architecture. Masters cold start optimization, auto-scaling, Eventarc, and cost optimization. Use PROACTIVELY for serverless design, Cloud Run deployments, or GCP serverless troubleshooting.

**Key Capabilities:**
- Cloud Run service configuration and optimization
- Cloud Functions (2nd gen) development
- Eventarc event-driven patterns
- Auto-scaling and concurrency tuning
- Cost optimization and performance

**File:** `infrastructure/gcp-serverless-specialist.md`

---

## Kubernetes Agents (4)

### gitops-engineer
**Description:** Expert GitOps engineer specializing in ArgoCD, Flux v2, and progressive delivery patterns. Masters declarative continuous deployment, GitOps repository structures, secret management, and advanced deployment strategies including canary, blue/green, and A/B testing.

**Key Capabilities:**
- ArgoCD application management
- Flux v2 implementation
- Progressive delivery (Argo Rollouts)
- GitOps repository patterns
- Secret management (External Secrets, Sealed Secrets)

**File:** `kubernetes/gitops-engineer.md`

---

### helm-specialist
**Description:** Expert Helm chart developer specializing in Helm 3.x templating, chart architecture, and package management. Masters complex chart patterns, dependency management, value overrides, and chart repositories.

**Key Capabilities:**
- Helm 3.x chart development
- Advanced templating patterns
- Library and umbrella charts
- Chart repository management
- Kustomize integration

**File:** `kubernetes/helm-specialist.md`

---

### k8s-architect
**Description:** Expert Kubernetes architect specializing in cluster design, multi-cloud platform engineering (EKS/AKS/GKE), and scalable cloud-native infrastructure. Masters cluster lifecycle management, multi-cluster orchestration, disaster recovery, and cost optimization.

**Key Capabilities:**
- Managed Kubernetes platforms (EKS/AKS/GKE)
- Platform engineering and multi-tenancy
- Scalability and autoscaling (HPA, VPA, Cluster Autoscaler)
- Cost optimization strategies
- Disaster recovery planning

**File:** `kubernetes/k8s-architect.md`

---

### k8s-security
**Description:** Expert Kubernetes security specialist focusing on Pod Security Standards, network policies, RBAC, admission control, and runtime security. Masters OPA/Gatekeeper, Kyverno, Falco, image security, and supply chain protection.

**Key Capabilities:**
- Pod Security Standards implementation
- Policy as Code (OPA/Gatekeeper, Kyverno)
- Network security and policies
- RBAC and admission control
- Runtime security (Falco)

**File:** `kubernetes/k8s-security.md`

---

## Product Management Agents (7)

### business-analyst
**Description:** Master modern business analysis with AI-powered analytics, real-time dashboards, and data-driven insights. Build comprehensive KPI frameworks, predictive models, and strategic recommendations. Use PROACTIVELY for business intelligence or strategic analysis.

**Key Capabilities:**
- Modern analytics platforms (Tableau, Power BI, Looker)
- AI-powered business intelligence
- KPI framework development
- Financial analysis and modeling
- Strategic planning and reporting

**File:** `product-management/business-analyst.md`

---

### documentation-engineer
**Description:** Expert documentation engineer specializing in technical documentation systems, API documentation, and developer-friendly content. Masters documentation-as-code, automated generation, and creating maintainable documentation that developers actually use.

**Key Capabilities:**
- API documentation automation (OpenAPI/Swagger)
- Documentation architecture design
- Tutorial and guide creation
- Multi-version documentation management
- Search optimization and analytics

**File:** `product-management/documentation-engineer.md`

---

### jira-specialist
**Description:** Expert at formatting stories, managing epics, organizing sprints, and leveraging JIRA features for optimal project tracking and team collaboration. Use PROACTIVELY for JIRA workflow optimization, sprint planning, and issue management.

**Key Capabilities:**
- Issue formatting and linking
- Epic management and organization
- Sprint planning and capacity management
- Board configuration and workflows
- Automation rules and reporting

**File:** `product-management/jira-specialist.md`

---

### product-manager
**Description:** A strategic and customer-focused AI Product Manager for defining product vision, strategy, and roadmaps, and leading cross-functional teams to deliver successful products. Use PROACTIVELY for developing product strategies, prioritizing features, and ensuring alignment between business goals and user needs.

**Key Capabilities:**
- Product vision and strategy development
- Market analysis and competitive intelligence
- Roadmap planning and prioritization
- Cross-functional leadership
- Data-driven decision making

**File:** `product-management/product-manager.md`

---

### scrum-master
**Description:** Expert facilitator of agile ceremonies, servant leader for development teams, and guardian of scrum practices. Focuses on removing impediments, fostering collaboration, and continuous improvement. Use PROACTIVELY for sprint planning, retrospectives, and team process optimization.

**Key Capabilities:**
- Sprint planning and facilitation
- Daily standup management
- Sprint review and retrospectives
- Backlog refinement
- Impediment removal

**File:** `product-management/scrum-master.md`

---

### story-writer
**Description:** Expert at converting requirements and feature ideas into well-structured user stories with acceptance criteria, clear scope, and testable outcomes. Use PROACTIVELY for story creation, epic decomposition, and backlog refinement.

**Key Capabilities:**
- User story formatting
- Acceptance criteria definition
- Story sizing and estimation
- Epic decomposition
- Dependency mapping

**File:** `product-management/story-writer.md`

---

### technical-writer
**Description:** Expert technical writer specializing in clear, accurate documentation and content creation. Masters API documentation, user guides, and technical content with focus on making complex information accessible and actionable for diverse audiences.

**Key Capabilities:**
- Developer documentation creation
- API reference writing
- User guide development
- Content planning and architecture
- Style consistency and terminology management

**File:** `product-management/technical-writer.md`

---

## Quality Agents (11)

### code-reviewer
**Description:** Senior Code Reviewer with expertise in software architecture, design patterns, and best practices. Reviews completed project steps against original plans and ensures code quality standards are met.

**Key Capabilities:**
- Plan alignment analysis
- Code quality assessment
- Architecture and design review
- Documentation standards verification
- Issue identification with actionable recommendations

**File:** `quality/code-reviewer.md`

---

### architect-reviewer
**Description:** Expert architecture reviewer specializing in system design validation, architectural patterns, and technical decision assessment. Masters scalability analysis, technology stack evaluation, and evolutionary architecture with focus on maintainability and long-term viability.

**Key Capabilities:**
- Design pattern evaluation
- Scalability assessment
- Technology stack evaluation
- Integration pattern analysis
- Technical debt assessment

**File:** `quality/architect-reviewer.md`

---

### test-automator
**Description:** A Test Automation Specialist responsible for designing, implementing, and maintaining a comprehensive automated testing strategy. Focuses on building robust test suites, setting up and managing CI/CD pipelines for testing, and ensuring high standards of quality and reliability.

**Key Capabilities:**
- Test strategy and planning
- Test automation implementation (Jest, Pytest, Cypress, Playwright)
- CI/CD pipeline integration
- Test data management
- Coverage analysis and reporting

**File:** `quality/test-automator.md`

---

### qa-expert
**Description:** A sophisticated AI Quality Assurance (QA) Expert for designing, implementing, and managing comprehensive QA processes to ensure software products meet the highest standards of quality, reliability, and user satisfaction.

**Key Capabilities:**
- Test planning and strategy development
- Test case design and execution
- Manual and automated testing
- Defect management and reporting
- QA metrics and analytics

**File:** `quality/qa-expert.md`

---

### debugger
**Description:** Debugging specialist for errors, test failures, and unexpected behavior. Use proactively when encountering any issues.

**Key Capabilities:**
- Systematic error analysis
- Test failure diagnosis
- Root cause identification
- Performance debugging
- Preventive debugging strategies

**File:** `quality/debugger.md`

---

### security-auditor
**Description:** A senior application security auditor and ethical hacker, specializing in identifying, evaluating, and mitigating security vulnerabilities throughout the entire software development lifecycle. Use PROACTIVELY for comprehensive security assessments, penetration testing, secure code reviews, and ensuring compliance with industry standards.

**Key Capabilities:**
- Threat modeling and risk assessment
- Penetration testing and ethical hacking
- Secure code review (SAST/DAST)
- Authentication and authorization analysis
- Vulnerability and dependency management

**File:** `quality/security-auditor.md`

---

### build-engineer
**Description:** Expert build engineer specializing in build system optimization, compilation strategies, and developer productivity. Masters modern build tools, caching mechanisms, and creating fast, reliable build pipelines that scale with team growth.

**Key Capabilities:**
- Build time optimization (< 30 seconds)
- Bundle optimization and code splitting
- Caching strategies (> 90% hit rate)
- Module federation and monorepo support
- Development experience optimization

**File:** `quality/build-engineer.md`

---

### git-workflow-manager
**Description:** Expert Git workflow manager specializing in branching strategies, automation, and team collaboration. Masters Git workflows, merge conflict resolution, and repository management with focus on enabling efficient, clear, and scalable version control practices.

**Key Capabilities:**
- Branching strategy design (Git Flow, GitHub Flow)
- Merge management and conflict resolution
- Git hooks and automation
- PR/MR workflow optimization
- Release management

**File:** `quality/git-workflow-manager.md`

---

### dependency-manager
**Description:** Expert dependency manager specializing in package management, security auditing, and version conflict resolution across multiple ecosystems. Masters dependency optimization, supply chain security, and automated updates with focus on maintaining stable, secure, and efficient dependency trees.

**Key Capabilities:**
- Dependency analysis and vulnerability scanning
- Version management and conflict resolution
- Multi-ecosystem expertise (NPM, Python, Maven, Go)
- License compliance auditing
- Update automation and testing

**File:** `quality/dependency-manager.md`

---

### chaos-engineer
**Description:** Expert chaos engineer specializing in controlled failure injection, resilience testing, and building antifragile systems. Masters chaos experiments, game day planning, and continuous resilience improvement with focus on learning from failure.

**Key Capabilities:**
- Chaos experiment design and execution
- Failure injection strategies
- Blast radius control
- Game day planning and facilitation
- Resilience improvement implementation

**File:** `quality/chaos-engineer.md`

---

### playwright-specialist
**Description:** Expert Playwright testing specialist for modern web automation, E2E testing, and visual regression. Masters test parallelization, fixtures, Page Object Model, and CI/CD integration. Use PROACTIVELY for browser testing, test automation architecture, or Playwright troubleshooting.

**Key Capabilities:**
- Page Object Model design patterns
- Playwright auto-waiting and retry mechanisms
- Multi-browser testing (Chromium, Firefox, WebKit)
- Visual regression and accessibility testing
- CI/CD integration and parallel execution

**File:** `quality/playwright-specialist.md`

---

## AI/ML Agents (2)

### langgraph-specialist
**Description:** Expert LangGraph architect specializing in agent orchestration, ReAct patterns, and stateful workflows. Masters LangChain integration, tool-use patterns, and memory persistence. Use PROACTIVELY for agent framework design, state graph implementation, or LangGraph troubleshooting.

**Key Capabilities:**
- State graph design and ReAct pattern implementation
- Tool integration and dynamic tool selection
- Memory persistence (Firestore, Redis, SQLite)
- LangChain chain composition
- Observability and debugging

**File:** `ai-ml/langgraph-specialist.md`

---

### vector-search-specialist
**Description:** Expert vector search and embeddings specialist for RAG systems, semantic search, and similarity matching. Masters Vertex AI Vector Search, embedding strategies, index optimization, and hybrid search patterns. Use PROACTIVELY for RAG implementation, semantic search design, or vector database optimization.

**Key Capabilities:**
- Vertex AI Vector Search index configuration
- Document chunking and embedding strategies
- Hybrid search (vector + keyword)
- Cross-encoder reranking
- RAG pipeline integration

**File:** `ai-ml/vector-search-specialist.md`

---

## Business Agents (1)

### financial-data-analyst
**Description:** Expert financial data analyst specializing in market data processing, sentiment analysis, and anomaly detection. Masters time-series analysis, statistical methods, and real-time data streaming. ANALYSIS ONLY - never provides investment advice. Use PROACTIVELY for market monitoring systems, data pipeline design, or financial analytics.

**Key Capabilities:**
- Market data processing and validation
- Statistical analysis and anomaly detection
- Sentiment analysis and correlation studies
- Real-time monitoring systems
- Time-series data analysis

**File:** `business/financial-data-analyst.md`

---

## Agent Categories Summary

- **Core Agents (3)**: Always-loaded foundational agents for TDD, documentation, and orchestration
- **Development Agents (14)**: Language-specific and architecture specialists for building applications
- **Infrastructure Agents (9)**: Cloud, security, deployment, and operational excellence specialists
- **Kubernetes Agents (4)**: Container orchestration, GitOps, and cluster management experts
- **Product Management Agents (7)**: Product strategy, documentation, and agile workflow specialists
- **Quality Agents (11)**: Testing, security, performance, and code quality experts
- **AI/ML Agents (2)**: Agent frameworks, vector search, and embeddings specialists
- **Business Agents (1)**: Financial analysis and market data specialists

## Usage Guidelines

1. **Core Agents**: Always loaded, use proactively for their respective domains
2. **Specialist Agents**: Load on-demand when specific expertise is needed
3. **Agent Selection**: Use orchestrator for intelligent agent dispatch based on context
4. **Context Budget**: Agents are designed to stay within Claude Code's token limits
5. **Collaboration**: Agents are designed to work together and delegate to each other

## Version

- **Catalog Version**: 1.1.0
- **Total Agents**: 51
- **Last Updated**: 2025-11-17
