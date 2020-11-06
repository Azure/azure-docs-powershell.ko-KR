---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 704c4c2a11cc83136481573190e745d7a4b2c83f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537099"
---
# Get-AzureRmApplicationSecurityGroup

## SYNOPSIS
응용 프로그램 보안 그룹을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzureRmApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 가져옵니다.

## 예제의

### 예제 1: 모든 응용 프로그램 보안 그룹을 검색 합니다.
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

위의 명령은 구독에 있는 모든 응용 프로그램 보안 그룹을 반환 합니다.

### 예제 2: 리소스 그룹의 응용 프로그램 보안 그룹을 검색 합니다.
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

위의 명령은 리소스 그룹 MyResourceGroup에 속하는 모든 응용 프로그램 보안 그룹을 반환 합니다.

### 예제 3: 특정 응용 프로그램 보안 그룹 검색
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

위의 명령은 리소스 그룹 MyApplicationSecurityGroup 아래에 있는 응용 프로그램 보안 그룹

## 변수

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

### -이름
자원 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. * PSApplicationSecurityGroup

## 상속자

## 관련 링크

[새로운 AzureRmApplicationSecurityGroup](./New-AzureRmApplicationSecurityGroup.md)

[제거-AzureRmApplicationSecurityGroup](./Remove-AzureRmApplicationSecurityGroup.md)

[Get-AzureRmNetworkSecurityRuleConfig](./Get-AzureRmNetworkSecurityRuleConfig.md)

[Get-AzureRmNetworkInterfaceIpConfig](./Get-AzureRmNetworkInterfaceIpConfig.md)
