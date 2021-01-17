---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 393b811ec7bc2d7a3ddafda3a33b5460e4bef6dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327816"
---
# Disable-AzContextAutosave

## SYNOPSIS
Azure 자격 증명 자동 저장을 해제합니다.  다음에 PowerShell 창을 열면 로그인 정보가 잊혀지기

## 구문

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
Azure 자격 증명 자동 저장을 해제합니다.  다음에 PowerShell 창을 열면 로그인 정보가 잊혀지기

## 예제

### 예제 1: 컨텍스트 자동 조정 사용 안
```powershell
PS C:\> Disable-AzContextAutosave
```

현재 사용자에 대해 자동저장 기능을 사용하지 않도록 설정합니다.

### 예제 2

이 PowerShell 세션에서 Azure 자격 증명 자동 저장을 해제합니다. (자동Generated)

```powershell <!-- Aladdin Generated Example --> 
Disable-AzContextAutosave -Scope Process
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
변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부와 같은 컨텍스트 변경의 범위를 결정

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## 참고 사항

## 관련 링크
