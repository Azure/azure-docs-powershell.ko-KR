---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: 64a8282cb1dc99b32e0296ebf97f59ab96b5fd96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524411"
---
# Test-AzureRmEventHubName

## SYNOPSIS
지정 된 네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 사용 가능 여부를 확인 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NamespaceCheckNameAvailabilitySet (기본값)
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
네임 스페이스 이름 또는 별칭 (DR 구성 이름)의 **AzureRmEventhubName** Cmdlet 검사 사용 가능성

## 예제의

### 예제 1
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

사용 가능한 경우 네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 True로 반환 합니다.

### 예제 2
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

네임 스페이스 이름 ' MyNameSapceName '의 가용성 상태를 False로 반환 합니다.

### 예제 3
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

사용 가능한 경우 ' MyNameSapceName ' 네임 스페이스에 대 한 별칭 이름 ' myAliasName '의 사용 가능 상태를 True로 반환 합니다.

## 변수

### -AliasName
DR 구성 이름-별칭 이름

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
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

### -Namespace
Eventhub 네임 스페이스 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### PSCheckNameAvailabilityResultAttributes (.).

## 상속자

## 관련 링크
