# The Freedom of IaC w/Ansible and CloudFormation

## Bio

Adam Krieger is a Developer and Architect from Winnipeg with over ten years of professional experience and a background in application service development and DevOps-powered deployment. Now a consultant with Online Business Systems, and well versed in several frameworks and languages, he is passionate about continuous improvement of technology solutions, and also the people that create them. His personal projects are automated in order to leave more time for cooking, listening to records, and reading science fiction.

## Abstract

Rubber, meet road. IaC is the process of source-controlling your runbooks. It's Dev and Ops collaborating to drive results greater than the sum. Using Ansible and AWS CloudFormation, but generic understanding, this session aims to accelerate your DevOps journey and power value into production.

## Overview

This session will discuss the value of Infrastructure as Code (IaC), including decentralization of complex knowledge, componentization of repetitious tasks, and segregation of product and context, and of course, security. Ansible and AWS CloudFormation will be used as tooling examples, and we'll look at their advantages and synergies, but goals will remain vendor-neutral. Better practices and collaborative ways forward will be a critical outcome.

## Topics

- Discuss IaC Benefits
  - Decentralize complex procedures
  - Componentize repetitious tasks
  - Segregate Product from Context
  - Abstract Non-differentiated value
- Discuss Tooling with Ansible and AWS CloudFormation as examples
  - Declarative syntax
  - Codified procedures
  - Secret Management with Vaults
  - Configuration Management with Templating
- Better Practice
  - Use the simplest tool for the job
  - Treat deployment as part of the product
  - Collaborate with all stakeholders
  - Manage all that yaml!

## Goals

- Participants know ...
  - why IaC is worth the time in any IT value stream
  - possible tools to start working with IaC
  - ways to improve an existing CI/CD pipeline
- To make value delivery a better place by allowing Dev and Ops to do what they're best at: solve problems.

[1] but that term's simplicity belies its ability to vastly improve deployment behaviour. To illustrate an example, we'll look at Ansible and AWS CloudFormation, both technically and culturally.

## Subtitle Options

- Is complexity endangered
- Runbooks in Source Control
- Responsibility as Code

## Topics (Rough)

- Declarative syntax
- Codifying the deployment process
- Codifying non-deployment processes
- Sorting complexity in buckets
- Decentralizing important application decisions
  - Beattie talked about no layer caring about the layer below it
  - Code bases shouldn't care about build server, cloud, container, but should define the constraints in which they operate. Yml files give us the happy medium, where the apps get to define their constraints, even if those constraints are defined in a specific tooling language.
  - Q+A in 1_1, show yml files to all involved parties to set hard and soft limits, sensible defaults
    - What's the sensible default of how many xlarge instances to run on your AWS account? -> 0, obv, no cost for no value
- Deploy-time environment definition, vaulted keys
- Ansible is YNAB
  - Tangerine is CloudFormation
- Entrypoint v Specsheet
  - Theorhetical v Pragmatic
  - Consuming value from others v producing value on your own

### Distribution/Sharing of Responsibility

- From general to specific, app -> build -> image -> instance
  - The more to the left, the more you have power to influence more easily (leverage), make physics metaphor
    - Are there more examples than vaulting that segregate?
  - Vaulting and segregation of environment and application
    - Helps with image/build -> instance, or else they are the same spec
- Environment = Product + Context
  - Product = Running(Apps + Servers + ...)
  - Context = Configuration + Secrets

## Ansible

- ssh + python + yml
- Runbooks as code:
  - Deployment
  - Tasks
- Vault & Secrets
- Templates with jinja

## AWS CloudFormation

- Deploy into stacks
- Describe resources in most natural state: closest to the vendor

I have been speaking about delivery and DevOps for the past few years, and have had the chance to work on several different manifestations of IaC. Building robust delivery platforms is a passion of mine, and I hope that I can improve the skills of all attendees or at least get them excited to implement these techniques in their own product workflows.


## AnsibleFest: Mastering Environments in Ansible and CloudFormation

### Description

Maybe you already use Ansible to provision services on AWS resources, but why not also provision the resources as well? Get out of the console and back into your .yml files. Extend the capabilities of Stacks with the dynamic nature of Ansible Templates. Secure your deployments with per-environment vaulting. Give developers truly production-like cloud environments to prove their work. It's time to make two great tools work well together.

### The attendee will learn...

This session will focus on cleanly laying the foundation for multi-environment AWS deployments contained by CloudFormation Stacks. The attendee will learn where and how to manipulate CloudFormation Templates with Ansible, proper vaulting of secrets within Ansible Vault, and composition of roles leading to solutions that are simple to maintain and extend.

### Comments

## CF recommendations

- CloudFront deployment changes take :48-02 (14 minutes)
- Security Group and WAF changes take (~3 minutes)

## Slides

Feedback Notes

- Speed of actual deployment (N-environment)
- Secrets demonstrated
- How to automate the hard stuff


Visual comparison of ansible and cf crossfading

Tool expl:
- hello world equiv of toolset
- Visual of ansible concepts
- Visual of difference between ansible and cloud formation 
    - Ex: ansible ssh’s

Automation of repeatable task
Visual of simple tasks being wrapped into complex, and being titled as business concerns (deploy commerce site)
Error handling during deployment

Tyler
- Expand acronym on first slide
- (Expand AWS, or put logos)
- Logos for diff modules within ansible
- Ansible history in a nutshell
- Ansible pricing, builder, background, enterprise level?
- Graphic showing vendor options
- Product selection, why we chose ansible
- Center on jinja (v j2, jinja) (need to talk about file interpretation)
- Ditch CF component explanation in exchange for
