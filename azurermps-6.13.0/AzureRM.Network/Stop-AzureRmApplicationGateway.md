---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702788"
---
# Stop-AzureRmApplicationGateway

## SYNOPSIS
응용 프로그램 게이트웨이를 중지 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 중지 합니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 중지
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

이 명령은 $AppGw 변수에 저장 된 응용 프로그램 게이트웨이를 중지 합니다.

## 변수

### -ApplicationGateway
이 cmdlet이 중지 하는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

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

### Microsoft. * PSApplicationGateway
매개 변수: ApplicationGateway (ByValue)

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[새로운 AzureRmApplicationGateway](./New-AzureRmApplicationGateway.md)

[제거-AzureRmApplicationGateway](./Remove-AzureRmApplicationGateway.md)

[Set-AzureRmApplicationGateway](./Set-AzureRmApplicationGateway.md)

[시작-AzureRmApplicationGateway](./Start-AzureRmApplicationGateway.md)


