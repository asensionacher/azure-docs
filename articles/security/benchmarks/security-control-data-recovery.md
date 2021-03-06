---
title: Azure Security Control - Data Recovery
description: Security Control Data Recovery
author: msmbaldwin
manager: rkarlin

ms.service: security
ms.topic: conceptual
ms.date: 12/30/2019
ms.author: mbaldwin
ms.custom: security-recommendations

---

# Security Control: Data Recovery

Ensure that all system data, configurations, and secrets are automatically backed up on a regular basis.

## 9.1: Ensure regular automated back ups

| Azure ID | CIS IDs | Responsibility |
|--|--|--|
| 9.1 | 10.1 | Customer |

Enable Azure Backup and configure the backup source (Azure VMs, SQL Server, or File Shares), as well as the desired frequency and retention period.

How to enable Azure Backup:
https://docs.microsoft.com/azure/backup/

## 9.2: Perform complete system backups and backup any customer managed keys

| Azure ID | CIS IDs | Responsibility |
|--|--|--|
| 9.2 | 10.2 | Customer |

Enable Azure Backup and target VM(s), as well as the desired frequency and retention periods. Backup customer managed keys within Azure Key Vault.

How to enable Azure Backup:
https://docs.microsoft.com/azure/backup/

How to backup key vault keys in Azure:
https://docs.microsoft.com/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey?view=azurermps-6.13.0

## 9.3: Validate all backups including customer managed keys

| Azure ID | CIS IDs | Responsibility |
|--|--|--|
| 9.3 | 10.3 | Customer |

Ensure ability to periodically perform data restoration of content within Azure Backup. If necessary, test restore to an isolated VLAN. Test restoration of backed up customer managed keys.

How to recover files from Azure Virtual Machine backup:

https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm

How to restore key vault keys in Azure:

https://docs.microsoft.com/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey?view=azurermps-6.13.0

## 9.4: Ensure protection of backups and customer managed keys

| Azure ID | CIS IDs | Responsibility |
|--|--|--|
| 9.4 | 10.4 | Customer |

For on-premises backup, encryption-at-rest is provided using the passphrase you provide when backing up to Azure. For Azure VMs, data is encrypted-at-rest using Storage Service Encryption (SSE). You may enable Soft-Delete in Key Vault to protect keys against accidental or malicious deletion.

How to enable Soft-Delete in Key Vault:

https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete?tabs=azure-portal

## Next steps

See the next security control: [Incident Response](security-control-incident-response.md)
