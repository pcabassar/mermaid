```mermaid
graph TD
    subgraph "Care Adviser: Find an Attorney Process"
        A[Step 1: Receive & Review Task] --> B{Is there enough info to start?};
        B -- "No, critical info missing" --> C["Request info from CC <br>(If no reply in 24hrs, task -> Planned)"];
        B -- "Yes, with assumptions" --> D["Proceed with task <br>(Inform CC of assumptions)"];
        C --> D;
        D --> E[Step 2: Create Search Task in Care Network];
        E --> F[Step 3: Search Internal Care Network for existing options];
        F --> G[Step 4: Build Initial List via External Research];
        G --> H[Step 5: Qualify List <br>(Check licenses, ratings, etc.)];
        H --> I[Step 6: Vet Qualified List <br>(Call/email to confirm availability & fit)];
        I --> J{Did vetting yield enough viable options?};
        J -- "No, striking out" --> K["Collaborate with CC & <br> return to research"];
        K --> G;
        J -- "Yes" --> L[Step 7: Analyze & Present Findings to CC];
        L --> M([End Process]);
    end
