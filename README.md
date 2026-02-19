# AWS Lambda – Stale EBS Snapshot Cost Optimization
## Overview

This AWS Lambda function automatically deletes stale Amazon EBS snapshots to reduce unnecessary storage costs.

Unused snapshots continue generating charges even if their associated infrastructure is no longer active. This function helps keep your AWS environment clean and cost-efficient.

## What It Does

Deletes snapshots if:

The associated volume does not exist

The volume is not attached to a running instance

The snapshot has no valid volume reference

## Benefits

Reduces AWS storage costs

Removes orphaned snapshots

Automates cleanup

Improves infrastructure hygiene

## Required IAM Permissions

ec2:DescribeSnapshots

ec2:DescribeInstances

ec2:DescribeVolumes

ec2:DeleteSnapshot
