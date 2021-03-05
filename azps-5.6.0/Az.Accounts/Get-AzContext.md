---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: 2060a1cbe9f002a20b94e82ac9547c5fc96c0e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010128"
---
# Get-AzContext

## SYNOPSIS
Azure Resource Manager 요청을 인증하는 데 사용되는 메타데이터를 얻습니다.

## 구문

### GetSingleContext(기본값)
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### ListAllContexts
```
Get-AzContext [-ListAvailable] [-RefreshContextFromTokenCache] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
Get-AzContext cmdlet은 Azure Resource Manager 요청을 인증하는 데 사용되는 현재 메타데이터를 얻습니다.
이 cmdlet은 Active Directory 계정, Active Directory 테넌트, Azure 구독 및 대상 Azure 환경을 제공합니다.
Azure Resource Manager cmdlet은 Azure Resource Manager 요청을 만들 때 기본적으로 이러한 설정을 사용합니다.

## 예제

### 예제 1: 현재 컨텍스트를
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

이 예제에서는 Connect-AzAccount를 사용하여 Azure 구독으로 계정에 로그인한 다음 Get-AzContext를 호출하여 현재 세션의 컨텍스트를 얻습니다.

### 예제 2: 사용 가능한 모든 컨텍스트 나열
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

이 예제에서는 현재 사용 가능한 모든 컨텍스트가 표시됩니다.  사용자는 Select-AzContext를 사용하여 이러한 컨텍스트 중 하나를 선택할 수 있습니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -ListAvailable
현재 세션에서 사용 가능한 모든 컨텍스트를 나열합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
컨텍스트의 이름

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshContextFromTokenCache
토큰 캐시에서 컨텍스트 새로 고침

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext

## 참고 사항

## 관련 링크

[Set-AzContext](./Set-AzContext.md)

