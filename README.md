# WCF Migration & Modernization Patterns

Publishers of WCF Services have two reasonable paths to modernize and maintain their applications in the modern development context. This document serves to outline and aggregate recommendations and guides to help ease migration and modernization of these services. 

## Upgrading Services

### CoreWCF and dotnet 6

Core WCF was introduced as an upgrade path, instead of an alternative for hosting services.
The feature set for CoreWCF is currently limited, but if you're upgrading basic HTTP/S bindings, this route should be relatively simple.

#### References

* [CoreWCF GitHub](https://github.com/CoreWCF/CoreWCF)
* [dotnet client libraries](https://github.com/dotnet/wcf)
* [Upgrade DevBlog](https://devblogs.microsoft.com/dotnet/upgrading-a-wcf-service-to-dotnet-6/)

## Migrating Services

Because of limited feature parity and broader support with other hosting frameworks, developers may choose to migrate their WCF services to alternative hosting solutions. If this is the desired path, the sections outlines below outline recommended solutions.

### ASP.NET Core 6.0 gRPC

#### References

* [Why gRPC](https://learn.microsoft.com/en-us/aspnet/core/grpc/why-migrate-wcf-to-dotnet-grpc?view=aspnetcore-6.0)
* [migration checklist](https://learn.microsoft.com/en-us/dotnet/architecture/grpc-for-wcf-developers/migrate-wcf-to-grpc)
* [sample application](https://github.com/dotnet-architecture/grpc-for-wcf-developers)

### ASP.NET Web API

#### References

* [Migrating to a Web API App](https://social.technet.microsoft.com/wiki/contents/articles/33261.migrating-a-wcf-service-to-an-api-app.aspx)

## Recommendations for Feature Parity

Modern technology stacks supply many of the feature sets that WCF used to provide in software. Below are recommendations for achieving feature parity with modern solutions. Some are directly replacements for code; Others rely on the host platform, rather than dev code, to provide common application aspects.

### Authentication / Authorization

#### References

* [Client Certificates on Azure Web Apps](https://learn.microsoft.com/en-us/azure/app-service/app-service-web-configure-tls-mutual-auth?tabs=azurecli)
* [General Auth](https://learn.microsoft.com/en-us/azure/app-service/overview-authentication-authorization)

### Encryption

#### References

* [PaaS Encryption with Azure](https://learn.microsoft.com/en-us/azure/security/fundamentals/encryption-overview#tls-encryption-in-azure)

### Bindings

#### Queues

##### References

* [Azure Function Queue Trigger](https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-service-bus-trigger?tabs=in-process%2Cextensionv5&pivots=programming-language-csharp)

#### Http Services

##### References

* [Azure Function Http Trigger](https://learn.microsoft.com/en-us/azure/azure-functions/functions-bindings-http-webhook-trigger?tabs=in-process%2Cfunctionsv2&pivots=programming-language-csharp)

#### WS Http Bindings

Currently Not Available

##### References

* [Azure Web PubSub](https://learn.microsoft.com/en-us/azure/azure-web-pubsub/concept-service-internals)
* [Azure SignalR](https://learn.microsoft.com/en-us/azure/azure-signalr/signalr-overview)

#### Net Named Pipes

Currently Not Available

### Validation
Several kinds of validation are available for use from the dotnet community; Recommendations for the variety of validations available are detailed below.

#### Schema Validation

##### References

* [protobuf](https://learn.microsoft.com/en-us/aspnet/core/grpc/protobuf?view=aspnetcore-6.0)
* [Newtonsoft JSON Schema](https://www.newtonsoft.com/json/help/html/JsonSchema.htm)
* [XML Validation](https://learn.microsoft.com/en-us/dotnet/standard/data/xml/xml-schema-xsd-validation-with-xmlschemaset)

#### Data Validation

##### References

* [Data Annotations](https://learn.microsoft.com/en-us/aspnet/mvc/overview/older-versions-1/models-data/validation-with-the-data-annotation-validators-cs)
* [Fluent Validation](https://docs.fluentvalidation.net/en/latest/)

### Transactions

Currently Not Available

### Metadata

#### Service Descriptors / Contract / Client Generation

Service documentation and descriptors for service discovery can be provided with OpenAPI compliant protocol implementations such as NSwag and Swashbuckle. These two frameworks can read and generate service clients for compliant apis.

##### References

* [Swashbuckle/Swagger Docs](https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-6.0&tabs=visual-studio)
* [NSwag Docs](https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-nswag?view=aspnetcore-6.0&tabs=visual-studio)

### Caching

#### References

* [Framework Caching](https://learn.microsoft.com/en-us/dotnet/core/extensions/caching)
* [Azure Cache for Redis](https://learn.microsoft.com/en-us/azure/azure-cache-for-redis/cache-dotnet-how-to-use-azure-redis-cache)

### Transient Fault Handling

#### References

* [Polly Framework](https://dotnetfoundation.org/projects/polly)

### Custom Behaviors

TO BE DETEREMINED

### Data Streaming

TO BE DETEREMINED

## Future-proofing Considerations

* [Explore best practices in the Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)
* [Become familiar with the Azure Well-Architected Framework](https://azure.microsoft.com/en-us/solutions/cloud-enablement/well-architected/)
* [Microsoft Security Benchmark](https://learn.microsoft.com/en-us/security/benchmark/azure/)
* [OWASP Top 10](https://owasp.org/www-project-top-ten/)
* [Microservices for Containerized Apps](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/)
* [Cloud-native App Development](https://dotnet.microsoft.com/en-us/learn/microservices)

