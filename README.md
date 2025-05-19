# FIT3182 Collaborative Docker Setup

## Requirements
- Docker
- Your teammate must have the same Docker images:
  - `fit3182/pyspark`
  - `fit3182/mongo`

## Usage
1. Clone this repo
2. Ensure you have the local images:
   - `docker images` should list `fit3182/pyspark` and `fit3182/mongo`
3. Run:
   ```
   docker-compose up
   ```
4. Access Jupyter at: http://localhost:8888

## Folder Structure
- `notebooks/`: Jupyter notebooks go here
- `data/`: Place your CSV or JSON datasets here

MongoDB is accessible inside the notebook via:
```python
from pymongo import MongoClient
client = MongoClient("mongodb://mongodb:27017")
db = client['fit3182']
```
