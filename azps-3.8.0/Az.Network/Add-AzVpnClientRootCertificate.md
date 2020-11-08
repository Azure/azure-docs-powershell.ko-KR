---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: efb8640f765468432a2927f865ce9f67c7b9164f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042518"
---
# Add-AzVpnClientRootCertificate

## SYNOPSIS
VPN 클라이언트 루트 인증서를 추가 합니다.

## 구문과

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Add-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 루트 인증서를 추가 합니다.
루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다.
설계상 게이트웨이에서 사용 되는 모든 인증서는 루트 인증서를 신뢰 합니다.
이 cmdlet은 기존 인증서를 게이트웨이 루트 인증서로 할당 합니다.
X.509 인증서를 사용할 수 없는 경우 공개 키 인프라를 통해 하나를 생성 하거나 makecert.exe 등의 인증서 생성기를 사용할 수 있습니다.
루트 인증서를 추가 하려면 인증서 이름을 지정 하 고 인증서의 텍스트 전용 표현을 제공 해야 합니다 (자세한 내용은 *PublicCertData* 매개 변수 참조).
Azure를 사용 하 여 게이트웨이에 두 개 이상의 루트 인증서를 할당할 수 있습니다.
여러 루트 인증서는 두 개 이상의 회사의 사용자를 포함 하는 조직에 의해 배포 되는 경우가 많습니다.

## 예제의

### 예제 1: 가상 게이트웨이에 클라이언트 루트 인증서 추가
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

이 예제에서는 클라이언트 루트 인증서를 ContosoVirtualGateway 이라는 가상 게이트웨이에 추가 합니다.
첫 번째 명령은 **가져오기-내용** cmdlet을 사용 하 여 루트 인증서의 이전 내보낸 텍스트 표현을 가져오고 해당 텍스트 데이터를 $Text 라는 변수에 저장 합니다.
두 번째 명령은 for 루프를 사용 하 여 첫 번째 줄과 마지막 줄을 제외한 모든 텍스트를 추출 합니다.
추출 된 텍스트는 $CertificateText 라는 변수에 저장 됩니다.
세 번째 명령은 **AzVpnClientRootCertificate** cmdlet을 사용 하 여 $CertificateText에 저장 된 텍스트를 사용 하 여 게이트웨이에서 루트 인증서를 추가 합니다.

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

### -PublicCertData
추가할 루트 인증서의 텍스트 표현을 지정 합니다.
텍스트 표현을 얻으려면 .cer 형식 (Base64 인코딩 사용)으로 인증서를 내보낸 다음 텍스트 편집기에서 결과 파일을 엽니다.
이렇게 하면 다음과 유사한 출력이 표시 됩니다 (실제 출력에는 여기에 표시 된 간략 한 샘플 보다 많은 줄의 텍스트가 포함 됨).----------MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----인증서를 시작 하는 것을 요청-----PublicCertData는 첫 번째 줄 (-----시작 인증서-----)과 마지막 줄 (-----END CERTIFICATE-----) 사이의 모든 줄로 구성 됩니다.
다음과 유사한 Windows PowerShell 명령을 사용 하 여이 데이터를 검색할 수 있습니다. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
루트 인증서가 할당 된 리소스 그룹의 이름을 지정 합니다.
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

### -VirtualNetworkGatewayName
인증서가 추가 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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
이 cmdlet에 추가 되는 클라이언트 루트 인증서의 이름을 지정 합니다.

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

### PSVpnClientRootCertificate에 대 한.

## 상속자

## 관련 링크

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[새로운 AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[제거-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


