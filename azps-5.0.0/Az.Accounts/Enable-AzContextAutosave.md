---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218266"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure 컨텍스트는 명령을 실행할 활성 구독을 나타내는 PowerShell 개체와 Azure 클라우드에 연결 하는 데 필요한 인증 정보입니다. Azure 컨텍스트를 사용 하는 경우 Azure PowerShell에서는 구독을 전환할 때마다 계정을 다시 인증 하지 않아도 됩니다. 자세한 내용은 [Azure PowerShell 컨텍스트 개체](https://docs.microsoft.com/powershell/azure/context-persistence)를 참조 하세요.

이 cmdlet을 사용 하면 PowerShell 프로세스를 시작할 때 Azure 컨텍스트 정보가 저장 되 고 자동으로 로드 됩니다. 예를 들어 새 창을 열 때

## 구문과

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은

Azure 컨텍스트 정보를 저장 하 고 PowerShell 프로세스가 시작 될 때 자동으로 로드 되도록 합니다. 컨텍스트는 컨텍스트에 영향을 주는 cmdlet 실행의 끝에 저장 됩니다. 예를 들어 모든 프로필 cmdlet을 사용할 경우 사용자 인증을 사용 하는 경우 cmdlet을 실행 하는 동안 토큰을 업데이트할 수 있습니다.

## 예제의

### 예제 1: 현재 사용자에 대해 autosaving 자격 증명 사용

현재 사용자에 대 한 자격 증명 자동 저장을 설정 합니다. PowerShell 창을 열 때마다 로그인 하지 않고 현재 컨텍스트가 기억 됩니다.

```powershell
Enable-AzContextAutosave
```

### 예제 2

이 PowerShell 세션에서 PowerShell 창을 열 때 Azure 자격 증명, 계정 및 구독 정보를 저장 하 고 자동으로 로드 하도록 허용 합니다. 생성

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## 변수

### -DefaultProfile

Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독

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

컨텍스트 변경의 범위를 결정 합니다. 예를 들어 변경 내용이 현재 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 되는지 여부 범위를 변경 하면 `CurrentUser` 사용자가 시작한 모든 PowerShell 세션에 영향을 줍니다. 특정 세션에 다른 설정이 필요한 경우 범위를 사용 `Process` 합니다.

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

Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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

Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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

### 공통 매개 변수

이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft. Azure. Common. 인증. ContextAutosaveSettings

## 상속자

## 관련 링크
