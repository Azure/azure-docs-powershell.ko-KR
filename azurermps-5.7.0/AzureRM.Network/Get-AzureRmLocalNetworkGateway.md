---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537703"
---
# Get-AzureRmLocalNetworkGateway

## SYNOPSIS
로컬 네트워크 게이트웨이를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.

**AzureRmLocalNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 온-프레미스 gateway를 나타내는 개체를 반환 합니다.

## 예제의

### 1: 로컬 네트워크 게이트웨이 가져오기
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 반환 합니다.

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

### -이름
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### Microsoft. 네트워크. PSLocalNetworkGateway

## 상속자

## 관련 링크

