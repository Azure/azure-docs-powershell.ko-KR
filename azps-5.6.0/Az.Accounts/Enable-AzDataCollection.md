---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999040"
---
# Enable-AzDataCollection

## SYNOPSIS
Azure PowerShell을 사용하여 데이터를 수집하여 Azure PowerShell cmdlet을 사용하여 사용자 환경을 개선할 수 있습니다. 이 cmdlet을 실행하면 현재 컴퓨터의 현재 사용자의 데이터 수집에 옵트인됩니다. 명시적으로 옵트아웃하지 않는 한 데이터는 기본적으로 수집됩니다.

## 구문

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명

`Enable-AzDataCollection`cmdlet은 데이터 수집을 옵트인하는 데 사용됩니다. Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집합니다. Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell의 환경을 개선합니다.
Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집하지 않습니다. 데이터 수집을 사용하지 않도록 설정하려면 을 실행하여 명시적으로 옵트아웃해야 `Disable-AzDataCollection` 합니다.

## 예제

### 예제 1: 현재 사용자에 대한 데이터 수집 사용

다음 예제에서는 현재 사용자에 대한 데이터 수집을 사용하도록 설정하는 방법을 보여줍니다.

```powershell
Enable-AzDataCollection
```

## 매개 변수

### -DefaultProfile

Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -확인

cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### 없음

## 출력

### System.Void

## 참고 사항

## 관련 링크

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
