# Capture (AWS SAA-C03 Capstone)

Voice and text capture, processed by AI into action items, routed to downstream task systems.

## Status

Phase 1: AWS backend build during SAA-C03 cert prep (May 13 - June 24, 2026).

Phase 2 (post-cert): Chrome browser extension, published to Chrome Web Store.

## Architecture

Serverless on AWS:

- **S3**: audio/text uploads, storage classes, lifecycle policies
- **Lambda**: orchestration and processing
- **Step Functions**: workflow (transcribe -> extract -> deliver)
- **Amazon Transcribe**: speech-to-text
- **Amazon Bedrock (Claude)**: action-item extraction from transcripts
- **API Gateway**: HTTPS endpoints
- **DynamoDB**: capture history and metadata
- **Cognito**: authentication (Phase 2)
- **EventBridge**: scheduling and integrations
- **SNS / SQS**: async delivery to downstream tools
- **KMS**: encryption at rest
- **CloudWatch / CloudTrail**: monitoring and audit
- **CloudFront**: Phase 2 frontend delivery

## Build approach

Console (weeks 1-2), then AWS CDK in Python (weeks 3-6).

## Weekly progress

- [ ] Week 1: IAM, S3, account hygiene
- [ ] Week 2: Compute, networking, Lambda foundations
- [ ] Week 3: Databases, IaC pivot to CDK
- [ ] Week 4: High availability, scaling, Cognito
- [ ] Week 5: Security deep-dive, KMS, monitoring
- [ ] Week 6: Practice exams and polish

## License

MIT
