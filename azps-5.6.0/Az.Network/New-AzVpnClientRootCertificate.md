---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964091"
---
# New-AzVpnClientRootCertificate

## SYNOPSIS
새 VPN 클라이언트 루트 인증서를 만듭니다.

## 구문

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 사용할 새 VPN 루트 인증서를 만듭니다.
루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다. 게이트웨이에서 사용되는 다른 모든 인증서는 루트 인증서를 신뢰합니다.
이 cmdlet은 가상 게이트웨이에 할당되지 않은 독립 실행형 인증서를 만듭니다.
대신 **New-AzVpnClientRootCertificate에서** 만든 인증서는 새 게이트웨이를 만들 때 New-AzVirtualNetworkGateway cmdlet과 함께 사용됩니다.
예를 들어 새 인증서를 만들고 새 인증서를 새 인증서라는 변수에 $Certificate.
그런 다음 새 가상 게이트웨이를 만들 때 해당 인증서 개체를 사용할 수 있습니다.
예를 들어, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
자세한 내용은 New-AzVirtualNetworkGateway cmdlet에 대한 설명서를 참조하세요.

## 예제

### 예제 1: 클라이언트 루트 인증서 만들기
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

이 예제에서는 클라이언트 루트 인증서를 만들고 인증서 개체를 $Certificate.
그런 **다음, New-AzVirtualNetworkGateway** cmdlet에서 이 변수를 사용하여 새 가상 네트워크 게이트웨이에 루트 인증서를 추가할 수 있습니다.
첫 번째 명령은 **Get-Content** cmdlet을 사용하여 루트 인증서의 이전에 내보낼 텍스트 표현을 얻게 됩니다. 텍스트 데이터가 이라는 변수에 $Text.
그런 다음, 두 번째 명령은 for loop를 사용하여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출하고, 추출된 텍스트를 변수에 저장하여 $CertificateText.
세 번째 명령은 **New-AzVpnClientRootCertificate** cmdlet을 사용하여 인증서를 만들고 만든 개체를 $Certificate.

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
새 클라이언트 루트 인증서의 이름을 지정합니다.

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

### -PublicCertData
추가할 루트 인증서의 텍스트 표현을 지정합니다.
텍스트 표현을 얻었다면 .cer 형식으로 인증서를 내보낼 수 있습니다(Base64 인코딩 사용) 텍스트 편집기에서 결과 파일을 니다.
이와 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 많은 텍스트 줄이 포함되어 있습니다 -----. MIIC13FAAXC3671Auij9HHhgUNEW8343NMJklo에서 BEGIN CERTIFICATE ----- 09982CVVFAw8w ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 ----- 있습니다.
$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText =($i=1; $i -lt $Text.length -1 ; $i+){$i+){$Text+){$Text $i } Windows PowerShell \[ \]

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## 참고 사항

## 관련 링크

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


