---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ff3e4f4a69309d2dfa5655fefac3d1c5a0e933f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878945"
---
# Get-AzVpnClientIpsecParameter

## SYNOPSIS
사이트 연결을 위한 가상 네트워크 게이트웨이에 설정 된 vpn Ipsec 매개 변수를 가져옵니다.

## 구문과

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.
**AzVpnClientIpsecParameter** Cmdlet은 게이트웨이 이름 및 리소스 그룹 이름에 기반 하 여 Azure의 게이트웨이에서 설정 된 vpn ipsec 매개 변수 개체를 반환 합니다.

## 예제의

### 1: 사이트 간 연결에 대 한 가상 네트워크 게이트웨이에 설정 된 vpn Ipsec 매개 변수를 가져옵니다.
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

리소스 그룹 "Mygateway" 내에서 이름이 "myGateway" 인 가상 네트워크 게이트웨이에 설정 된 vpn ipsec 매개 변수 개체를 반환 합니다.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### PSVpnClientIPsecParameters에 대 한.

## 상속자

## 관련 링크

[새로운 AzVpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[제거-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-AzVpnClientIpsecParameter](./Set-AzVpnClientIpsecParameter.md)
