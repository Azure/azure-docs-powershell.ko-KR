---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 20e0c403656cc7fd714981f73b2a5a8c1335f9b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378309"
---
# Unregister-AzRecoveryServicesBackupContainer

## SYNOPSIS
자격 증명 모음에서 Windows Server 또는 다른 컨테이너의 등록을 등록을 등록하지 않습니다.

## 구문

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Unregister-AzRecoveryServicesBackupContainer** cmdlet은 자격 증명 모음에서 Windows Server 또는 기타 Backup 컨테이너를 등록을 등록하지 않습니다.
이 cmdlet은 자격 증명 모음에서 컨테이너에 대한 참조를 제거합니다.
컨테이너를 등록을 등록을 등록하려면 먼저 해당 컨테이너와 연결된 모든 보호된 데이터를 삭제해야 합니다.
현재 cmdlet을 사용하기 전에 Set-AzRecoveryServicesVaultContext cmdlet을 사용하여 자격 증명 모음 컨텍스트를 설정할 수 있습니다.

## 예제

### 예제 1: 자격 증명 모음에서 Windows Server 등록을 등록하지 않습니다.
```powershell
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

첫 번째 명령은 자격 증명 모음에 server01.contoso.com 이름의 Windows 컨테이너를 다운로드한 다음 $Cont 변수에 저장합니다.
두 번째 명령은 Azure Backup 자격 증명 모음에서 지정된 Windows Server를 등록을 등록하지 않습니다.

### 예제 2

자격 증명 모음에서 Windows Server 또는 다른 컨테이너의 등록을 등록을 등록하지 않습니다. (자동Generated)

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupContainer -Container $Cont -VaultId $vault.ID
```

## PARAMETERS

### -Container
등록을 등록할 Backup 컨테이너 개체를 지정합니다.
**BackupContainer** 개체를 얻습니다. Get-AzRecoveryServicesBackupContainer cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -PassThru
삭제할 컨테이너를 반환합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM 자격 증명 모음의 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesBackupContainer](./Get-AzRecoveryServicesBackupContainer.md)


