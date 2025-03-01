# 100 - Customer Discovery

### NotePlan - Repository Pattern

```mermaid
classDiagram
    class Client {
      +createHypothesis()
      +retrieveHypothesis()
      +updateHypothesis()
    }
    class HypothesisRepository {
      +save(hypothesis)
      +findById(id)
      +findAll()
      +update(hypothesis)
    }
    class NotePlanStorage {
      -connection
      +saveToNotes(data)
      +fetchFromNotes(query)
      +updateNote(id, data)
    }
    Client --> HypothesisRepository
    HypothesisRepository --> NotePlanStorage
```

### StoriesOnBoards - CQRS Pattern (Command Query Responsibility Segregation)

```mermaid
flowchart TB
    Client[Client Application]
    CommandBus[Command Bus]
    QueryBus[Query Bus]
    CommandHandler[Canvas Command Handler]
    QueryHandler[Canvas Query Handler]
    WriteDB[(Write Database)]
    ReadDB[(Read Database)]
    Sync[Synchronization Service]
    
    Client -->|Create/Update Canvas| CommandBus
    Client -->|Request Canvas Data| QueryBus
    CommandBus --> CommandHandler
    QueryBus --> QueryHandler
    CommandHandler --> WriteDB
    QueryHandler --> ReadDB
    WriteDB --> Sync
    Sync --> ReadDB
```

### Flowlu - Event-Driven Architecture

```mermaid
flowchart LR
    MusicApp[Music App Client]
    EventBus[Event Bus]
    CustomerSvc[Customer Service]
    FeedbackSvc[Feedback Service]
    AnalyticsSvc[Analytics Service]
    NotificationSvc[Notification Service]
    
    MusicApp -->|Publish Events| EventBus
    EventBus -->|Customer Events| CustomerSvc
    EventBus -->|Feedback Events| FeedbackSvc
    EventBus -->|User Activity Events| AnalyticsSvc
    EventBus -->|Alert Events| NotificationSvc
    
    CustomerSvc -.->|Publish Domain Events| EventBus
    FeedbackSvc -.->|Publish Domain Events| EventBus
    AnalyticsSvc -.->|Publish Insight Events| EventBus
```

### ActivePieces - Pipes and Filters Pattern

### Visual Studio Code - Plugin Architecture Pattern

### GitHub - Gitflow Workflow Pattern

### Cursor.io - AI-Enhanced Middleware Pattern

## 100 - Define Your Vision and Hypotheses

See [README.md](./100/README.md)

## 200 - Identify Customer Problems

See [README.md](./200/README.md)

## 300 - Test Problem Hypotheses

See [README.md](./300/README.md)

## 400 - Develop a Minimum Viable Product (MVP)

See [README.md](./400/README.md)

## 500 - Iterate based on Feedback

See [README.md](./500/README.md)
