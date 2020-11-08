---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226218"
---
# Add-AzVpnClientRevokedCertificate

## SYNOPSIS
VPN 클라이언트 해지 인증서를 추가 합니다.

## 구문과

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Add-AzVpnClientRevokedCertificate** cmdlet은 가상 네트워크 게이트웨이에 클라이언트 해지 인증서를 할당 합니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증을 위해 지정 된 인증서를 사용 하지 못하도록 합니다.
이 cmdlet을 사용 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이에 새 클라이언트-해지 인증서 추가
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

이 명령은 ContosoVirtualNetwork 이라는 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서를 추가 합니다.
인증서를 추가 하려면 인증서 이름과 인증서 지문을 모두 지정 해야 합니다.

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

### -ResourceGroupName
가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.
리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.

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

### -지문
추가할 인증서의 고유 식별자를 지정 합니다.
예:-손도장 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 다음과 유사한 Windows PowerShell 명령을 사용 하 여 인증서에 대 한 지문 정보를 얻을 수 있습니다 `Get-ChildItem -Path Cert:\LocalMachine\Root` .
앞의 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대 한 정보를 가져옵니다.

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

### -VirtualNetworkGatewayName
인증서를 추가 해야 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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

### -VpnClientRevokedCertificateName
추가할 VPN 클라이언트 인증서의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### PSVpnClientRevokedCertificate에 대 한.

## 상속자

## 관련 링크

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[새로운 AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[제거-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


