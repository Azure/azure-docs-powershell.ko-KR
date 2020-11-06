---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529167"
---
# Find-AzureRmResourceGroup

## SYNOPSIS
리소스 그룹을 검색 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Find-AzureRmResourceGroup** cmdlet은 지정 된 매개 변수를 사용 하 여 리소스 그룹을 검색 합니다.

## 예제의

### 예제 1: 모든 리소스 그룹 찾기
```
PS C:\>Find-AzureRmResourceGroup
```

이 명령은 모든 리소스 그룹을 찾습니다.

### 예제 2: 태그별 이름으로 리소스 그룹 찾기
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

이 명령은 testtag 라는 태그가 있는 모든 리소스 그룹을 찾습니다.

### 예제 3: 태그 이름 및 값을 기준으로 리소스 그룹 찾기
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

이 명령은 testtag 이라는 태그와 testtag 값이 있는 모든 리소스 그룹을 찾습니다.

## 변수

### -ApiVersion
사용할 리소스 공급자 API의 버전을 지정 합니다. 버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.

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

### 태그
결과를 필터링 하는 해시 테이블로 태그 정보를 지정 합니다. 다음과 같은 형식을 사용 합니다.

@ {tagName = $null} 또는 @ {tagName = ' tagValue '}.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### System.webserver. 자동. PSObject

## 상속자

## 관련 링크

