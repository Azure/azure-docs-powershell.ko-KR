---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003179"
---
# Get-AzRecoveryServicesVaultSettingsFile

## SYNOPSIS
Azure Site Recovery 자격 증명 모음 설정 파일을 얻습니다.

## 구문

### ForSiteWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefaultWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultTypeWithCertificate
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzRecoveryServicesVaultSettingsFile** cmdlet은 Azure Site Recovery 자격 증명 모음에 대한 설정 파일을 얻습니다.

## 예제

### 예제 1: Azure Backup용 Windows Server 또는 DPM 컴퓨터 등록
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

첫 번째 명령은 TestVault라는 자격 증명 모음을 얻은 다음, 해당 자격 증명 모음을 $Vault 01 변수에 저장합니다.
두 번째 명령은 $CredsPath 변수를 C:\Downloads로 설정합니다.
마지막 명령은 Azure Backup용 자격 증명을 사용하여 $Vault 01에 $CredsPath 자격 증명 파일을 얻습니다.

### 예제 2
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

명령은 자격 증명 모음 형식 siteRecovery의 자격 증명 모음 $Vault 01의 자격 증명 모음 자격 증명 파일을 얻습니다.

### 예제 3: Azure Backup용 Windows Server 또는 DPM 컴퓨터 등록
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

명령은 자격 증명 모음 자격 증명 파일을 $Vault 01입니다.

## 매개 변수

### -Backup
자격 증명 모음 자격 증명 파일이 Azure Backup에 적용할 수 있는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -인증서
{{Fill Certificate Description}}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Azure Site Recovery 자격 증명 모음 설정 파일에 대한 경로를 지정합니다.
Azure Site Recovery 자격 증명 모음 포털에서 이 파일을 다운로드하고 로컬로 저장할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
사이트 친화적인 이름을 지정합니다.
자격 증명 모음 자격 증명을 다운로드하는 경우 이 매개 변수를 Hyper-V 사용합니다.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
사이트 식별자를 지정합니다.
자격 증명 모음 자격 증명을 다운로드하는 경우 이 매개 변수를 Hyper-V 사용합니다.

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
자격 증명 모음 자격 증명 파일이 Azure Site Recovery에 적용할 수 있는지 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vault
Azure Site Recovery 자격 증명 모음 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## 출력

### Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesVault](./Get-AzRecoveryServicesVault.md)

[New-AzRecoveryServicesVault](./New-AzRecoveryServicesVault.md)

[Remove-AzRecoveryServicesVault](./Remove-AzRecoveryServicesVault.md)


