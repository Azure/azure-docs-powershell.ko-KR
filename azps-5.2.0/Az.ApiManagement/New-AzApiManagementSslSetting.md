---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356013"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
PsApiManagementSslSetting의 인스턴스를 만듭니다.

## 구문

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.
이 명령은 New-AzApiManagement 사용할 수 있습니다.

## 예제

### 예제 1: 백 엔드 및 프런트 엔드 모두에서 TLS 1.0을 사용하도록 설정하는 SSL 설정 만들기
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

PsApiManagementSslSetting의 새 인스턴스를 만들어 ApiManagement 게이트웨이의 프런트 엔드(클라이언트와 APIM 간) 및 백 엔드(APIM과 백 엔드 간)에서 TLSv 1.0을 사용하도록 설정합니다.

## PARAMETERS

### -BackendProtocol
백end 보안 프로토콜 설정입니다. 이 매개 변수는 선택 사항입니다.
유효한 프로토콜 설정은 `Tls11` Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
Ssl 암호 모음 설정은 지정된 순서로 설정됩니다. 이 매개 변수는 선택 사항입니다.
유효한 `TripleDes168` 설정은 - Tripe Des 168 사용/사용 안 하도록 설정

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -FrontendProtocol
프런트 엔드 보안 프로토콜 설정입니다. 이 매개 변수는 선택 사항입니다.
유효한 프로토콜 설정은 `Tls11` Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0입니다.


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
Http2와 같은 서버 프로토콜 설정입니다. 이 매개 변수는 선택 사항입니다.
유효한 설정은 `Http2` Http 2.0 사용입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings

## 참고 사항

## 관련 링크

[New-AzApiManagement](./New-AzApiManagement.md)

