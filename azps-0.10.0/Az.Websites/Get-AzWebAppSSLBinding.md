---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876149"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Azure Web App 인증서 SSL 바인딩을 가져옵니다.

## 구문과

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 구성원과
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzWebAppSSLBinding** Cmdlet은 Azure Web App에 대 한 SSL (Secure Sockets layer) 바인딩을 가져옵니다.
SSL 바인딩은 웹 앱을 업로드 된 인증서와 연결 하는 데 사용 됩니다.
웹 앱은 여러 인증서에 바인딩할 수 있습니다.

## 예제의

### 예제 1: 웹 앱에 대 한 SSL 바인딩 가져오기
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

이 명령은 리소스 그룹 ContosoResourceGroup와 연결 된 웹 앱 ContosoWebApp에 대 한 SSL 바인딩을 검색 합니다.

### 예제 2: 웹 앱에 대 한 SSL 바인딩을 가져오려면 개체 참조를 사용 합니다.
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

또한이 예제의 명령은 웹 앱 ContosoWebApp SSL 바인딩도 가져옵니다. 그러나이 경우에는 웹 앱 이름 대신 개체 참조와 연결 된 리소스 그룹의 이름을 사용 합니다.
이 개체 참조는 **AzWebApp** 를 사용 하 여 ContosoWebApp 이라는 웹 앱에 대 한 개체 참조를 만드는 예제에서 첫 번째 명령에 의해 생성 됩니다.
해당 개체 참조는 $WebApp 라는 변수에 저장 됩니다.

이 변수 및 **AzWebAppSSLBinding** cmdlet은 두 번째 명령에서 SSL 바인딩을 가져오는 데 사용 됩니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
SSL 바인딩의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.

동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.

```yaml
Type: String
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
Type: String
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

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
이 cmdlet이 SSL 바인딩을 가져오는 웹 앱의 이름을 지정 합니다.

동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Site
' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

[새로운 AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[제거-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


