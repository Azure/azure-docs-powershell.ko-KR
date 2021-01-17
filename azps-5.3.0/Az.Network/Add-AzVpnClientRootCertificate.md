---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491813"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
VPN 클라이언트 루트 인증서를 추가합니다.

## 구문

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Add-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 루트 인증서를 추가합니다.
루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다.
기본적으로 게이트웨이에서 사용되는 모든 인증서는 루트 인증서를 신뢰합니다.
이 cmdlet은 기존 인증서를 게이트웨이 루트 인증서로 할당합니다.
X.509 인증서를 사용할 수 없는 경우 공개 키 인프라를 통해 인증서를 생성하거나 인증서 생성기(예: makecert.exe.
루트 인증서를 추가하려면 인증서 이름을 지정하고 인증서의 텍스트 전용 표현을 제공해야 합니다(자세한 내용은 *PublicCertData* 매개 변수 참조).
Azure를 사용하면 게이트웨이에 두 개 이상의 루트 인증서를 할당할 수 있습니다.
여러 루트 인증서는 여러 회사의 사용자를 포함 하는 조직에 의해 배포되는 경우가 종종 있습니다.

## 예제

### 예제 1: 가상 게이트웨이에 클라이언트 루트 인증서 추가
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

이 예제에서는 ContosoVirtualGateway라는 가상 게이트웨이에 클라이언트 루트 인증서를 추가합니다.
첫 번째 명령은 **Get-Content** cmdlet을 사용하여 루트 인증서의 이전에 내보낼 텍스트 표현을 얻게 하여 해당 텍스트 데이터를 $Text.
그런 다음 두 번째 명령은 for 루프를 사용하여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출합니다.
추출된 텍스트는 이 변수에 $CertificateText.
그런 다음, 세 번째 명령은 **Add-AzVpnClientRootCertificate** cmdlet과 함께 $CertificateText 저장된 텍스트를 사용하여 루트 인증서를 게이트웨이에 추가합니다.

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

### -PublicCertData
추가할 루트 인증서의 텍스트 표현을 지정합니다.
텍스트 표현을 얻습니다. 인증서를 .cer 형식으로 내보내고(Base64 인코딩 사용) 결과 파일을 텍스트 편집기에서 열 수 있습니다.
이 경우 다음과 유사한 출력이 표시됩니다(실제 출력에는 여기에 표시된 약어 샘플보다 더 많은 텍스트 줄이 포함되어 있습니다. ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJ end CERTIFICATE ----- END CERTIFICATE ----- PublicCertData는 파일의 첫 번째 줄(----- BEGIN CERTIFICATE -----)과 마지막 줄(----- END CERTIFICATE -----) 사이의 모든 줄로 ----- 있습니다.
이와 유사한 명령으로 이 Windows PowerShell 검색할 수 있습니다. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
루트 인증서가 할당된 리소스 그룹의 이름을 지정합니다.
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

### -VirtualNetworkGatewayName
인증서가 추가되는 가상 네트워크 게이트웨이의 이름을 지정합니다.

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

### -VpnClientRootCertificateName
이 cmdlet이 추가하는 클라이언트 루트 인증서의 이름을 지정합니다.

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

### Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate

## 참고 사항

## 관련 링크

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


