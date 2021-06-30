# Options

![Compute Icon](Compute_light-bg.svg){ align=left  }
> Compute in the cloud is about understanding, What you are processing, How frequently, and What size resources you require.

---

=== "ECS"

    * Sed sagittis eleifend rutrum
    * Donec vitae suscipit est
    * Nulla tempor lobortis orci

=== "Lambda"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

=== "Serverless"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

=== "EC2"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci

## Compute Principles

1. What kind of processing are you doing? [^1]
2. High consistent CPU load? [^2]
3. Sporadic CPU load? [^3]
4. How long does your processing run for? [^4]
5. How fast do you need to scale? [^5]
6. Higher up the stack [^6]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^3]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^4]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^5]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^6]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.

## When Fargate is better

1. If you don't want to rearchitect you app, and want to lift and shift quickly.
2. You need to scale (small to medium*)
3. You can't deal with cold-starts
4. You are doing large batch processing with high compute needs (Use Fargate Spot)

### Pluses and Minuses

| Positives (+):      | Negatives (-):            |
| ------------------- | ------------------------- |
| Less Complexity     | Higher Costs (Maybe)      |
| Better Security     | Less Customization        |
| Lower Costs (Maybe) | Limited Regions Available |

!!! abstract "Fargate Cost Calculator"
    [Fargate Cost Calculator](https://www.fargate.org/) - <https://www.fargate.org/>

!!! question "Faragate Consideration"
    *Fargate has had some issues for us when tried scaling very quickly at very large scales.
    Our docker repo was on-prem, and we've switched over to using AWS's native ECR (Docker Container Registry)
    This has improved performance. We've found problems as Fargate takes a while to spin up a new task.

### Resilency

Do you need Fargate in Multi-AZ?

## When Lambda is better

1. Cost-sensitivity
2. Spoardic workloads
3. Processing batches takes less than 15 minutes

!!! warning "Lambda Constraints"
    15 min per invocation for a lambda

### Example Usage

For example you could rearchitect your react app (front-end) to work within a lambda
The lambda could then call a CMS content api (back-end)
Your remaining static assets could live on a S3 bucket.

This architect is highly scaleable, cost-effective.
The challenge: it may require significant rearchitecture from your current solution.

### Lambda Considerations

1. Can you replace EC2/ECS with lambda?
2. Portability
3. Environment control
4. Trigger type
5. Response time
6. Response size
7. Process time
8. Memory usage
9. What's the size of your lambda?
10. How fast does scaling need to happen?
11. Max run time?
12. What kind of processing are you doing?

Lambda largely operates based on **trigger events** that originate in other system

!!! warning "Lambda Constraints"
    1. **15 min** per invocation for a lambda
    2. Even using S3, you're limited to **50MB** for lambda code

!!! tip "💡 Architecture Ideas"
    1. Idea: Main Lambda could trigger queue then process w/ further child lambdas"

## When EC2 is better

## What are your compute options?

### Options Table

| Element                        | Description                                                                                      | Tags            |
| ------------------------------ | ------------------------------------------------------------------------------------------------ | --------------- |
| Lambda                         |                                                                                                  | Serverless      |
| S3 (Serverless WebApp)         | Serverless Web App on S3 Buckets                                                                 | Serverless      |
| Docker Containers              |                                                                                                  | Containers      |
| ECR (Container Registry)       | Elastic Container Registry for managing and sharing container images                             | Containers      |
| Fargate (ECS)                  |                                                                                                  | Containers      |
| Kubernetes/Kinesis (EKS / K8S) |                                                                                                  | Containers      |
| Auto Scaling                   | automatically change the number of VM instances. You set defined metric   and thresholds         | Virtual Servers |
| Batch                          | Run large-scale parallel and high-performance computing applications   efficiently in the cloud. | Virtual Servers |
| EC2 (Mac)                      | Mac Instances                                                                                    | Virtual Servers |
| EC2                            | Servers (Linux / Windows)      Instance types provide combinations of CPU/RAM                    | Virtual Servers |
| Parallel Cluster               |                                                                                                  | Virtual Servers |
| VMware Cloud on AWS            |                                                                                                  | Virtual Servers |
| AMI                            | Machine Image                                                                                    | Virtual Servers |
| App Mesh                       |                                                                                                  |                 |

## How to implement

## References
