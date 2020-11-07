---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 8129634e940624fe09dad4a1199f96dbcf5162bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872557"
---
# Get-AzRedisCacheLink

## SYNOPSIS
Redis Cache에 대 한 지역 복제 링크를 가져옵니다.

## 구문과

### All링크 Forcache (기본값)
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### All링크 Forprimarycache
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### All링크 Forsecondarycache
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
지리적 복제 링크 세부 정보는 네 가지 방법으로 얻을 수 있습니다. 매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 제공 합니다. Name이 지정 되 면 캐시가 존재 하는 모든 링크가 반환 됩니다. PrimaryServerName만 지정 하는 경우 캐시가 기본으로 있는 모든 링크는 반환 됩니다. SecondaryServerName만 지정 하는 경우 캐시가 보조 인 모든 링크는 반환 됩니다. PrimaryServerName 및 SecondaryServerName이 모두 지정 된 경우 올바른 역할의 특정 링크가 반환 됩니다. 

## 예제의

### 예제 1: using 매개 변수 설정 가져오기 All링크 Forcache
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1 이라는 Redis Cache에 대 한 모든 지역/복제 링크를 가져옵니다.

### 예제 2: using 매개 변수 설정 가져오기 All링크 Forprimarycache
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1 이라는 Redis 캐시가 기본 인 지역 복제 링크를 가져옵니다.

### 예제 3: 사용 하는 매개 변수 설정 Get Allindex Forsecondarycache
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache2 이라는 Redis 캐시가 보조 인 지역 복제 링크를 가져옵니다.

### 예제 4: SingleLink set 매개 변수를 사용 하 여 가져오기
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1 이라는 Redis 캐시가 기본 인 단일 지역 복제 링크와 mycache2 이라는 Redis Cache를 보조로 가져옵니다.

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
Redis cache의 이름입니다.

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Link의 기본 redis cache 이름입니다.

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Link의 보조 redis 캐시 이름입니다.

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### PSRedisLinkedServer. 모델. m e.

## 상속자

## 관련 링크

[새로운 AzRedisCacheLink](./New-AzRedisCacheLink.md)

[제거-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[새로운 AzRedisCache](./New-AzRedisCache.md)

[제거-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)