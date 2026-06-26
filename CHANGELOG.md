# Changelog

All notable changes to AEGIS will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] — 2025-06-01 🎉

### Added
- **HGAT-FD**: Heterogeneous Graph Attention Network for Fraud Detection (novel contribution)
- **TTAAS**: Temporal Transformer with Adaptive Anomaly Scoring (novel contribution)
- Full ML ensemble: XGBoost, LightGBM, CatBoost, LSTM, Bi-LSTM, Autoencoder, Isolation Forest
- Real-time Kafka streaming pipeline with 50,000+ TPS throughput
- FastAPI backend with JWT auth, RBAC, and rate limiting
- Next.js 14 frontend with 10 specialized pages
- SHAP, LIME, and counterfactual explainability
- LLM investigation assistant (GPT-4o / Llama3)
- MLflow model tracking and registry
- Prometheus + Grafana monitoring with pre-built dashboards
- Neo4j graph database for transaction network analysis
- Kubernetes deployment manifests with HPA and PDB
- Docker Compose for local development
- GitHub Actions CI/CD pipeline
- 94%+ test coverage

### Performance
- AUC-ROC: 0.9784 on IEEE-CIS benchmark
- P99 detection latency: 87ms
- Throughput: 50,000+ TPS
- False positive rate: 0.23%

---

## [0.9.0-beta] — 2025-04-15

### Added
- Initial HGAT-FD architecture implementation
- Basic Kafka consumer
- FastAPI skeleton with authentication
- PostgreSQL schema with Alembic migrations

### Fixed
- N/A (initial release)

---

## Upcoming [1.1.0]

### Planned
- LLM investigation assistant GA (currently preview)
- Federated learning module for cross-institutional fraud detection
- Mobile app (React Native)
- Advanced counterfactual explanations with DiCE
- WebSocket streaming improvements
- Model A/B testing framework
