---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208845"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
업로드된 인증서에서 SSL 바인딩을 제거합니다.

## 구문

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzWebAppSSLBinding** cmdlet은 Azure 웹앱에서 Secure Sockets Layer(SSL) 바인딩을 제거합니다.
SSL 바인딩은 웹앱을 인증서와 연결하는 데 사용됩니다.

## 예제

### 예제 1: 웹앱에 대한 SSL 바인딩 제거
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

이 명령은 웹앱 ContosoWebApp에 대한 SSL 바인딩을 제거합니다.
*DeleteCertificate* 매개 변수가 포함되지 않은 경우 더 이상 SSL 바인딩이 없는 경우 인증서가 삭제됩니다.

### 예제 2: 인증서를 제거하지 않고 SSL 바인딩 제거
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

예제 1과 마찬가지로 이 명령은 웹앱 ContosoWebApp에 대한 SSL 바인딩도 제거합니다.
그러나 이 경우 *DeleteCertificate* 매개 변수가 포함되고 매개 변수 값이 $False.
즉, SSL 바인딩이 있는지 여부에 관계없이 인증서가 삭제되지 않습니다.

### 예제 3: 개체 참조를 사용하여 SSL 바인딩 제거
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

이 예제에서는 웹앱 웹 사이트에 대한 개체 참조를 사용하여 웹앱에 대한 SSL 바인딩을 제거합니다.
첫 번째 명령은 Get-AzWebApp cmdlet을 사용하여 ContosoWebApp이라는 웹앱에 대한 개체 참조를 만듭니다.
해당 개체 참조는 $WebApp.
두 번째 명령은 개체 참조 및 **Remove-AzWebAppSSLBinding** cmdlet을 사용하여 SSL 바인딩을 제거합니다.

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

### -DeleteCertificate
제거되는 SSL 바인딩이 인증서에서 사용되는 유일한 바인딩인 경우 수행되는 작업을 지정합니다.
*DeleteCertificate를* $False 바인딩이 삭제될 때 인증서가 삭제되지 않습니다.
*DeleteCertificate를* $True 명령에 포함되지 않은 경우 인증서가 SSL 바인딩과 함께 삭제됩니다.
제거되는 SSL 바인딩이 인증서에서 사용되는 유일한 바인딩인 경우 인증서가 삭제됩니다.
인증서에 두 개 이상의 바인딩이 있는 경우 *DeleteCertificate* 매개 변수의 값에 관계없이 인증서가 제거되지 않습니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
웹앱 배포 슬롯을 지정합니다.
배포 슬롯을 얻습니다. Get-AzWebAppSlot cmdlet을 사용 합니다.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
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
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
웹앱의 이름을 지정합니다.
동일한 명령에서 *WebAppName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


