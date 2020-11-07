---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700484"
---
# Get-AzVirtualNetworkGateway

## SYNOPSIS
가상 네트워크 게이트웨이를 가져옵니다.

## 구문과

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.
**AzVirtualNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름에 따라 Azure에서 게이트웨이의 개체를 반환 합니다.

## 예제의

### 1: 가상 네트워크 게이트웨이 가져오기
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

리소스 그룹 "myRG" 내에서 이름이 "myGateway1" 인 가상 네트워크 게이트웨이의 개체를 반환 합니다.

### 2: 가상 네트워크 게이트웨이 가져오기
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

리소스 그룹 "Mygateway" 내에서 "myGateway"로 시작 하는 모든 가상 네트워크 게이트웨이를 반환 합니다.

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
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### PSVirtualNetworkGateway에 대 한.

## 상속자

## 관련 링크

[새로운 AzVirtualNetworkGateway](./New-AzVirtualNetworkGateway.md)

[제거-AzVirtualNetworkGateway](./Remove-AzVirtualNetworkGateway.md)

[다시 설정-AzVirtualNetworkGateway](./Reset-AzVirtualNetworkGateway.md)

[크기 조정-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGateway](./Set-AzVirtualNetworkGateway.md)
