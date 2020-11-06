---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525803"
---
# Get-AzureRmApiManagementOpenIdConnectProvider

## SYNOPSIS
OpenID 연결 공급자를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 모든 OpenID 연결 공급자 가져오기 (기본값)
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Get by OpenID 연결 공급자 ID
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### OpenID에서 찾기 공급자 이름 연결
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 가져옵니다.

## 예제의

### 예제 1: 모든 공급자 가져오기
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

이 명령은 지정 된 컨텍스트에 대 한 모든 OpenID Connect 공급자를 가져옵니다.

### 예제 2: ID를 사용 하 여 공급자 가져오기
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

이 명령은 ID OICProvicer01 인 공급자를 가져옵니다.

### 예제 3: 이름을 사용 하 여 공급자 가져오기
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

이 명령은 Contoso OpenID Connect Provider 라는 공급자를 가져옵니다.

## 변수

### -컨텍스트
**PsApiManagementContext** 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
공급자의 이름을 지정 합니다.
이름을 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OpenIdConnectProviderId
이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.
ID를 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### IList를<ApiManagement> ServiceManagement. PsApiManagementOpenIdConnectProvider

## 상속자

## 관련 링크

[새로운 AzureRmApiManagementOpenIdConnectProvider](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[제거-AzureRmApiManagementOpenIdConnectProvider](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[Set-AzureRmApiManagementOpenIdConnectProvider](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


