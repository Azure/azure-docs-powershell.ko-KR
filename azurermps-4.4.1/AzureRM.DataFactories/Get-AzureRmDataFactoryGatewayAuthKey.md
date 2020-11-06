---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9de30d10b34cf666b040c1b25b84e4afeae63a10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537356"
---
# Get-AzureRmDataFactoryGatewayAuthKey

## SYNOPSIS
Azure Data Factory에 대 한 게이트웨이 인증 키를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByFactoryName (기본값)
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataFactoryGatewayAuthKey** cmdlet은 지정 된 Azure Data Factory 게이트웨이에 대 한 게이트웨이 인증 키를 가져옵니다.
이 auth 키의 key1 또는 key2를 사용 하 여 클라우드 서비스에 게이트웨이를 등록 합니다.

## 예제의

### 예제 1: 게이트웨이의 auth 키를 가져옵니다.
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

이 명령은 MyGateway 라는 data factory gateway에 대 한 게이트웨이 인증 키를 가져옵니다.

## 변수

### -DataFactoryName
Data factory 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### --게이트웨이 이름
Data factory 게이트웨이 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
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

### -InputObject
Data factory 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
System. 문자열

## 출력

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리

## 관련 링크

[새로운 AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [새로운 AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)

