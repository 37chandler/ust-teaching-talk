## Code for Mermaid Diagram

Access the diagram directly [here](https://www.mermaidchart.com/raw/077e4cc9-f1fe-41be-94b7-0c16d9679f23?theme=light&version=v0.1&format=png).

```
---
config:
  theme: default
  look: classic
  layout: fixed
---
flowchart TB
 subgraph subGraph0["Data Collection"]
        harvest["harvest_pages"]
        get["get_links"]
        raw[("raw_listing_pages")]
  end
 subgraph subGraph1["Processing Pipeline"]
        build["build_filtered_raw_listing_pages"]
        filtered[("filtered_raw_listing_pages")]
        process["process_listing_pages"]
        processed[("processed_listing_pages")]
  end
 subgraph subGraph2["Regression Models"]
        lm["lm_fit_vw"]
        make[("make_model_year")]
        model["Model per Make/Model"]
  end
 subgraph Analysis["Analysis"]
        location["vw_location_summary"]
        deals["hot_deals_dashboard"]
        subGraph2
  end
 subgraph Monitoring["Monitoring"]
    direction LR
        monitor["text-monitoring"]
  end
    get --> harvest
    harvest --> raw
    raw --> build
    build --> filtered
    filtered --> process
    process --> processed
    processed --> location & deals & lm & make
    make --> model
    raw -.-> monitor
    filtered -.-> monitor
    processed -.-> monitor
    model -.-> monitor
    deals -.-> monitor
     harvest:::function
     get:::function
     raw:::table
     build:::function
     filtered:::table
     process:::function
     processed:::table
     lm:::function
     make:::table
     monitor:::monitoring
    classDef table fill:#f9f,stroke:#333,stroke-width:2px
    classDef function fill:#bbf,stroke:#333,stroke-width:2px
    classDef monitoring fill:#ffd,stroke:#333,stroke-width:2px
```
