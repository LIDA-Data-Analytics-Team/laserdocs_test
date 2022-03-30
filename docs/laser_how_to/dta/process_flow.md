---
layout: default
title: Process Flow
parent: Data Transfer App
grand_parent: LASER How To
nav_order: 5
---

<head>
  <script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js">
  <script>mermaid.initialize({startOnLoad:true});</script>
</head>

# Process Flows for LASER Transfers
{:.no_toc}

* seed list
{:toc}


## Imports
<div class="mermaid">
flowchart TB;
	subgraph Key;
        requestor(Requestor<br>action);
	    reviewer(Reviewer<br>action);
	end;

    create_job --> |Files moved by DTA| review_store;
    import[[Import]] --> |Biscom/OneDrive/STFP etc.| import_store;
	
    subgraph DTIS [Data Transfer Import Server];
        import_store[(Data Transfer <br> Import Storage)];
        import_store --> create_job(Create New <br> Import Request <br> in DTA);
	end;

	subgraph VRE;
        review_store[(VRE Import <br> Review Storage)];
        review_store --> review(Review Files);
        review --> approve_reject(Approve / Reject <br> in DTA);
        approve_reject --> |Files moved by DTA| project_store[(VRE Project <br> Storage)];
	end;

	style requestor fill:Gold;
	style reviewer fill:lightgreen;
	style import_store fill:LightSkyBlue;
	style review_store fill:LightSkyBlue;
	style project_store fill:LightSkyBlue;
	style create_job fill:Gold;
	style review fill:lightgreen;
	style approve_reject fill:lightgreen;
</div>


## Exports
<div class="mermaid">
graph TB;
	subgraph Key;
        requestor(Requestor<br>action);
	    reviewer(Reviewer<br>action);
	end;
	
    export_store --> |Biscom/OneDrive/STFP etc.| export[[Export]];
    approve_reject --> |Files moved by DTA| export_store;

    subgraph VRE;
        project_store[(VRE Project <br> Storage)];
        project_store --> |Requestor creates files in Export Request Storage| export_request_store;
        export_request_store[(Export Request <br> Storage)] --> create_job(Create New <br> Export Request <br> in DTA);
        create_job --> |Files copied by DTA| export_review_store[(Export Review <br> Storage)];
        export_review_store --> review(Review Files);
        review --> approve_reject(Approve / Reject <br> files in DTA);
    end;

    subgraph DTES [Data Transfer Export Server];
        export_store[(Data Transfer <br> Export Storage)];
    end;
	
    style requestor fill:Gold;
	style reviewer fill:lightgreen;
    style export_store fill:LightSkyBlue;
    style export_review_store fill:LightSkyBlue;
    style export_request_store fill:LightSkyBlue;
    style project_store fill:LightSkyBlue;
    style export fill:LightSkyBlue;
    style create_job fill:gold;
    style review fill:lightgreen;
    style approve_reject fill:lightgreen;
</div>


