---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964096"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
새 VPN 클라이언트 해지 인증서를 만듭니다.

## 구문

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN(가상 사설 네트워크) 클라이언트 해지 인증서를 만듭니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증에 지정된 인증서를 사용할 수 없습니다.
이 cmdlet은 가상 게이트웨이에 할당되지 않은 독립 실행형 인증서를 만듭니다.
대신 **New-AzVpnClientRevokedCertificate에서** 만든 인증서는 새 게이트웨이를 만들 때 New-AzVirtualNetworkGateway cmdlet과 함께 사용됩니다.
예를 들어 새 인증서를 만들고 새 인증서를 새 인증서라는 변수에 $Certificate.
그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.
예를 들어, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
자세한 내용은 New-AzVirtualNetworkGateway cmdlet에 대한 설명서를 참조하세요.

## 예제

### 예제 1: 새 클라이언트 해지 인증서 만들기
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

이 명령은 새 클라이언트 해지 인증서를 만들고 인증서 개체를 $Certificate.
그런 다음 **New-AzVirtualNetworkGateway** cmdlet에서 이 변수를 사용하여 새 가상 네트워크 게이트웨이에 인증서를 추가할 수 있습니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
새 클라이언트 해지 인증서에 대한 고유한 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -지문
추가할 인증서의 고유 식별자를 지정합니다.
이와 유사한 Windows PowerShell 사용하여 인증서에 대한 지문 정보를 반환할 수 있습니다. `Get-ChildItem -Path Cert:\LocalMachine\Root`
위의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대한 정보를 반환합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## 참고 사항

## 관련 링크

[Add-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


