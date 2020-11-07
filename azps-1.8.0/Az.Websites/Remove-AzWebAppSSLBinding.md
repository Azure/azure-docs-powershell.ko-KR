---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: fda088ff8e8b3942ca6dbf94605b3887e3f6884b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698318"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
업로드 된 인증서에서 SSL 바인딩을 제거 합니다.

## 구문과

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### 구성원과
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzWebAppSSLBinding** Cmdlet은 Azure 웹 앱에서 SSL (Secure Sockets layer) 바인딩을 제거 합니다.
SSL 바인딩은 웹 앱을 인증서와 연결 하는 데 사용 됩니다.

## 예제의

### 예제 1: 웹 앱에 대 한 SSL 바인딩 제거
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

이 명령은 웹 앱 ContosoWebApp에 대 한 SSL 바인딩을 제거 합니다.
*DeleteCertificate* 매개 변수가 포함 되지 않기 때문에 더 이상 SSL 바인딩이 없는 경우 인증서가 삭제 됩니다.

### 예제 2: 인증서를 제거 하지 않고 SSL 바인딩 제거
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

예제 1과 유사 하 게,이 명령은 웹 앱 ContosoWebApp SSL 바인딩도 제거 합니다.
그러나이 경우 *DeleteCertificate* 매개 변수가 포함 되며 매개 변수 값이 $False 설정 됩니다.
이는 SSL 바인딩이 있는지 여부에 관계 없이 인증서가 삭제 되지 않는다는 의미입니다.

### 예제 3: 개체 참조를 사용 하 여 SSL 바인딩 제거
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

이 예제에서는 웹 앱 웹 사이트에 대 한 개체 참조를 사용 하 여 웹 앱에 대 한 SSL 바인딩을 제거 합니다.
첫 번째 명령은 Get-AzWebApp cmdlet을 사용 하 여 ContosoWebApp 이라는 웹 앱에 대 한 개체 참조를 만듭니다.
해당 개체 참조는 $WebApp 라는 변수에 저장 됩니다.
두 번째 명령은 개체 참조와 **remove-AzWebAppSSLBinding** cmdlet을 사용 하 여 SSL 바인딩을 제거 합니다.

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

### -DeleteCertificate
제거할 SSL 바인딩이 인증서에 사용 되는 유일한 바인딩만 하는 경우 수행할 작업을 지정 합니다.
*DeleteCertificate* 가 $False으로 설정 되 면 바인딩이 삭제 될 때 인증서가 삭제 되지 않습니다.
*DeleteCertificate* 가 $True으로 설정 되거나 명령에 포함 되어 있지 않으면 SSL 바인딩과 함께 인증서가 삭제 됩니다.
제거 하려는 SSL 바인딩이 인증서에 사용 되는 유일한 바인딩만 있는 경우에만 인증서가 삭제 됩니다.
인증서에 둘 이상의 바인딩이 있는 경우 *DeleteCertificate* 매개 변수의 값에 관계 없이 인증서가 제거 되지 않습니다.

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
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -슬롯
웹 앱 배포 슬롯을 지정 합니다.
배포 슬롯을 얻으려면 Get-AzWebAppSlot cmdlet을 사용 합니다.

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

### -Web app
웹 앱을 지정 합니다.
웹 앱을 가져오려면 Get-AzWebApp cmdlet을 사용 합니다.
*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.

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
웹 앱의 이름을 지정 합니다.
동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft Azure. *. m a i m Apps.

## 출력

### 시스템. i a o

## 상속자

## 관련 링크

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[새로운 AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


