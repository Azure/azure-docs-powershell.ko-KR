---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216858"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## SYNOPSIS
이 명령은 지정 된 백업 항목의 끊어지지 않은 로그 체인 시작점과 끝점을 나열 합니다. 이 기능을 사용 하 여 사용자가 DB를 복원 하려는 시점 시간 (유효 여부)을 결정할 수 있습니다.

## 구문과

### NoFilterParameterSet (기본값)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesBackupRecoveryLogChain** cmdlet은 백업 된 Azure 백업 항목에 대 한 시간 범위 복구 지점을 가져옵니다.
항목을 백업한 후에는 **AzRecoveryServicesBackupRecoveryLogChain** 개체에 복구 시간 범위가 하나 이상 있습니다.

## 예제의

### 예제 1
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

첫 번째 명령은 7 일 전 날짜를 가져온 다음 $StartDate 변수에 저장 합니다.
두 번째 명령은 오늘 날짜를 가져온 다음 $EndDate 변수에 저장 합니다.
세 번째 명령은 AzureWorkload 부하 백업 컨테이너를 가져와 $Container 변수에 저장 합니다.
네 번째 명령은 백업 항목을 가져온 다음,이를 파이프 된 cmdlet에서 백업 항목 개체로 공유 합니다.
마지막 명령은 $BackupItem의 항목에 대 한 복구 시점 시간 범위의 배열을 가져온 다음 $RP 변수에 저장 합니다.

### 예제 2

이 명령은 지정 된 백업 항목의 끊어지지 않은 로그 체인 시작점과 끝점을 나열 합니다. 생성

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
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

### -EndDate
복구 지점을 가져오지 않아도 되는 시간 범위 종료 시간

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -항목
복구 지점을 가져오지 않아도 되는 보호 된 항목 개체

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -시작 날짜
복구 지점을 가져오지 않아도 되는 시작 시간 범위

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
복구 서비스 자격 증명 모음의 팔 ID입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Microsoft Azure.. i g i..
System. 문자열

## 출력

### RecoveryPointBase에서. i. i m/.

## 상속자

## 관련 링크
