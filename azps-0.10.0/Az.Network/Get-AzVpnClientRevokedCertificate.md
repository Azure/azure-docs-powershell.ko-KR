---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 3151ffb45064d1cb85b69d11a1ccbd49d4c045e8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875489"
---
# Get-AzVpnClientRevokedCertificate

## SYNOPSIS
VPN 클라이언트 해지 인증서에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당 된 클라이언트 해지 인증서에 대 한 정보를 반환 합니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.
**Get-AzVpnClientRevokedCertificate** 를 사용 하면 게이트웨이에서 모든 클라이언트 해지 인증서에 대 한 정보를 반환 하거나 *VpnClientRevokedCertificateName* 매개 변수를 사용 하 여 단일 인증서에 대 한 정보를 가져올 수 있습니다.

## 예제의

### 예제 1: 모든 클라이언트 철회 인증서에 대 한 정보 가져오기
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

이 명령은 ContosoVirtualNetworkGateway 이라는 가상 네트워크 게이트웨이에 연결 된 모든 클라이언트 해지 인증서에 대 한 정보를 가져옵니다.

### 예제 2: 특정 클라이언트 해지 인증서에 대 한 정보 가져오기
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

이 명령은 예제 1에 표시 된 명령의 변형입니다.
그러나이 경우 *VpnClientRevokedCertificateName* 매개 변수는 반환 된 데이터를 특정 클라이언트로 제한 하는 데 사용 됩니다 (해지 된 인증서: 이름이 ContosoRevokedClientCertificate 인 인증서).

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

### -ResourceGroupName
가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.

리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.

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

### -VirtualNetworkGatewayName
해지 된 인증서 정보가 할당 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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

### -VpnClientRevokedCertificateName
이 cmdlet이 가져오는 VPN 클라이언트 인증서의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

###  
**Get-AzVpnClientRevokedCertificate** **PSVpnClientRevokedCertificate** 개체의 인스턴스를 반환 합니다.

## 상속자

## 관련 링크

[추가-AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[새로운 AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[제거-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


