---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042565"
---
# New-AzCosmosDBAccount

## SYNOPSIS
새 CosmosDB 계정을 만듭니다.

## 구문과

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
지정 된 ResourceGroup에 새 CosmosDB Account를 만듭니다.

## 예제의

### 예제 1
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

이름 databaseAccountName을 사용 하는 새 CosmosDB 계정이 ResourceGroup resourceGroupName에 만들어집니다.

## 변수

### -ApiKind
만들 Cosmos DB 데이터베이스 계정의 유형입니다.
허용 되는 값: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.
기본값: GlobalDocumentDB

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultConsistencyLevel
Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.
허용 되는 값: BoundedStaleness, ConsistentPrefix, 궁극적인, Session, Strong

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableKeyBasedMetadataWriteAccess
계정 키를 통해 메타 데이터 리소스 (데이터베이스, 컨테이너, 처리량)에 대 한 쓰기 작업을 사용 하지 않도록 설정

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable자동 장애 조치
비활성으로 인해 지역을 사용할 수 없는 드문 이벤트에서 쓰기 영역의 자동 장애 조치를 사용 하도록 설정 합니다.
자동 장애 조치 (failover)로 인해 계정에 대 한 새 쓰기 영역이 만들어지고 계정에 대해 구성 된 장애 조치 (failover) 우선 순위에 따라 선택 됩니다.
허용 된 값: false, true

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableMultipleWriteLocations
여러 쓰기 위치를 사용 하도록 설정 합니다.
허용 된 값: false, true

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableVirtualNetwork
Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용 하도록 설정 합니다.
허용 된 값: false, true

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpRangeFilter
방화벽 지원.
지정 된 데이터베이스 계정에 대 한 클라이언트 Ip의 허용 목록으로 포함할 IP 주소 또는 IP 주소 범위 집합을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.
장애 조치 우선 순위에 따라 정렬 되는 문자열의 배열입니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocationObject
Cosmos DB 데이터베이스 계정에 위치를 추가 합니다. PSLocation 개체의 배열입니다.

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxStalenessIntervalInSeconds
제한 된 부실 일관성에 사용 하는 경우이 값은 부실 (timespan) 허용의 시간을 나타냅니다.
이 값에 허용 된 범위는 5-86400입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxStalenessPrefix
제한 된 만료 일관성에 사용 하는 경우이 값은 허용 되는 부실 요청 수를 나타냅니다.
이 값에 허용 되는 범위는 1-2147483647입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Cosmos DB 데이터베이스 계정의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccess
이 서버에 대 한 공개 끝점 액세스가 허용 되는지 여부 사용할 수 있는 값은 다음과 같습니다. ' Enabled ', ' Disabled '

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
태그의 해시 테이블 (키-값 쌍)
빈 문자열을 사용 하 여 기존 태그 지우기

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRule
가상 네트워크에 대 한 ACL의 문자열 값 배열입니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkRuleObject
가상 네트워크에 대 한 PSVirtualNetworkRuleObjects의 배열입니다.

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### CosmosDB [] PSCorsRule []

## 출력

### Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount

## 상속자

## 관련 링크
