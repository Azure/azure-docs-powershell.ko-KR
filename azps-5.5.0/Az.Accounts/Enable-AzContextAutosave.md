---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195444"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure 컨텍스트는 명령을 실행할 활성 구독을 나타내는 PowerShell 개체 및 Azure 클라우드에 연결하는 데 필요한 인증 정보입니다. Azure 컨텍스트를 사용하면 구독을 전환할 때마다 Azure PowerShell에서 계정을 다시 등록할 필요가 없습니다. 자세한 내용은 [Azure PowerShell 컨텍스트 개체를 참조하세요.](https://docs.microsoft.com/powershell/azure/context-persistence)

이 cmdlet을 사용하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다. 예를 들어 새 창을 열 때입니다.

## 구문

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명

PowerShell 프로세스가 시작될 때 Azure 컨텍스트 정보를 저장하고 자동으로 로드할 수 있습니다. 컨텍스트는 컨텍스트에 영향을 주는 모든 cmdlet의 실행 끝에 저장됩니다. 예를 들어 모든 프로필 cmdlet입니다. 사용자 인증을 사용하는 경우 cmdlet을 실행하는 동안 토큰을 업데이트할 수 있습니다.

## 예제

### 예제 1: 현재 사용자에 대한 자격 증명 자동 저장 사용

현재 사용자에 대한 자격 증명 자동 저장을 켜야 합니다. PowerShell 창이 열리면 현재 컨텍스트가 로그인하지 않고 기억됩니다.

```powershell
Enable-AzContextAutosave
```

### 예제 2

이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장하고 자동으로 로드하도록 허용합니다. (자동Generated)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETERS

### -DefaultProfile

Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독

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

컨텍스트 변경의 범위를 지정합니다. 예를 들어 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용될지 여부입니다. 범위를 변경하면 사용자가 시작한 모든 `CurrentUser` PowerShell 세션에 영향을 미치게 됩니다. 특정 세션에 다른 설정이 필요한 경우 범위를 `Process` 사용합니다.

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

### -Confirm

cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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

cmdlet이 실행되는 경우의 결과 표시
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

### 일반 매개 변수

이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## 참고 사항

## 관련 링크
