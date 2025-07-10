# Corporate Financial Data RAG Pipeline Assignment

Build a production-scale Financial Intelligence RAG System handling concurrent queries on corporate financial reports and earnings data with Redis caching and OpenAI API integration.

## RAG Implementation

- **Data**: Corporate annual reports, quarterly earnings, financial statements
- **Pipeline**: Document ingestion → Vector DB → Retrieval → OpenAI generation
- **Queries**: Financial metrics, company comparisons, trend analysis

## Production Infrastructure

### Concurrency Handling

- Handle 100+ concurrent requests with <2s response time
- Rate limiting per API key
- Async support and connection pooling

### Redis Caching

- Query result caching (TTL: 1h real-time, 24h historical)
- Cache popular financial metrics and company data
- Target >70% cache hit ratio

### Scaling

- Background job queue for document processing
- Async API with proper connection pooling

## Technical Stack

- **Cache**: Redis cluster
- **API**: FastAPI (async) or Node.js
- **DB**: PostgreSQL + Pinecone/Weaviate
- **Queue**: Celery/RQ
- **Monitoring**: Real-time system metrics

## Deliverables

- Scalable RAG System with concurrent request handling
- Redis Integration: Smart caching with financial data versioning
- Load Testing: Concurrent request validation + performance metrics
- Monitoring: Real-time dashboards for system metrics

## Load Testing Scenarios

- **Burst Testing**: 200 concurrent users × 10 min
- **Performance Validation**: Response time and cache hit ratio measurement

## Goal

Build a high-performance financial RAG system optimized for concurrent access with intelligent caching.
