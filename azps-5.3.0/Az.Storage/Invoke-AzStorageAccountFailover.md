---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376223"
---
# Invoke-AzStorageAccountFailover

## SYNOPSIS
Storage 계정의 장애 조치(failover)를 호출합니다.

## 구문

### AccountName(기본값)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Storage 계정의 장애 조치(failover)를 호출합니다. 가용성 문제가 있는 경우 저장소 계정에 대해 장애 조치 요청을 트리거할 수 있습니다. 장애 조치는 저장소 계정의 주 클러스터에서 RA-GRS 계정에 대한 보조 클러스터로 발생합니다. 장애 조치(failover) 후 보조 클러스터가 주 클러스터가 됩니다.
장애 조치(failover)를 시작하기 전에 저장소 계정에 미치는 영향은 1.1입니다. 계정에 대해 GET Blob Service 통계(, GET Table Service 통계( 및 GET Queue Service 통계)를 사용하여 마지막 동기화 https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 시간을 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 확인하세요. 장애 조치(failover)를 시작하면 손실될 수 있는 데이터입니다.
2.장애 조치(failover) 후 저장소 계정 유형은 LRS(로컬 중복 저장소)로 변환됩니다. GRS(지역 중복 저장소)를 사용하려면 계정을 변환할 수 있습니다.
3.저장소 계정에 대해 GRS를 다시 사용하도록 설정하면 Microsoft는 새 보조 지역에 데이터를 복제합니다. 복제 시간은 복제할 데이터의 양에 따라 달라집니다. 부트스트힙에 대한 대역폭 요금이 있습니다. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## 예제

### 예제 1: Storage 계정의 장애 조치(failover) 호출
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

이 명령은 Storage 계정의 마지막 동기화 시간을 확인한 다음, 해당 계정의 장애 조치(failover)를 호출하고, 장애 조치(failover) 후 보조 클러스터가 주 클러스터가 됩니다. 장애 조치(failover)에 시간이 오래 걸리기 때문에 -Asjob 매개 변수를 사용하여 백엔드에서 실행한 다음 작업이 완료될 때까지 기다릴 수 있습니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet 실행

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

### -Force
강제로 계정을 장애 조치(failover)합니다.

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

### -InputObject
Storage 계정 개체

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
저장소 계정 이름입니다.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## 참고 사항

## 관련 링크
