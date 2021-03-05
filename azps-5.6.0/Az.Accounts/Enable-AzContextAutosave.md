---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999054"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure 컨텍스트는 Azure 클라우드에 연결하는 데 필요한 인증 정보를 실행하기 위해 활성 구독을 나타내는 PowerShell 개체입니다. Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 등록할 필요가 없습니다. 자세한 내용은 [Azure PowerShell 컨텍스트 개체 를 참조하세요.](https://docs.microsoft.com/powershell/azure/context-persistence)

이 cmdlet을 사용하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다. 예를 들어 새 창을 여는 경우입니다.

## 구문

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명

PowerShell 프로세스가 시작될 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다. 컨텍스트는 컨텍스트에 영향을 주는 모든 cmdlet의 실행 끝에 저장됩니다. 예를 들어 모든 프로필 cmdlet입니다. 사용자 인증을 사용하는 경우 cmdlet을 실행하는 동안 토큰을 업데이트할 수 있습니다.

## 예제

### 예제 1: 현재 사용자에 대한 자동 저장 자격 증명 사용

현재 사용자의 자격 증명 자동 저장을 설정합니다. PowerShell 창이 열리면 로그인하지 않고 현재 컨텍스트가 기억됩니다.

```powershell
Enable-AzContextAutosave
```

### 예제 2

이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장하고 자동으로 로드할 수 있습니다. (자동 재생)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## 매개 변수

### -DefaultProfile

Azure와 통신하는 데 사용되는 자격 증명, 테넌트 및 구독

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

컨텍스트 변경의 범위를 결정합니다. 예를 들어 변경 내용이 현재 프로세스에만 적용되는지 아니면 이 사용자가 시작한 모든 세션에 적용하는지 여부입니다. 범위가 변경된 경우 사용자가 시작한 `CurrentUser` 모든 PowerShell 세션에 영향을 미치게 됩니다. 특정 세션에 다른 설정이 필요한 경우 범위 `Process` 를 사용합니다.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인

cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
