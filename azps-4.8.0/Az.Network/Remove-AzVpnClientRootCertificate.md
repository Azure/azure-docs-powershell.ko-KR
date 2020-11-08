---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214335"
---
# Remove-AzVpnClientRootCertificate

## SYNOPSIS
기존 VPN 클라이언트 루트 인증서를 제거 합니다.

## 구문과

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에서 지정 된 루트 인증서를 제거 합니다.
루트 인증서는 루트 인증 기관을 식별 하는 x.509 인증서입니다. 게이트웨이에서 사용 되는 다른 모든 인증서는 루트 인증서를 신뢰 합니다.
루트 인증서를 제거 하면 인증을 위해 인증서를 사용 하는 컴퓨터가 더 이상 게이트웨이에 연결할 수 없게 됩니다.
**AzVpnClientRootCertificate** 을 사용할 때는 인증서 이름과 인증서 데이터의 텍스트 표현을 모두 제공 해야 합니다.
인증서의 텍스트 표현에 대 한 자세한 내용은 *Publiccertdata* 매개 변수 설명을 참조 하세요.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이에서 클라이언트 루트 인증서 제거
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

이 예제에서는 가상 네트워크 게이트웨이 ContosoVirtualGateway에서 ContosoRootCertificate 이라는 클라이언트 루트 인증서를 제거 합니다.
첫 번째 명령은 **콘텐츠 가져오기** cmdlet을 사용 하 여 이전에 내보낸 인증서의 텍스트 표현을 가져옵니다. 이 텍스트 표현은 $Text 이라는 변수에 저장 됩니다.
두 번째 명령은 for 루프를 사용 하 여 첫 번째 줄과 마지막 줄을 제외한 $Text에서 모든 텍스트의 압축을 풉니다.
추출 된이 텍스트는 $CertificateText 라는 변수에 저장 됩니다.
세 번째 명령은 **AzVpnClientRootCertificate** cmdlet과 함께 $CertificateText 변수에 저장 된 정보를 사용 하 여 게이트웨이에서 인증서를 제거 합니다.

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
제거할 루트 인증서의 텍스트 표현을 지정 합니다.
텍스트 표현을 얻으려면 .cer 형식 (Base64 사용)에서 인증서를 내보낸 다음 텍스트 편집기에서 결과 파일을 엽니다.
다음과 유사한 출력이 표시 되어야 합니다 (실제 출력에는 여기에 표시 된 간략 한 샘플 보다 많은 줄의 텍스트가 포함 됨).----------MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----인증서를 시작-----합니다. PublicCertData는 첫 번째 줄 (-----시작 인증서-----)과 마지막 줄 (-----END CERTIFICATE-----) 사이의 모든 줄로 구성 됩니다.
다음과 유사한 Windows PowerShell 명령을 사용 하 여 PublicCertData를 검색할 수 있습니다. $Text = Get-Content-경로 "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = = ($i = 1, $i-lt $Text. 길이-1; $i + +) {$Text \[ $i \] }

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

### -VirtualNetworkGatewayName
인증서를 제거 하는 가상 네트워크 게이트웨이의 이름을 지정 합니다.

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
이 cmdlet이 제거 하는 클라이언트 루트 인증서의 이름을 지정 합니다.

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

### 시스템 부울

## 상속자

## 관련 링크

[추가-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[새로운 AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


