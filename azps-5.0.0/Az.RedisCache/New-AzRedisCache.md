---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218477"
---
# New-AzRedisCache

## SYNOPSIS
Redis 캐시를 만듭니다.

## 구문과

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.

## 예제의

### 예제 1: Redis 캐시 만들기
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

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
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.Nullable`1[System.Boolean]
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -없음 Tls 버전
클라이언트가 캐시에 연결 하는 데 필요한 TLS 버전을 지정 합니다.

```yaml
Type: System.String
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
Type: System.String
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
자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 http://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 http://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: System.Collections.Hashtable
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
Type: System.String
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
Type: System.Nullable`1[System.Int32]
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
- P5
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
- 53GB 기본 값은 1GB 또는 C1입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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
- Premium 기본 값은 표준입니다.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: System.Collections.Hashtable
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
Type: System.Collections.Hashtable
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
Type: System.String[]
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

### 시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### 시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])

### System.webserver []

## 출력

### RedisCacheAttributesWithAccessKeys. 모델. m e.

## 상속자

## 관련 링크

[Get-AzRedisCache](./Get-AzRedisCache.md)

[제거-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)


