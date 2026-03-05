# 01 — AD/DNS/Domain Lab

## Objective
Build a small, realistic Windows domain to practice and demonstrate Service Desk (N1) fundamentals.

## Lab architecture
- **Hypervisor:** VMware Workstation Pro
- **DC:** `DC01` — Windows Server 2022 (AD DS + DNS)
- **Client:** `PC-USER01` — Windows 11 (domain-joined)
- **Network:** NAT (lab-internal)
- **Admin workflow:** macOS (MacBook Air M4) → Windows host (RDP) → VMware lab

## Build steps (high level)
1. Create VM for `DC01` and install Windows Server 2022 (Desktop Experience)
2. Baseline configuration (rename, time, updates)
3. Configure static IP + DNS on `DC01`
4. Install roles: AD DS + DNS
5. Promote `DC01` to Domain Controller (new forest)
6. Create OUs, users, groups (basic structure)
7. Join `PC-USER01` to the domain
8. Validate authentication, DNS resolution, and basic GPO processing

## Validation (what I verified)
- `ipconfig /all` on DC and client
- ADUC: OUs/users/groups created
- DNS: forward lookup zone for the domain
- Client successfully joined and can log in with a domain user
- `gpresult /r` (client) shows domain policies are applied (baseline)

## Evidence
Screenshots and outputs will be added as the lab is built.

## N1 tasks covered
Password reset, account unlock, basic user/group management, domain join, DNS basics, GPO basics, documentation and escalation criteria.

## Devices (for context)
- **Admin device:** MacBook Air (M4)
- **Lab host:** Windows PC (Ryzen 7 5800X, 32GB RAM)
