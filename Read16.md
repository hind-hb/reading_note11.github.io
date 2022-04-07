# Reading 16 : Serverless

## What is serverless ? 
Serverless is a cloud computing execution model that 

  - Automatically provisions the computing resources required to run application code on demand, or in response to a specific event;
  - Automatically scales those resources up or down in response to increased or decreased demand;
  - Automatically scales resources to zero when the application stops running. 

## Serverless pros and cons
 **Pros**
 
Serverless offers a number of individual technical and business benefits:

- serverless enables development teams to focus on writing code, not managing infrastructure.
- Also as noted above, serverless customers pay for execution only. The meter starts when the request is made, and ends when execution finishes
- Serverless is a polyglot environment, enabling developers to code in any language or framework - Java, Python, node.js - with which they're comfortable.

**cons**
With so much to like about serverless computing, organizations are using it for a wide variety of applications (see Figure 2 below). However, 
there are certain applications for which serverless is not favorable, or which present technical and business trade-offs to consider:
- Stable or predictable workloads: Because serverless scales up and down on demand in response to workload, it offers significant cost savings for spiky workloads
- Cold starts: Because serverless architectures forgo long-running processes in favor of scaling up and down to zero, they also sometimes need to start up from zero to serve a new request
- Vendor lock-in: Serverless architectures are designed to take advantage of an ecosystem of managed cloud services and, in terms of architectural models, go the furthest to decouple a workload from something more portable, like a virtual machine (VM) or Docker container.



