---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e0ca615d856e7905127c488c17c039b23051cc0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875702"
---
# Add-AzApplicationGatewayFrontendPort

## SYNOPSIS
응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.

## 구문과

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Add-AzApplicationGatewayFrontendPort** cmdlet은 응용 프로그램 게이트웨이에 프런트 엔드 포트를 추가 합니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이에 프런트 엔드 포트 추가
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.
두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이의 프런트 엔드 포트로 포트 80를 추가 하 고 포트 FrontEndPort01를 이름으로 만듭니다.

## 변수

### -ApplicationGateway
이 cmdlet이 프런트 엔드 포트를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
프런트 엔드 포트의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -포트
포트 번호를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. * PSApplicationGateway

## 상속자

## 관련 링크

[Get-AzApplicationGatewayFrontendPort](./Get-AzApplicationGatewayFrontendPort.md)

[새로운 AzApplicationGatewayFrontendPort](./New-AzApplicationGatewayFrontendPort.md)

[제거-AzApplicationGatewayFrontendPort](./Remove-AzApplicationGatewayFrontendPort.md)

[Set-AzApplicationGatewayFrontendPort](./Set-AzApplicationGatewayFrontendPort.md)


