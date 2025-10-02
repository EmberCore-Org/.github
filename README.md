# EmberCore Organization

<div align="center">

## 🔥 Keeping medication safe, together

**A comprehensive family caregiver platform starting with EmberCare medication management**

[![.NET 8](https://img.shields.io/badge/.NET-8.0-512BD4?logo=dotnet)](https://dotnet.microsoft.com/)
[![Avalonia UI](https://img.shields.io/badge/Avalonia-11.0-9C5DC5?logo=avalonia)](https://avaloniaui.net/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active_development-orange.svg)](https://github.com/EmberCore-Org)

[About](#about) • [Projects](#projects) • [Getting Started](#getting-started) • [Community](#community) • [Roadmap](#roadmap)

</div>

---

## About

**EmberCore** helps the **Sandwich Generation**—adults caring for both children and aging parents—manage the overwhelming responsibility of family medication tracking.

### The Problem We're Solving

47 million caregivers in the United States juggle medication management for their loved ones. They face:

- **Lost medications** hiding in purses, cabinets, and travel bags
- **Expired bottles** discovered months after they should have been discarded
- **Duplicate purchases** from forgetting what's already at home
- **Family coordination chaos** when multiple people manage the same medications
- **Anxiety and overwhelm** from tracking it all mentally

### Our Solution

EmberCare provides **systematic medication inventory management** through a simple desktop application that:

- ✅ **Tracks medications through 4 lifecycle phases** (In Transit → Just Arrived → Working Inventory → In Pillbox)
- ✅ **Prevents lost doses** with clear location tracking and expiration monitoring
- ✅ **Reduces stress** through organized, visible inventory management
- ✅ **Supports family coordination** with shared medication tracking
- ✅ **Protects privacy** with local-first data storage (SQLite)

### Why EmberCore?

**"Ember"** represents the warm, steady flame of family care—not flashy, but essential and enduring.

We build **useful-first software** that genuinely helps caregivers, then focus on commercial viability. Our approach prioritizes:

- 🎯 **Safety and simplicity** over feature bloat
- 🔒 **Privacy through local-first architecture**
- 💡 **Caregiver-centered design** with large buttons and clear workflows
- 🏗️ **Clean architecture** supporting long-term maintainability

---

## Projects

EmberCore uses a **modular repository architecture** with specialized repositories for different concerns:

### 🔧 Technical Repositories

| Repository | Purpose | Status | Tech Stack |
|------------|---------|--------|------------|
| **[domain](https://github.com/EmberCore-Org/domain)** | Zero-dependency domain layer with business rules | ✅ Complete | C# / .NET 8 |
| **[infrastructure](https://github.com/EmberCore-Org/infrastructure)** | EF Core + SQLite data access layer | 🚧 In Progress | Entity Framework Core |
| **[application](https://github.com/EmberCore-Org/application)** | Application services and business workflows | ✅ Complete | C# / .NET 8 |
| **[desktop](https://github.com/EmberCore-Org/desktop)** | Avalonia UI cross-platform desktop app | 🚧 In Progress | Avalonia UI + ReactiveUI |

### 📊 Strategic Repositories

| Repository | Purpose | Status |
|------------|---------|--------|
| **[business](https://github.com/EmberCore-Org/business)** | Market research and commercialization strategy | 🚧 Ongoing |
| **[DevOps](https://github.com/EmberCore-Org/DevOps)** | CI/CD infrastructure and deployment automation | 📋 Planned |

### 🎯 Master Workspace

| Repository | Purpose |
|------------|---------|
| **[workspace](https://github.com/EmberCore-Org/workspace)** | Master coordination repository with Git submodules |

The **workspace** repository coordinates all specialized repositories through Git submodules, providing a single solution file (`EmberCore.sln`) for full-stack builds.

---

## Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) or later
- [Git](https://git-scm.com/) for version control
- [GitKraken](https://www.gitkraken.com/) (recommended for submodule management)

### Quick Start

```bash
# Clone the master workspace with all submodules
git clone --recursive https://github.com/EmberCore-Org/workspace.git
cd workspace

# Build the entire solution with local project references
dotnet build EmberCore.sln -p:UseLocalReferences=true

# Run the desktop application
dotnet run --project desktop/EmberCore.Desktop.csproj

# Run all tests
dotnet test EmberCore.sln -p:UseLocalReferences=true
```

### Individual Repository Development

```bash
# Work on specific components
cd domain && dotnet build && dotnet test
cd infrastructure && dotnet build && dotnet test
cd application && dotnet build && dotnet test
cd desktop && dotnet build && dotnet run
```

### Documentation

- **[Architecture Overview](https://github.com/EmberCore-Org/workspace/blob/main/CLAUDE.md)** - Complete architecture and development guide
- **[GitKraken Workflow](https://github.com/EmberCore-Org/workspace/blob/main/GITKRAKEN-WORKFLOW-GUIDE.md)** - Git operations and submodule management
- **[Business Strategy](https://github.com/EmberCore-Org/business/blob/main/strategy/unified-strategy.md)** - Market validation and commercialization plan
- **[MVP Roadmap](https://github.com/EmberCore-Org/workspace/blob/main/EmberCore-MVP-Roadmap.md)** - Development milestones and timelines

---

## Community

### Contributing

We welcome contributions! Here's how to get involved:

1. **Check the [project board](https://github.com/orgs/EmberCore-Org/projects)** for current priorities
2. **Review repository-specific issues** in the appropriate submodule
3. **Follow our Git Flow branching strategy**: `main` (production) ← `dev` (integration) ← `feature/bug/chore` branches
4. **Create issues in the correct repository** based on the work scope (see [Issue Management Strategy](https://github.com/EmberCore-Org/workspace#issue-management-strategy))
5. **Use GitKraken** for visual submodule management and issue → branch → PR workflow

### Code of Conduct

EmberCore is built for caregivers with empathy and respect. We expect:

- 🤝 **Respectful collaboration** with all contributors
- 💬 **Clear communication** about technical decisions and reasoning
- 📚 **Documentation-first approach** with verbose comments explaining the "why"
- 🛡️ **Safety-critical mindset** since we're building tools for medication management
- 🎓 **Teaching through code** with explanatory comments and helpful error messages

### Development Philosophy

> **"No one tool does it all. Orchestrate a stack. Own your flow."**

We build with:

- **Clean Architecture** - Clear separation between domain, application, infrastructure, and UI layers
- **Domain-Driven Design** - Business rules in the domain layer, zero framework dependencies
- **Test-Driven Development** - Comprehensive test coverage (85%+ target for domain/application layers)
- **Waterfall Methodology** - Systematic, phase-based development with clear milestones
- **Local-First Privacy** - SQLite database, no cloud requirements, family data stays private

---

## Roadmap

### Current Status (October 2025)

- ✅ **Domain Layer** - Complete with medication lifecycle management
- ✅ **Application Services** - Business workflows and validation logic
- ✅ **Infrastructure Layer** - EF Core repositories and SQLite integration
- 🚧 **Desktop UI** - Avalonia views and navigation (current focus)
- 📋 **Market Validation** - Business strategy and customer research

### Phase 1: MVP Launch (Q4 2025)

**Goal:** Working desktop application for family caregivers

- [x] Domain model with 4-phase medication lifecycle
- [x] SQLite database with Entity Framework Core
- [x] Application services for medication management
- [ ] Complete Avalonia UI with medication list views
- [ ] Medication add/edit/archive workflows
- [ ] Phase transition operations (move between lifecycle phases)
- [ ] Testing with real caregiver scenarios

### Phase 2: Market Validation (Q1 2026)

**Goal:** Validate caregiver demand and willingness to pay

- [ ] Landing page and subscription infrastructure
- [ ] Customer acquisition through caregiver communities
- [ ] Target: 25+ trial users, 10+ paying customers
- [ ] Goal: $2K MRR with clear growth trajectory
- [ ] Document customer acquisition costs and retention

### Phase 3: Growth & Scale (Q2-Q4 2026)

**Goal:** Build sustainable business or validate exit strategy

- [ ] Scale to $5K+ MRR consistently
- [ ] Expand feature set based on customer feedback
- [ ] Multi-family coordination features
- [ ] Cross-platform support (macOS, Linux, Windows)
- [ ] Decision gate: Continue growth vs. strategic sale vs. portfolio expansion

### Long-Term Vision (2027+)

**Potential expansion** based on market validation:

- Additional caregiver tools (document tracking, care coordination)
- Portfolio strategy for multiple family caregiver applications
- Platform architecture for systematic app development
- Strategic partnerships with healthcare organizations

> **Decision-driven approach:** Every milestone includes validation gates. We adapt based on real customer feedback and business results, not assumptions.

---

## Technology Stack

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Language** | C# / .NET 8 | Cross-platform, type-safe, excellent tooling |
| **UI Framework** | Avalonia UI 11.0 | Modern XAML-based cross-platform desktop UI |
| **State Management** | ReactiveUI | MVVM pattern with reactive programming |
| **Database** | SQLite + EF Core | Local-first, zero-configuration data storage |
| **Testing** | xUnit | Comprehensive test coverage with mocking support |
| **Architecture** | Clean Architecture | Domain-driven design with clear layer separation |
| **Version Control** | Git + GitKraken | Submodule coordination and visual workflow |

---

## Contact & Support

### Project Maintainer

**John Junkins** ([@macjunkins](https://github.com/macjunkins))
- Primary focus: Personal AI tooling and family caregiver applications
- Philosophy: Build useful products first, commercialize if genuinely valuable
- Approach: Systematic development with empathy for end users

### Get Involved

- 📧 **Issues:** Create issues in the [appropriate repository](https://github.com/EmberCore-Org/workspace#issue-management-strategy)
- 💬 **Discussions:** Use GitHub Discussions for ideas and questions
- 🐛 **Bug Reports:** Submit detailed bug reports with reproduction steps
- 💡 **Feature Requests:** Share user stories with caregiver context

### License

All EmberCore repositories are released under the [MIT License](LICENSE).

We believe family caregiving tools should be accessible and transparent.

---

<div align="center">

**Built with ❤️ for the Sandwich Generation**

*Helping caregivers keep medication safe, together*

[![EmberCore Organization](https://img.shields.io/badge/EmberCore-Organization-FF6B3C?style=for-the-badge)](https://github.com/EmberCore-Org)

</div>
