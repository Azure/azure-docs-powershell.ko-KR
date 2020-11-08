---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 9e1ba332efbaf3c7e314f4daf7ebfb9bb96b22b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216362"
---
# Get-AzRecoveryServicesBackupStatus

## SYNOPSIS
ARM 리소스가 백업 되었는지 여부를 확인 합니다.

## 구문과

### Name (기본값)
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdWorkload
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### I
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
지정 된 리소스가 구독의 복구 서비스 자격 증명 모음에서 보호 되지 않으면 명령이 null을 반환 하거나 비어 있습니다. 보호 된 경우 관련 자격 증명 모음 세부 정보가 반환 됩니다.

## 예제의

### 예제 1

ARM 리소스가 백업 되었는지 여부를 확인 합니다. 생성

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupStatus -Name 'myAzureVM' -ResourceGroupName 'myAzureVMRG' -Type AzureVM
```

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -이름
구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableObjectName
구독에서 일부 복구 서비스 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 이름입니다.

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
구독에서 일부 RecoveryServices 자격 증명 모음으로 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
구독에서 일부 RecoveryServices 자격 증명 모음이 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 ID입니다.

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
구독에서 일부 복구 서비스 자격 증명 모음에 의해 이미 보호 되 고 있는 경우 대표 항목을 확인 해야 하는 Azure 리소스의 유형입니다.

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### Microsoft Azure.. i m.. i a m.

## 상속자

## 관련 링크
