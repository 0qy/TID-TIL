# CORS - Command Query Resonsibility Segregation
as seen [here](https://www.martinfowler.com/bliki/CQRS.html)
Using a different model to update information than the model you use to read information. Adding valuable seperation, but almost risky complexity.

### The mainstream approach for interacting with an information system
The mainstream approach is to treat it as a CRUD datastore, there is mental model of some record structure to create new records, read records, update existing records and detle records. Interaction defined by STORING and RETRIEVING these records. 

[graph - cqrs1](../assets/images/cqrs1.png)

### CQRS
comparable to collapsing multiple records into one, or forming virtual records by combining information for different places. 

Users may interact with various presentations of information. 

[graph - cqrs2](../assets/images/cqrs2.png)

Separate models for update and display. Because for many problems, particularly in more complicated domains, having the same conceptual model for commands and queries leads to a more complex model that does neither well. 

### CQRS fits with some architectual pattersn
- Fits well with event-based programming models. Common to see CQRS system split into separate services communicating with [Event Collaboration](https://www.martinfowler.com/eaaDev/EventCollaboration.html). Allowing thse services to easily take advantages of [Event Sourcing](https://www.martinfowler.com/eaaDev/EventSourcing.html) 
- Separate modesl rasises questions about how hard to keep those models consistent, which raises the likelihood of using [eventual consistency](https://www.allthingsdistributed.com/2008/12/eventually_consistent.html)
- [EagerReadDerivation](https://www.martinfowler.com/bliki/EagerReadDerivation.html)
- If the write model generates events for all updates, you can structure read models as [EventPosters](https://www.martinfowler.com/bliki/EventPoster.html), allowing them to be [MemoryImages](https://www.martinfowler.com/bliki/MemoryImage.html) and thus avoiding a lot of database interactions. 
- CQRS is suited to complex domains, the kind that also benefit from [DomainDriven Design](https://www.amazon.com/gp/product/0321125215/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=0321125215&linkCode=as2&tag=martinfowlerc-20).

### When to use it? 
