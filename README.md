# AI-Powered Interview Panel Selection System

## Project Description
An intelligent system that leverages knowledge graphs and large language models to match job descriptions with candidate resumes for optimal interview panel selection. The system goes beyond traditional keyword matching by understanding semantic relationships between skills and creating dynamic knowledge graphs.

## Key Features
- **Knowledge Graph Generation**: Creates hierarchical relationships between technical skills and domains
- **Semantic Skill Mapping**: Uses LLMs to understand relationships between different technologies and concepts
- **Multi-format Resume Parsing**: Supports PDF, DOCX, and TXT formats
- **Sophisticated Matching Algorithm**: Considers both skill coverage and semantic distance in the knowledge graph
- **Scoring System**: Provides detailed match metrics including:
  - Coverage Ratio
  - Semantic Relevance Score
  - Overall Match Score

## Architecture
1. **Document Processing**
   - Resume parsing using PyMuPDF and python-docx
   - Text extraction and normalization

2. **Knowledge Graph Construction**
   - Base knowledge from domain expertise
   - Dynamic expansion using LLM-powered relationship inference
   - Neo4j graph database integration

3. **Skill Matching Engine**
   - Path-based distance calculation
   - Weighted scoring algorithm
   - Hierarchical relationship consideration

## Requirements
Create a `requirements.txt` file with:

```txt
langchain>=0.1.0
langchain-community>=0.0.10
langchain-openai>=0.0.3
langchain-experimental>=0.0.42
langchain-groq>=0.0.3
neo4j>=5.14.0
python-docx>=1.1.2
PyMuPDF>=1.24.0
pandas>=2.0.0
pathlib>=1.0.1
typing>=3.7.4
```

## Setup
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure environment variables:
   ```bash
   NEO4J_URI=<your-neo4j-uri>
   NEO4J_USERNAME=<your-username>
   NEO4J_PASSWORD=<your-password>
   GROQ_API_KEY=<your-groq-api-key>
   ```

## Output
The system provides:
- Individual resume match scores
- Detailed skill coverage analysis
- Semantic relevance metrics
- Ranked list of candidates

## Advantages Over Traditional Methods
- Goes beyond simple keyword matching
- Understands skill relationships and hierarchies
- Considers both direct and indirect skill matches
- Provides explainable matching metrics
- Adapts to new technologies and skills