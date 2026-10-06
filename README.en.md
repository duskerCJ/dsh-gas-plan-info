# dsh-gas-plan

[中文](README.md) | [English](README.en.md)

> **Public overview and access-request repository.** Plugin source code, the bundled Skill, and project references remain in a separate private repository and are intentionally not included here.

`dsh-gas-plan` is a DSH profile bundle for **DZProject (Unreal Engine 5.8)**. It provides a Gameplay Ability System (GAS)-aware planning convention for gameplay requirements.

It adds `/plan-gas`; it does not replace DSH's built-in `/plan` command or modify the plan-mode state machine.

## Overview

- Enter DSH built-in plan mode with `/plan-gas <gameplay requirement>`.
- Apply GAS Core conventions for GA activation/end flow, GE state and lifecycle, and GC presentation boundaries.
- Enable five knowledge presets by default: UnLua, ListenServer, Gameplay Tags & Items, ActiveGE & Duration, and GameplayCue.
- Bundle the `dz-gas-split` Skill and require a consolidated GA/GE/GC/Tag Master Plan.
- Enforce UE 5.8 constraints around GameplayEvents, prediction, replication, Lua boundaries, Duration GEs, and ReplicationID.

## Test Examples

The screenshots below show a plan-mode test run using **Mimo v2.6 Pro High**.

The requirement models a fire-stack mechanic for item `04012021`: successful fire attacks add permanent stacks up to 30; a qualifying skill hit at full stacks amplifies damage and consumes the stacks.

### Feature Summary and GA Split

The model inspects existing damage, event, and Tag flow before producing actors, trigger chain, authority, terminal condition, and the GA split:

![Mimo v2.6 Pro High - fire stack plan](docs/images/mimo-v2.6-pro-high-fire-stack-plan.jpg)

### GA/GE/GC/Tag Master Plan

The final plan consolidates GA, GE, GC, and Tag counts. It gives every proposed asset a sole responsibility, lifecycle, optional status, and explicit missing placeholders:

![Mimo v2.6 Pro High - fire stack master plan](docs/images/mimo-v2.6-pro-high-fire-stack-master-plan.jpg)

## Request Access to the Private Source Repository

The actual plugin source repository is private and available only to authorized users.

For evaluation, use, or contribution access, open an [access request issue](../../issues/new?template=access-request.md) in this repository and provide:

1. Your GitHub username;
2. Intended use and expected scenario;
3. Whether you need read/install access only or write access for contributions;
4. Team or project, if applicable.

After approval, the account is added to the organization and granted the appropriate team permission:

- **Read**: clone and install the private plugin;
- **Write**: clone, push, and collaborate.

> Never post Tokens, passwords, private keys, or other credentials in an issue.

## Scope

This public repository exists only for the overview, examples, and access requests. It does not provide cloneable plugin source code, the private Skill, or project reference material.
