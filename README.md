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

### Bindings

#### Queues

#### Http Services

#### WS Http Bindings

#### Net Named Pipes

#### NetBinding and WebSockets

### Validation

#### Schema Validation

#### Data Validation

### Transactions

### REST Style Services

### Metadata

#### Service Descriptors

#### Service Contract

### Client Generation

### Caching

### Transient Fault Handling

### Reliable Sessions

### Custom Behaviors

### Data Streaming
