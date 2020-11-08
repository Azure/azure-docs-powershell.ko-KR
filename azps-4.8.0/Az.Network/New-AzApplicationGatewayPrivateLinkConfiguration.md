---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214874"
---
# New-AzApplicationGatewayPrivateLinkConfiguration

## SYNOPSIS
응용 프로그램 게이트웨이에 대 한 개인 링크 구성을 만듭니다.

## 구문과

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet은 Azure application gateway에 대 한 PrivateLink 구성을 만듭니다.
비공개 링크 기능을 사용 하려면 개인 링크 구성을 프런트 엔드 ip 구성에 연결 해야 합니다.
하나의 개인 링크 구성은 응용 프로그램 게이트웨이에서 하나의 프런트 엔드 ip 구성에만 연결할 수 있습니다.

## 예제의

### 예제 1: 단일 Ip 구성을 사용 하 여 개인 링크 구성 만들기
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

이 명령은 ' privateLinkConfig01 ' 이라는 PrivateLink 구성을 만들고 그 결과를 $PrivateLinkConfiguration 이라는 변수에 저장 합니다.

### 예제 2: 여러 Ip 구성을 사용 하 여 개인 링크 구성 만들기
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

이 명령은 두 개의 ipConfigurations 있는 ' privateLinkConfig01 ' PrivateLink 구성을 만들고 그 결과를 $PrivateLinkConfiguration 이라는 변수에 저장 합니다. 

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpConfiguration
IpConfiguration 목록

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
PrivateLink 구성의 이름입니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### PSApplicationGatewayPrivateLinkIpConfiguration [] (으)로

## 출력

### PSApplicationGatewayPrivateLinkConfiguration에 대 한.

## 상속자

## 관련 링크

[Get-AzApplicationGatewayPrivateLinkConfiguration](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[추가-AzApplicationGatewayPrivateLinkConfiguration](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[제거-AzApplicationGatewayPrivateLinkConfiguration](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[Set-AzApplicationGatewayPrivateLinkConfiguration](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
