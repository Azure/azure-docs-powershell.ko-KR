---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218275"
---
# Disable-AzDataCollection

## SYNOPSIS
Azure PowerShell cmdlet을 개선 하기 위해 데이터를 수집 하는 Opts. 명시적으로 옵트아웃 하지 않는 한 기본적으로 데이터는 수집 됩니다.

## 구문과

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은

`Disable-AzDataCollection`Cmdlet은 데이터 수집을 옵트아웃 하는 데 사용 됩니다. Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집 합니다. 데이터 수집을 사용 하지 않도록 설정 하려면 명시적으로 옵트아웃 해야 합니다. Microsoft는 수집 된 데이터를 집계 하 여 사용 패턴을 식별 하 고, 일반적인 문제를 식별 하 고, Azure PowerShell의 환경을 개선 합니다. Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집 하지 않습니다. 이전에 옵트아웃 한 경우 cmdlet을 실행 `Enable-AzDataCollection` 하 여 현재 컴퓨터의 현재 사용자에 대 한 데이터 수집을 다시 사용 하도록 설정 합니다.

## 예제의

### 예제 1: 현재 사용자에 대해 데이터 수집을 사용 하지 않도록 설정

다음 예제에서는 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 하는 방법을 보여 줍니다.

```powershell
Disable-AzDataCollection
```

## 변수

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

### -확인

Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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

Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.

## 입력

### 않아야

## 출력

### 시스템. i a o

## 상속자

## 관련 링크

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
