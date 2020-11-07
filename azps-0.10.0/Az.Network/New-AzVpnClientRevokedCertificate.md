---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: f9dbdaf531f4ccc35543dc542dc0637b9795360e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875383"
---
# New-AzVpnClientRevokedCertificate

## SYNOPSIS
새 VPN 클라이언트 해지 인증서를 만듭니다.

## 구문과

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN (가상 사설망) 클라이언트 해지 인증서를 만듭니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.

이 cmdlet은 가상 게이트웨이에 할당 되지 않은 독립 실행형 인증서를 만듭니다.
대신 새 게이트웨이를 만들 때 **AzVpnClientRevokedCertificate** 에서 만든 인증서가 New-AzVirtualNetworkGateway cmdlet과 함께 사용 됩니다.
예를 들어 새 인증서를 만들고이를 $Certificate 이라는 변수에 저장 한다고 가정 합니다.
그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.
예를 들어

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

자세한 내용은 New-AzVirtualNetworkGateway cmdlet에 대 한 설명서를 참조 하세요.

## 예제의

### 예제 1: 새 클라이언트 만들기-해지 된 인증서
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

이 명령은 새 클라이언트-해지 된 인증서를 만들고 $Certificate 이라는 변수에 인증서 개체를 저장 합니다.
그런 다음 새 가상 네트워크 게이트웨이에 인증서를 추가 하기 위해 **AzVirtualNetworkGateway** cmdlet에서이 변수를 사용할 수 있습니다.

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
새 클라이언트 해지 인증서의 고유한 이름을 지정 합니다.

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

### -지문
추가할 인증서의 고유 식별자를 지정 합니다.

다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다.

`Get-ChildItem -Path Cert:\LocalMachine\Root`

앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 반환 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

###  
이 cmdlet은 파이프라인 입력을 허용 하지 않습니다.

## 출력

###  
이 cmdlet은 **PSVpnClientRevokedCertificate** 개체의 새 인스턴스를 만듭니다.

## 상속자

## 관련 링크

[추가-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[제거-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


