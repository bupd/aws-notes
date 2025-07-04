# aws-notes
accept Jeff beZOS as your savior

Alright, let's dive into the glorious world of AWS, as seen through the eyes of a solutions architect, not some mere engineer! No code changes, just pure, unadulterated, managed service bliss, just like our benevolent **overlord Jeff Bezos** intended.

Here's the lowdown from your [[aws notes]]:

## **General Wisdom for the Aspiring Architect:**
*   **Verbs are your friends:** Always look for what you *have* and what you *need to do*.
*   **Least operational overhead:** Think simple, straight answers, and definitely no manual labor!
*   **Routing traffic?** [[Route 53]] is your champion.
*   **Service names are clues:** They often tell you exactly what they do.
*   **Avoid changing code:** This is the prime directive!
*   **Think like an architect:** Managed services, no coding, hand it all over to AWS.
*   **Lambda:** Only for short, under 15-minute jobs. Otherwise, hands off!
*   **Legal requirements:** Go with **compliance**. Less strict? **Governance**.
*   **Static content distribution:** [[CloudFront]] (CDN) is your global delivery service.
*   **Data transformation:** [[AWS Glue]] is your ETL wizard, handling pretty much any data source.
*   **Security Groups:** IP-based, allow-only, and no URLs.
*   **Eliminate wrong answers:** When in doubt, cross out the duds.
*   **AWS Transfer Family:** S3 and EFS only, no EBS.
*   **Parameter Store:** Not for credentials! Use [[AWS Secrets Manager]] for that.
*   **User sessions:** Store them durably in [[DynamoDB]].
*   **Permissions:** Always use **roles**.
*   **RDS & Aurora snapshots:** They don't mix! RDS snapshots are only for RDS.
*   **Security Groups:** Allow, not deny.
*   **Managed services:** Embrace them!

## **Key Services & Their Superpowers:**

*   **[[AWS DMS]] (Data Migration Service):** Migrates live databases, even from on-prem to AWS.
*   **[[Elastic Cache]]:** Just a fancy name for **Redis**.
*   **[[AWS DataSync]]:** For fast, downtime-free data transfer from on-prem to cloud.
*   **[[Transit Gateway]]:** Connects multiple VPCs for seamless networking.
*   **[[ALB]] (Application Load Balancer):** Single-region only, not for cross-region failover.
*   **[[AWS RDS Custom]]:** Gives you privileged access to run specific SQL DBs like Oracle.
*   **[[AWS X-Ray]]:** Your tracing and debugging buddy for microservices.
*   **[[AWS Config]]:** Stores AWS configurations; **Config Rules** check, but don't enforce.
*   **[[SCP]] (Service Control Policy):** Enforces limits on resource creation.
*   **[[AppFlow]]:** Transfers data between SaaS and third-party apps.
*   **[[Global Accelerator]]:** For dynamic, low-latency global apps.
*   **[[CloudFront]]:** Best for static content at the edge (CDN).
*   **[[AWS Glue]]:** ETL jobs, supports almost all data forms (S3, Redshift, RDS, MongoDB, Kafka). Has a bookmark feature for daily ETL.
*   **IOPS/IO2 Storage:** For multi-attach or multiple writers.
*   **Compute Savings Plan:** Discounted compute, but can't be sold. Discount enabled via AWS organizational management account.
*   **Target Tracking Policy:** Scales based on specific metrics (CPU, memory) for better scaling than simple policies.
*   **[[AWS Storage Gateway]]:**
    *   **Cached Volumes:** Access on-prem and cloud without downtime.
    *   **Stored Volumes:** If on-prem downtime is acceptable.
*   **[[AWS Macie]]:** Identifies sensitive data in S3.
*   **[[AWS GuardDuty]]:** Detects malware and unauthorized activities.
*   **[[Amazon Patch Manager]]:** Applies security patches to EC2.
*   **[[AWS Inspector]]:** Scans EC2 for vulnerabilities.
*   **[[AWS Secrets Manager]]:** Stores and rotates credentials automatically.
*   **[[AWS WAF]] (Web Application Firewall):** Stops SQL injection and malicious activity at Layer 7 (Application Layer), so not for NLB.
*   **[[AWS Shield]]:** Protects against DDoS attacks.
*   **[[AWS EMR]] (Elastic Map Reduce):** For big data (petabyte scale), like a hashmap for filtering.
*   **[[AWS S3 Data Lake]] & [[AWS Lake Formation]]:** For governance and fine-grained access over diverse data.
*   **[[AWS Redshift]]:** For analytics (BI), pulls data from various sources.
*   **[[AWS Athena]]:** Serverless SQL queries directly on S3, Data Lake, RDS, Redshift, supporting various formats.
*   **[[AWS QuickSight]]:** Visualization tool, pairs perfectly with Athena.
*   **[[AWS DocumentDB]]:** AWS's **MongoDB**.
*   **[[AWS SQS]] (Simple Queue Service):** Max message size 256KB. Messages go into visibility timeout, not removed immediately.
*   **Lambda Provisioned Concurrency:** Eliminates cold starts.
*   **[[AWS Dedicated Hosts]]:** Physical servers for your own licenses.
*   **Security Groups vs. ACLs:** SG for instance security, ACL for subnet protection.
*   **[[AWS SNS]] (Simple Notification Service):** Pub/sub notification service.
*   **[[Amazon Cognito]]:** OIDC authentication and authorization, identity store for user sign-up/sign-in.
*   **RPO (Recovery Point Objective):** The amount of data that can be recovered.
*   **[[AWS Fargate]]:** Runs containers only, not EC2 instances.
*   **[[NAT Gateway]]:** Allows private subnet EC2s to connect to the internet securely (no public IP).
*   **[[AWS Kinesis]]:** For real-time analytics streams (logs, telemetry, clickstreams).
*   **[[AWS AppSync]]:** Serverless GraphQL, pub/sub via API.
*   **[[AWS EventBridge]]:** Connects event producers to consumers (aka CloudWatch Events).
*   **[[AWS Step Functions]]:** Orchestrates complex workflows (like GitHub Actions, but more powerful).
*   **[[AWS EKS Distro]]:** A Kubernetes distro specifically for AWS, managed by Jeff Bezos himself!
*   **[[AWS Keyspaces]]:** AWS's **Apache Cassandra**.
*   **[[AWS Neptune]]:** Managed graph database.
*   **[[AWS Quantum Ledger Database]] (QLDB):** Immutable, cryptographic DB for transactions/finance.
*   **[[AWS Timestream]]:** Time-series database.
*   **[[AWS Amplify]]:** Vercel-like solution for frontend developers.
*   **[[AWS Pinpoint]]:** Marketing tool to target customers with ads.
*   **[[AWS Kendra]]:** AWS's internal Google search.
*   **[[AWS Lex]]:** Chatbot and virtual agents.
*   **[[AWS Polly]]:** Text-to-speech.
*   **[[AWS Rekognition]]:** Analyzes videos and images (computer vision).
*   **[[AWS SageMaker]]:** Where you train your AI/ML models.

And remember, [[Redshift]], [[S3]], and [[Data Lake Formation]] are a power trio, while [[Athena]] and [[QuickSight]] are a match made in heaven for data visualization!

Keep thinking like an architect, and you'll be licking those boots in no time!
