---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208864"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Azure 웹앱에 대한 SSL 인증서 바인딩을 만듭니다.

## 구문

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzWebAppSSLBinding** cmdlet은 Azure 웹앱에 대한 SSL(Secure Socket Layer) 인증서 바인딩을 만듭니다.
cmdlet은 다음 두 가지 방법으로 SSL 바인딩을 만듭니다. 
- 기존 인증서에 웹앱을 바인딩할 수 있습니다.
- 새 인증서를 업로드한 다음 웹앱을 이 새 인증서에 바인딩할 수 있습니다.
사용하는 방식에 관계없이 인증서와 웹앱은 동일한 Azure 리소스 그룹과 연결되어야 합니다.
리소스 그룹 A에 웹앱이 있는 경우 해당 웹앱을 리소스 그룹 B의 인증서에 바인딩하려는 경우 인증서의 복사본을 리소스 그룹 A에 업로드하는 것뿐입니다. 새 인증서를 업로드하는 경우 Azure SSL 인증서에 대한 다음 요구 사항에 유의하세요. 
- 인증서는 개인 키를 포함해야 합니다. 
- 인증서는 PFX(개인 정보 교환) 형식을 사용해야 합니다. 
- 인증서의 주체 이름은 웹앱에 액세스하는 데 사용되는 도메인과 일치해야 합니다. 
- 인증서는 최소 2048비트 암호화를 사용해야 합니다.

## 예제

### 예제 1: 웹앱에 인증서 바인딩
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

이 명령은 기존 Azure 인증서(지문 E3A38EBA60CAA1C162785A2E1C44A15AD450199C3이 있는 인증서)를 ContosoWebApp이라는 웹앱에 바인딩합니다.

### 예제 2

Azure 웹앱에 대한 SSL 인증서 바인딩을 만듭니다. (자동Generated)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETERS

### -CertificateFilePath
업로드할 인증서의 파일 경로를 지정합니다.
*CertificateFilePath* 매개 변수는 인증서가 아직 Azure에 업로드되지 않은 경우 필요합니다.

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
인증서의 암호 해독 암호를 지정합니다.

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

### -Name
웹앱의 이름을 지정합니다.

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
인증서가 할당된 리소스 그룹의 이름을 지정합니다.
동일한 명령에서 *ResourceGroupName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.

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

### -Slot
웹앱 배포 슬롯의 이름을 지정합니다.
Get-AzWebAppSlot cmdlet을 사용하여 슬롯을 얻을 수 있습니다.
배포 슬롯은 인터넷을 통해 액세스할 수 없는 웹앱을 준비하고 유효성을 검사할 수 있는 방법을 제공합니다.
일반적으로 스테이징 사이트에 변경 내용을 배포하고 해당 변경 내용의 유효성을 검사한 다음 프로덕션(인터넷 액세스 가능) 사이트에 배포합니다.

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
인증서를 사용하도록 설정하는지 여부를 지정합니다.
*SSLState* 매개 변수를 1로 설정하여 인증서를 사용하도록 설정하거나 *SSLState를* 0으로 설정하여 인증서를 사용하지 않도록 설정합니다.

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

### -Thumbprint
인증서에 대한 고유 식별자를 지정합니다.

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

### -WebApp
웹앱을 지정합니다.
웹앱을 얻습니다. Get-AzWebApp cmdlet을 사용하세요.
*ResourceGroupName* 매개 변수 및/또는 *WebAppName과* 동일한 명령에서 *WebApp* 매개 변수를 사용할 수 없습니다.

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
새 SSL 바인딩을 만들 웹앱의 이름을 지정합니다.
동일한 명령에서 *WebAppName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 출력

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## 참고 사항

## 관련 링크

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


