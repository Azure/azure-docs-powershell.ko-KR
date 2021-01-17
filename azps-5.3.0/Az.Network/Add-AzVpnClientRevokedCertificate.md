---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491816"
---
# Add-AzVpnClientRevokedCertificate

## SYNOPSIS
VPN 클라이언트 해지 인증서를 추가합니다.

## 구문

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Add-AzVpnClientRevokedCertificate** cmdlet은 클라이언트 해지 인증서를 가상 네트워크 게이트웨이에 할당합니다.
클라이언트 해지 인증서는 클라이언트 컴퓨터가 인증에 지정된 인증서를 사용하지 못하도록 방지합니다.
이 cmdlet을 사용하려면 인증서 이름과 인증서 지문을 모두 지정해야 합니다.

## 예제

### 예제 1: 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서 추가
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

이 명령은 ContosoVirtualNetwork라는 가상 네트워크 게이트웨이에 새 클라이언트 해지 인증서를 추가합니다.
인증서를 추가하려면 인증서 이름과 인증서 지문을 모두 지정해야 합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.
리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.

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

### -Thumbprint
추가할 인증서의 고유 식별자를 지정합니다.
예: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 다음과 유사한 Windows PowerShell 명령을 사용하여 인증서에 대한 지문 정보를 얻을 수 `Get-ChildItem -Path Cert:\LocalMachine\Root` 있습니다.
이전 명령은 루트 인증서 저장소에 있는 모든 로컬 컴퓨터 인증서에 대한 정보를 얻습니다.

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
인증서를 추가해야 하는 가상 네트워크 게이트웨이의 이름을 지정합니다.

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
추가할 VPN 클라이언트 인증서의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate

## 참고 사항

## 관련 링크

[Get-AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[New-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


