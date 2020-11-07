---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 555409187d2d48476a731be344d0404efddc946c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875299"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.

## 구문과

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
컨텍스트가 자동으로 저장 되는지 여부와 저장 된 컨텍스트 및 자격 증명 정보를 찾을 수 있는 위치를 포함 하 여 컨텍스트 자동 저장 기능에 대 한 메타 데이터를 표시 합니다.

## 예제의

### 현재 세션에 대 한 컨텍스트 저장 메타 데이터 가져오기
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

컨텍스트의 저장 여부 및 위치에 대 한 세부 정보를 가져옵니다.  위의 예제에서는 자동 저장 기능을 사용할 수 없습니다.

### 현재 사용자의 컨텍스트 저장 메타 데이터를 가져옵니다.
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

현재 사용자에 대해 컨텍스트를 기본적으로 저장 하는 경우 및 위치에 대 한 세부 정보를 가져옵니다.  이는 현재 세션에서 활성 상태인 설정과 다를 수 있습니다. 위의 예제에서는 자동 저장 기능을 사용 하도록 설정 하 고 데이터를 기본 위치에 저장 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -범위
컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft. Azure. Common. 인증. ContextAutosaveSettings

## 상속자

## 관련 링크
