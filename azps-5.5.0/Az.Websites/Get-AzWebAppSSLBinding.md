---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207488"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Azure 웹앱 인증서 SSL 바인딩을 얻습니다.

## 구문

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
**Get-AzWebAppSSLBinding** cmdlet은 Azure 웹앱에 Secure Sockets Layer(SSL) 바인딩을 얻습니다.
SSL 바인딩은 웹앱을 업로드된 인증서와 연결하는 데 사용됩니다.
Web Apps는 여러 인증서에 바인딩될 수 있습니다.

## 예제

### 예제 1: 웹앱에 대한 SSL 바인딩을 얻습니다.
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

이 명령은 리소스 그룹 ContosoResourceGroup과 연결된 웹앱 ContosoWebApp에 대한 SSL 바인딩을 검색합니다.

### 예제 2: 개체 참조를 사용하여 웹앱에 대한 SSL 바인딩을 얻습니다.
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

이 예제의 명령은 웹앱 ContosoWebApp에 대한 SSL 바인딩도 얻습니다. 그러나 이 경우 웹앱 이름 및 연결된 리소스 그룹의 이름 대신 개체 참조가 사용됩니다.
이 개체 참조는 **Get-AzWebApp을** 사용하여 ContosoWebApp이라는 웹앱에 대한 개체 참조를 만드는 예제의 첫 번째 명령에 의해 생성됩니다.
해당 개체 참조는 $WebApp.
이 변수 및 **Get-AzWebAppSSLBinding** cmdlet은 두 번째 명령에서 SSL 바인딩을 얻습니다.

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

### -Name
SSL 바인딩의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
이 cmdlet이 SSL 바인딩을 받을 웹앱의 이름을 지정합니다.
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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## 출력

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## 참고 사항

## 관련 링크

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


