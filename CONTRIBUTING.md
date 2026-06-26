# Contributing to AEGIS

We welcome contributions from researchers, engineers, and practitioners!

## Ways to Contribute

- 🐛 **Bug reports** — Open an issue with reproduction steps
- 💡 **Feature requests** — Discuss new capabilities in Issues
- 📖 **Documentation** — Improve guides, docstrings, or research notes
- 🔬 **Research** — Implement new models or extend existing ones
- 🧪 **Tests** — Expand test coverage toward our 90%+ target
- 🚀 **Performance** — Optimize inference latency or throughput

## Development Setup

```bash
git clone https://github.com/yourusername/fraud-detection-platform.git
cd fraud-detection-platform
cp backend/.env.example backend/.env
docker-compose up -d postgres redis
cd backend && pip install -r requirements.txt -r requirements-ml.txt
pip install -r requirements-dev.txt
pre-commit install
```

## Code Standards

- **Python**: Black formatting, Ruff linting, isort imports, MyPy type hints
- **TypeScript**: ESLint + Prettier, strict mode enabled
- **Tests**: pytest for Python, Jest for TypeScript — maintain 90%+ coverage
- **Commits**: Conventional Commits format (`feat:`, `fix:`, `docs:`, `test:`)
- **PRs**: Must pass all CI checks including security scan

## Submitting a PR

1. Fork the repo and create a branch: `git checkout -b feat/your-feature`
2. Write code + tests
3. Run: `pytest tests/ -v && ruff check . && black --check .`
4. Push and open a Pull Request against `develop`
5. Fill out the PR template completely
6. Wait for review (typically 2-3 business days)

## Research Contributions

For novel ML/DL contributions:
1. Open an Issue describing the approach and expected improvement
2. Include reference to supporting literature
3. Provide benchmark results vs. existing baselines
4. Add ablation study if introducing architectural changes
5. Update `research/` directory with methodology notes

## Code of Conduct

This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md). 
Be respectful, inclusive, and constructive.

## Questions?

Open a Discussion thread or email research@aegis-fraud.ai
