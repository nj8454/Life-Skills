# **Technical Investigation : Evaluating Elasticsearch, Solr and Lucene for Full Text Search**

## **1. Introduction**

This report investigates **Elasticsearch**, **solr** and **lucene** as potential solution to improve performance and scalability issues in **Full Text Search** beyond Traditional Database.

## **2. Issues with using Traditional Databases**

- **Performance Issues** - Databases are optimized for structured data. Searching large text fields becomes slow as data grows.
- **Limited Search Features** - Traditional Databases don't provide fuzzy search, typo tolerance, relevance ranking, stemming, lemmatization etc.
- **Scalability Problem** - Full text indexes get very large and slow down inserts/updates. Scaling horizontally is also hard for FTS in Traditional Database.
- **Lack of Flexibility** - Hard to implement advanced features like autocomplete, faceted search or weighted scoring.

## **3. Technology Evaluation**

### **3.1 Apache Lucene**

- Apache lucene is a high-performance, full-featured search engine library written in **Java**
- It is not a complete search engine application itself but rather a robust framework that allows developer to integrate search functionality into their own software system.
- It is designed to provide apowerfull Full Text Search capabilities within the aplications.

### **3.2 solr**

- Solr is an open-source platform written in **Java** and it uses lucene java search library as its core.
- Solr offers distributed search, faceting, near real-time indexing, rich document handling and integration with big data tools.
- Built on the battle tested Apache Zookeper, solr makes it easy to scale up and down.

### **3.3 Elasticsearch**

- Elaticsearch is an open-source, distributed search analytics engine built on Apache Lucene  that store and analyze large volumes of data in real-time using a JSON based structure and RESTful APIs.
- Elasticsearch is used for real-time search, log analysis, application performance monitoring, security  intelligence and bussiness analytics.
- It has gained more popularity than Solr in recent years due to its flexibility, scalability and developer friendly features. 

## 4. **Comparision**

| **Aspect**          | **Lucene**	            | **Solr**	          | **Elasticsearch** |
|-----------------|---------------------|-----------------|---------------|
| W**hat it is** | A search library (core engine) | Search server built on Lucene | Distributed search engine built on Lucene |
| **Ease of use** | Requires programming to use | Ready-to-use, HTTP API | Easy to use, RESTful JSON API |
| **Data format** |	Index files	| XML, JSON, CSV | JSON documents |
| **Scalability** |	N/A (library only) | Supports distributed search (SolrCloud with ZooKeeper) | Automatic sharding and horizontal scaling |
| **Real-time search** | Depends on usage | Near real-time indexing | Near real-time indexing |
| **Query language** | Lucene API | Query parsers and HTTP requests | Powerful JSON-based DSL |
| **Use cases** | Embedded search in apps | Mature enterprise search | Real-time search, analytics, logging |
| **Popularity** | Basis of Solr & Elastic | Mature, widely used enterprise | Fast-growing, widely adopted |

## 5. **Recommendation**

For full-text search, here is a recommendation of Elasticsearch, Solr, and Lucene in descending order based on overall ease of use, features, scalability, and popularity:

### **Elasticsearch**

- Best for ease of use with RESTful API and JSON documents.
- Excels in real-time full-text search, analytics, and distributed scalability.
- Ideal for modern applications needing fast indexing and flexible querying.

### **Solr**

- Mature and powerful with advanced enterprise features.
- Good for complex full-text search needs and large-scale deployments.
- Slightly more complex to set up than Elasticsearch but very customizable.

### **Lucene**

- Core search library, less user-friendly on its own.
- Best if you want to build fully custom search applications from scratch.
- Requires more programming effort and integration.

## 6. Conclusion

- **Elasticsearch** is likely the best choice if your primary concerns are improving performance and scaling full-text search quickly with minimal operational overhead. It offers built-in distributed capabilities, flexible querying, and wide community support for scaling efficiently.

- **Solr** is a solid option if you require advanced enterprise features and have the expertise to manage cluster coordination manually for scalability. It provides reliable performance but may require more tuning.

- **Lucene** alone is not recommended unless you have resources to develop and maintain a custom search solution, as it lacks the out-of-the-box infrastructure for scalability.
