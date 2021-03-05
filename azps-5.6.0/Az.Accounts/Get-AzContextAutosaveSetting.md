---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981344"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
컨텍스트가 자동으로 저장되는지 여부 및 저장된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함하여 컨텍스트 자동 저장 기능에 대한 메타데이터를 표시합니다.

## 구문

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
컨텍스트가 자동으로 저장되는지 여부 및 저장된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함하여 컨텍스트 자동 저장 기능에 대한 메타데이터를 표시합니다.

## 예제

### 현재 세션에 대한 컨텍스트 저장 메타데이터를 얻습니다.
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

컨텍스트가 저장되는지 여부와 위치를 자세히 알 수 있습니다.  위의 예제에서는 자동 도청 기능을 사용하지 않도록 설정했습니다.

### 현재 사용자의 컨텍스트 저장 메타데이터를 얻게 됩니다.
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

컨텍스트가 현재 사용자에 대해 기본적으로 저장되는지 여부와 위치를 자세히 알 수 있습니다.  이 설정은 현재 세션에서 활성 상태인 설정과 다를 수 있습니다. 위의 예제에서는 자동 저장 기능을 사용하도록 설정하고 데이터를 기본 위치에 저장합니다.

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

### -Scope
컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

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

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## 참고 사항

## 관련 링크
