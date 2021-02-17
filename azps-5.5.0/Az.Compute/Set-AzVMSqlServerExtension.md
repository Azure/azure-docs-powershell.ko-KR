---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196964"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
가상 머신에서 Azure SQL Server 확장을 설정합니다.

## 구문

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Set-AzVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL 서버 확장을 설정합니다.

## 예제

### 예제 1: 가상 머신에서 자동 패치 설정 설정
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

첫 번째 명령은 **New-AzVMSqlServerAutoPatchingConfig** cmdlet을 사용하여 구성 개체를 만듭니다.
이 명령은 구성을 $AutoPatchingConfig 저장합니다.
두 번째 명령은 Get-AzVM cmdlet을 사용하여 Service02라는 서비스에서 VirtualMachine11이라는 가상 머신을 얻습니다.
이 명령은 파이프라인 연산자를 사용하여 해당 개체를 현재 cmdlet에 전달합니다.
현재 cmdlet은 가상 머신에 대한 $AutoPatchingConfig 자동 패치 설정을 설정합니다.
이 명령은 가상 머신을 Update-AzVM cmdlet에 전달합니다.

### 예제 2: 가상 머신에서 자동 백업 설정 설정
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

첫 번째 명령은 **New-AzVMSqlServerAutoBackupConfig** cmdlet을 사용하여 구성 개체를 만듭니다.
이 명령은 구성을 $AutoBackupConfig 변수에 저장합니다.
두 번째 명령은 Service02라는 서비스에서 VirtualMachine11이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.
현재 cmdlet은 가상 머신에 대한 $AutoBackupConfig 백업 설정을 지정합니다.
이 명령은 가상 머신을 Update-AzVM cmdlet에 전달합니다.

### 예제 3: 가상 SQL Server 확장을 사용하지 않도록 설정
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

이 명령은 Service03에서 VirtualMachine08이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.
이 명령은 SQL Server 가상 머신 확장을 사용하지 않도록 설정합니다.

### 예제 4: 특정 가상 SQL Server 확장 제거
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

이 명령은 Service03에서 VirtualMachine08이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.
이 명령은 가상 머신에 SQL Server 가상 머신 확장을 제거합니다.

## PARAMETERS

### -AutoBackupSettings
자동 백업 SQL Server 지정합니다.
**AutoBackupSettings** 개체를 만들 New-AzVMSqlServerAutoBackupConfig cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
자동 패치 SQL Server 지정합니다.
**AutoPatchingSettings** 개체를 만들 New-AzVMSqlServerAutoPatchingConfig cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
가상 머신의 위치를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
확장에 대한 SQL Server 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
확장의 버전을 SQL Server 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
이 cmdlet이 확장을 설정하는 가상 머신의 SQL Server 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

### Microsoft.Azure.Commands.Compute.AutoBackupSettings

### Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


