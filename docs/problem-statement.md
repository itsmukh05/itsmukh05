# Problem Statement

## Who is affected?

- Campus IT Administrators and Resource Managers: They do not have tools to test capacity management strategies or choose the best autoscaling rules.

- Students and Campus Service Users: They face delays in job processing and slow service responses during high-demand times.

## What exactly is going wrong?

- Fixed-capacity resource setups cannot adjust when large numbers of jobs arrive at once leading to queues and slow performance.

- When job volumes drop servers remain the same and waste computing power.

- Resource managers cannot determine which scaling rules perform best and trying rules on live servers could damage active university services.

## Why does it matter?

- Poor resource planning slows down student work during peak times and wastes computing capacity when demand is low.

- Without a simulation environment IT managers cannot safely test allocation policies that balance job completion times, queue lengths and server efficiency before deploying them in real systems.

## Problem statement

Campus computing systems struggle with job surges around assignment deadlines, resulting in long waiting times under fixed server limits and idle resources during quieter periods (Jeong jeong,2025). Dynamic scaling rules could help but IT managers have no safe way to compare the resource allocation strategies under realistic student workloads.Qu et al. (2018) emphasize that allocation outcomes vary based on specific workload rules and conditions. Testing these rules directly on live servers risks disrupting services and university operations. To address this, a standalone simulator is needed so IT managers can safely evaluate trade-offs in job completion time, queue length and server utilisation which would support risk-free decisions in campus capacity planning.