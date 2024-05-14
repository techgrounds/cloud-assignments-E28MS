
## Subject

Cosmos DB is a globally distributed, multi-model database service provided by Microsoft Azure. It's designed to handle large-scale, real-time workloads with low latency and high availability. It offers support for multiple data models including document, key-value, graph, and column-family, providing flexibility for various types of applications.

## Assignment

Gain some practical experience with CosmosDB.  

In order to do this, I will follow the Azure Cosmos DB Quickstart Guide in order to:

*  Create an Azure Cosmos DB API for NoSQL account.
*  In that account, create a document database and container.
*  Add data to the container. 

##  Key Terms

API for NoSQL: 

Azure Cosmos DB supports multiple APIs for interacting with NoSQL data, including SQL (DocumentDB), MongoDB, Cassandra, Gremlin (Graph), and Table APIs.

Document Database: 

A type of NoSQL database in which data is stored in flexible, JSON-like documents.

Container: 

In the context of Azure Cosmos DB, a container is a logical entity for storing and querying JSON documents. It's similar to a table in a relational database.

Data: 

Refers to the information that you'll be adding to the container within your Azure Cosmos DB account.

JSON:

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. 

It is based on a subset of the JavaScript Programming Language.

JSON is a text format that is completely language-independent but uses conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. 

These properties make JSON an ideal data-interchange language.

JSON is built on two structures:

1. A collection of key/value pairs: This is realized as an object, record, dictionary, hash table, keyed list, or associative array.
2. An ordered list of values: This is realized as an array, vector, list, or sequence.

JSON supports primitive types such as strings, numbers, booleans, and null, as well as composite types such as arrays (ordered lists of values) and objects (unordered collections of key/value pairs). 

It is commonly used for transmitting data between a server and a web application as an alternative to XML (eXtensible Markup Language). 

JSON is often used as the data format for APIs and configuration files.

A URI (Uniform Resource Identifier) is a string of characters that identifies a particular resource. It provides a way to uniquely identify resources on the internet or any other network. A URI can be used to specify the location of a resource, such as a web page, a file, or a piece of data, and it also defines the means of accessing that resource.

URIs can be categorized into two main types:

1. **URL (Uniform Resource Locator):** A URL is a type of URI that specifies the location of a resource and the mechanism for accessing it. It typically consists of a protocol (such as HTTP or FTP), followed by a domain name or IP address, and optionally a path to the resource within the server.

   Example: https://www.example.com/index.html

2. **URN (Uniform Resource Name):** A URN is a type of URI that provides a unique identifier for a resource but does not specify its location or access method. URNs are used to globally identify resources regardless of their location.

   Example: urn:isbn:0451450523

In summary, a URI is a universal way to identify and locate resources on the internet or any network, and it encompasses both URLs and URNs.




##  Resources


[Cosmos DB Quickstart](https://learn.microsoft.com/en-us/azure/cosmos-db/nosql/quickstart-portal)

[Micrsoft Video: What is Cosmos DB?](https://youtu.be/Jvgh64rvdXU)


##  Difficulties

##  Results

Basics Tab for creating my Azure Cosmos DB Account for NoSQL:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/73fcbd87-7f0d-4364-bf09-93abe296931f)

Backup Policy Tab:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2c612ffd-d86c-4a08-9c4c-9943677844c6

Validation passed:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/30b4de2d-e6e9-47e2-9777-26644ba32cd6)

Deployment completed:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/1951a1e1-8a04-4f85-877c-816954ec89ff)


Next, I added a New Container through the Data Explorer :

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/36f7a419-0273-4e6e-b9cd-62abb6964f3d)


Here, I expanded the ToDoList, then expanded Items, and added a structure to the pane on the right using the code below:

```
{
    "id": "1",
    "category": "personal",
    "name": "groceries",
    "description": "Pick up apples and strawberries.",
    "isComplete": false
}
```


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/6b553049-b056-4992-8139-0c13b92c941f)


Next, I tried to another JSON file provided by ChatGPT by slecting New Item and then adding the code to the pane on the right, but this resulted in an error message:

![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/f9df57a0-00ea-4c11-9f67-713b84055a1b)


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/a52c5848-e2c0-458d-a4e5-727651e9c9ba)


I then tried another JSON file supplied by ChatGPT and got the same error, meaning that my document could not be created:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/2b93a27b-b101-4599-9dab-4b3186d31471)


In order to minimize time spent troubleshooting this issue, I conceived of a workaround by changing the information in the JSON file provided in the Quickstart guide:


![image](https://github.com/techgrounds/cloud-assignments-E28MS/assets/151161141/3cd949f2-62f1-4a92-808d-f04509e1197b)


I then moved on to the next step, querying the data:
















