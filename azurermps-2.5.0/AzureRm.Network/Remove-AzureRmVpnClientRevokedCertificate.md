---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882841"
---
# Remove-AzureRmVpnClientRevokedCertificate

## SYNOPSIS
VPN 클라이언트 해지 인증서를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.
클라이언트 철회 인증서를 제거한 경우 클라이언트 컴퓨터는 이전에 금지 된 인증서를 사용 하 여 VPN (가상 사설망) 연결을 만들 수 있습니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서 제거
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에서 클라이언트 해지 인증서를 제거 합니다.
클라이언트 해지 인증서를 제거 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.

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

### -지문
제거할 인증서의 고유 식별자를 지정 합니다.

다음과 같은 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 반환할 수 있습니다.

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

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

### -VirtualNetworkGatewayName
인증서가 할당 된 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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
제거할 VPN 클라이언트 인증서의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[새로운 AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)


