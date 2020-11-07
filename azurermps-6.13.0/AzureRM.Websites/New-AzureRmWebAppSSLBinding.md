---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 33efe02dd463334745e39d846d0b43c2ccd9dd6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704090"
---
# New-AzureRmWebAppSSLBinding

## SYNOPSIS
Azure Web App에 대 한 SSL 인증서 바인딩을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### S1
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 구성원과
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 시스템이
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Socket Layer) 인증서 바인딩을 만듭니다.
Cmdlet은 다음과 같은 두 가지 방법으로 SSL 바인딩을 만듭니다. 
- 웹 앱을 기존 인증서에 바인딩할 수 있습니다.
- 새 인증서를 업로드 한 다음 웹 앱을 새 인증서에 바인딩할 수 있습니다.
사용 하는 방법에 관계 없이 인증서와 웹 앱은 동일한 Azure 리소스 그룹과 연결 되어 있어야 합니다.
리소스 그룹 A에 웹 앱이 있고 리소스 그룹 B의 인증서에 웹 앱을 바인딩하는 경우 유일한 방법은 리소스 그룹 A에 인증서 복사본을 업로드 하는 것입니다. 새 인증서를 업로드 하는 경우 Azure SSL 인증서에 대 한 다음 요구 사항을 염두에 두어야 합니다. 
- 인증서에는 개인 키가 포함 되어 있어야 합니다. 
- 인증서는 PFX (개인 정보 교환) 형식을 사용 해야 합니다. 
- 인증서의 주체 이름은 웹 앱에 액세스 하는 데 사용 되는 도메인과 일치 해야 합니다. 
- 인증서는 최소 2048 비트 암호화를 사용 해야 합니다.

## 예제의

### 예제 1: 웹 앱에 인증서 바인딩
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

이 명령은 기존 Azure 인증서 (지문이 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 인 인증서)를 ContosoWebApp 이라는 웹 앱에 바인딩합니다.

## 변수

### -CertificateFilePath
업로드할 인증서의 파일 경로를 지정 합니다.
*Certificatefilepath* 매개 변수는 인증서가 아직 Azure에 업로드 되지 않은 경우에만 필요 합니다.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
인증서 암호를 해독 합니다.

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
웹 앱의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.
동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -슬롯
웹 앱 배포 슬롯의 이름을 지정 합니다.
Get-AzureRMWebAppSlot cmdlet을 사용 하 여 슬롯을 얻을 수 있습니다.
배포 슬롯은 인터넷을 통해 해당 앱에 액세스할 수 없는 웹 앱을 준비 하 고 유효성을 검사할 수 있는 방법을 제공 합니다.
일반적으로 변경 내용을 준비 사이트에 배포 하 고 해당 변경의 유효성을 검사 한 다음 프로덕션 (인터넷 액세스 가능) 사이트에 배포 합니다.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
인증서를 사용할 수 있는지 여부를 지정 합니다.
*Sslstate* 매개 변수를 1로 설정 하 여 인증서를 활성화 하거나, *sslstate* 를 0으로 설정 하 여 인증서를 비활성화 합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -지문
인증서에 대 한 고유 식별자를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web app
웹 앱을 지정 합니다.
웹 앱을 가져오려면 Get-AzureRmWebApp cmdlet을 사용 합니다.
*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
새 SSL 바인딩이 생성 되는 웹 앱의 이름을 지정 합니다.
동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. Azure. 사이트
매개 변수: Web app (ByValue)

## 출력

### Microsoft. Azure. 관리. i m m 네임 스페이스. i m m Namesslstate

## 상속자

## 관련 링크

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[제거-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


