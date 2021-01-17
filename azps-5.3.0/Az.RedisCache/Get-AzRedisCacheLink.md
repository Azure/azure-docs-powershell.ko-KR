---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378253"
---
# Get-AzRedisCacheLink

## SYNOPSIS
Redis Cache에 대한 지역 복제 링크를 얻습니다.

## 구문

### AllLinksForCache(기본값)
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
지역 복제 링크 세부 정보를 얻을 수 있는 네 가지 방법이 있습니다. 매개 변수 이름 또는 PrimaryServerName 및/또는 SecondaryServerName을 입력합니다. 이름이 지정된 후 캐시가 있는 모든 링크가 반환됩니다. PrimaryServerName만 제공된 경우 캐시가 기본인 모든 링크가 반환됩니다. SecondaryServerName만 제공된 경우 캐시가 보조인 모든 링크가 반환됩니다. PrimaryServerName 및 SecondaryServerName이 모두 제공된 경우 올바른 역할의 특정 링크가 반환됩니다. 

## 예제

### 예제 1: AllLinksForCache 매개 변수 집합 사용
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1이라는 Redis Cache에 대한 모든 지역 복제 링크를 얻습니다.

### 예제 2: AllLinksForPrimaryCache 매개 변수 집합 사용
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1이라는 Redis Cache가 기본인 지역 복제 링크를 얻습니다.

### 예제 3: AllLinksForSecondaryCache 매개 변수 집합 사용
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache2라는 Redis Cache가 보조인 지역 복제 링크를 얻습니다.

### 예제 4: 매개 변수 집합 SingleLink 사용
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

이 명령은 mycache1이라는 Redis Cache가 기본이고 mycache2라는 Redis Cache가 보조인 단일 지역 복제 링크를 얻습니다.

## PARAMETERS

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

### -Name
redis Cache의 이름입니다.

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
링크에 있는 기본 redis Cache의 이름입니다.

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
링크에 있는 보조 Redis Cache의 이름입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer

## 참고 사항

## 관련 링크

[New-AzRedisCacheLink](./New-AzRedisCacheLink.md)

[Remove-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)