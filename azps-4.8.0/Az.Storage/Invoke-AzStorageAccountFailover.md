---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212078"
---
# Invoke-AzStorageAccountFailover

## SYNOPSIS
저장소 계정의 장애 조치 (failover)를 호출 합니다.

## 구문과

### AccountName (기본값)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
저장소 계정의 장애 조치 (failover)를 호출 합니다. 가용성 문제가 발생 하는 경우 저장소 계정에 대 한 장애 조치 요청이 트리거될 수 있습니다. 저장소 계정의 기본 클러스터에서 RA-GRS 계정에 대 한 보조 클러스터로 장애 조치 (failover)가 발생 합니다. 보조 클러스터는 장애 조치 후에 기본으로 됩니다.
장애 조치 (failover)를 시작 하기 전에 저장소 계정에 대 한 다음 영향을 이해 하십시오. 1.1. Blob 가져오기 서비스 통계를 사용 하 여 마지막 동기화 시간을 확인 하세요 ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) 계정에 대 한 테이블 서비스 통계 가져오기 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 및 큐 서비스 통계 가져오기) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) . 장애 조치를 시작 하는 경우 손실 될 수 있는 데이터입니다.
2. 장애 조치 (failover) 후 저장소 계정 유형이 로컬 중복 저장소 (LRS)로 변환 됩니다. GRS (지역 중복 저장소)를 사용 하도록 계정을 변환할 수 있습니다.
3. 저장소 계정에 대 한 GRS을 다시 사용 하도록 설정 하면 Microsoft에서 새 보조 지역으로 데이터를 복제 합니다. 복제 시간은 복제할 데이터 양에 따라 달라 집니다. 부트스트랩에 대 한 대역폭 요금은에는 없다는 점에 유의 하세요. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## 예제의

### 예제 1: 저장소 계정의 장애 조치 (failover) 호출
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

이 명령은 저장소 계정의 마지막 동기화 시간을 확인 한 후 장애 조치를 실행 하 여 장애 조치 후 보조 클러스터가 기본으로 됩니다. 장애 조치 (failover)는 시간이 오래 걸리기 때문에-Asjob 매개 변수를 사용 하 여 백엔드에서 실행 하는 것을 제안 하 고 작업이 완료 될 때까지 기다립니다.

## 변수

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

### -Force
계정을 강제로 장애 조치 (Failover)

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
저장소 계정 개체

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

### -이름
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure.. i m a. 모델. PSStorageAccount

## 상속자

## 관련 링크
