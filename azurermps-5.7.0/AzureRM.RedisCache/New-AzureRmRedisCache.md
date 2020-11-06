---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528857"
---
# New-AzureRmRedisCache

## SYNOPSIS
Redis 캐시를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.

## 예제의

### 예제 1: Redis 캐시 만들기
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

이 명령은 Redis Cache를 만듭니다.

### 예제 2: 표준 SKU Redis 캐시 만들기
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

이 명령은 Redis Cache를 만듭니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNonSslPort
비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.
기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
Redis 캐시를 만들 위치를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 대한민국 미국 중부
- 미국 중부 US
- 중부 US
- 유럽 서유럽
- 동유럽
- 미국 서 부
- 미국 동부
- 미국 동부 2
- 일본 동부
- 일본 서쪽
- 브라질 남부
- 동남 아시아
- 동아시아
- 오스트레일리아 동부
- 오스트레일리아 남동쪽

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxMemoryPolicy
이 매개 변수는 더 이상 사용 되지 않습니다.
*Redisconfiguration* 매개 변수를 사용 하 여 maxmemory-정책을 설정 합니다.
예를 들어: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
만들 Redis 캐시의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
Redis 구성 설정을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- rdb-백업-사용 가능.
Redis 데이터 지 속성을 사용 하도록 지정 합니다.
프리미엄 계층만.
- rdb-저장소-연결 문자열입니다.
Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.
프리미엄 계층만.
- rdb-백업-빈도
Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.
프리미엄 계층만. 
- maxmemory-예약 됨.
비 캐시 프로세스에 예약 된 메모리를 구성 합니다.
표준 및 프리미엄 계층. 
- maxmemory-정책.
캐시에 대 한 제거 정책을 구성 합니다.
모든 가격 책정 계층 
- notify-keyspace-이벤트
Keyspace 알림을 구성 합니다.
표준 및 프리미엄 계층. 
- hash-최대 ziplist-항목.
작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.
표준 및 프리미엄 계층. 
- hash-max-ziplist-값.
작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.
표준 및 프리미엄 계층. 
- set-max-intset-항목
작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.
표준 및 프리미엄 계층. 
- zset-max-ziplist 항목.
작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.
표준 및 프리미엄 계층. 
- zset-max-ziplist-value.
작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.
표준 및 프리미엄 계층. 
- databases.
데이터베이스 수를 구성 합니다.
이 속성은 캐시 생성 시에만 구성할 수 있습니다.
표준 및 프리미엄 계층.

자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -버전 재
이 매개 변수는 더 이상 사용 되지 않으며 이후 릴리스에서 제거 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Redis 캐시를 만들 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- raid-1
- 2
- 3-4
- 4(tcp/ipv4)
- 5mb
- 26
- 7
- 20cm(8
- 되었는지 
- 1천만

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -크기
Redis 캐시의 크기를 지정 합니다.
유효한 값은 다음과 같습니다. 

- P1
- 즉
- P3
- P4
- C0
- C1
- 만족할
- C3
- C4
- C 5
- C6
- 250MB
- 1GB
- 2.5 GB
- 6GB
- 13GB
- 26GB
- 53GB

기본값은 1GB 또는 C1입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
만들 Redis Cache의 SKU를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 기본적
- 표준이
- Premium

기본값은 표준입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticIP
Redis 캐시에 대 한 서브넷의 고유한 IP 주소를 지정 합니다.

이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -서브넷
Redis 캐시를 배포할 서브넷의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
태그를 나타내는 해시 테이블입니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
이 매개 변수는 더 이상 사용 되지 않습니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Redis 캐시를 배포할 가상 네트워크의 리소스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
영역 목록.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.

## 출력

### RedisCacheAttributesWithAccessKeys. 모델. m e.
이 cmdlet은 기본 및 보조 선택 키를 포함 하 여 Redis 캐시의 모든 특성을 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[제거-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


