---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213765"
---
# New-AzApiManagementSslSetting

## SYNOPSIS
PsApiManagementSslSetting의 인스턴스를 만듭니다.

## 구문과

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
PsApiManagementSslSetting의 인스턴스를 만드는 도우미 명령입니다.
이 명령은 New-AzApiManagement 명령에 사용 됩니다.

## 예제의

### 예제 1: 백 엔드 및 프런트 엔드에서 모두 TLS 1.0을 사용 하도록 설정 하는 SSL 설정 만들기
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

PsApiManagementSslSetting의 새 인스턴스를 만들어 ApiManagement 게이트웨이에서 두 프런트 엔드 (클라이언트와 APIM) 및 백 엔드 (APIM 및 백 엔드 사이)에 TLSv 1.0를 설정 합니다.

## 변수

### -BackendProtocol
백 엔드 보안 프로토콜 설정 이 매개 변수는 선택 사항입니다.
유효한 프로토콜 설정은 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3.0

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
지정 된 순서의 Ssl 암호 그룹 설정 이 매개 변수는 선택 사항입니다.
유효한 설정은 `TripleDes168` Tripe Des 168에 대 한 사용 설정/해제

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

### -FrontendProtocol
프런트 엔드 보안 프로토콜 설정 이 매개 변수는 선택 사항입니다.
유효한 프로토콜 설정은 `Tls11` -tls 1.1 `Tls10` -tls 1.0 `Ssl30` -SSL 3.0


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
Http2 같은 서버 프로토콜 설정 이 매개 변수는 선택 사항입니다.
유효한 설정은 `Http2` -Enable Http 2.0입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### ApiManagement. PsApiManagementSslSettings/.

## 상속자

## 관련 링크

[새로운 AzApiManagement](./New-AzApiManagement.md)

