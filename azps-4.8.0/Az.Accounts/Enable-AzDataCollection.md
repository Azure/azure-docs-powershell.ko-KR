---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211924"
---
# Enable-AzDataCollection

## SYNOPSIS
Azure powershell에서 데이터를 수집 하 여 Azure PowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있도록 합니다. 현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다. 명시적으로 옵트아웃 하지 않는 한 기본적으로 데이터는 수집 됩니다.

## 구문과

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은

`Enable-AzDataCollection`Cmdlet을 사용 하 여 데이터 수집을 옵트아웃 합니다. Azure PowerShell은 기본적으로 원격 분석 데이터를 자동으로 수집 합니다. Microsoft는 수집 된 데이터를 집계 하 여 사용 패턴을 식별 하 고, 일반적인 문제를 식별 하 고, Azure PowerShell의 환경을 개선 합니다.
Microsoft Azure PowerShell은 개인 또는 개인 데이터를 수집 하지 않습니다. 데이터 수집을 사용 하지 않도록 설정 하려면를 실행 하 여 명시적으로 옵트아웃 해야 합니다 `Disable-AzDataCollection` .

## 예제의

### 예제 1: 현재 사용자의 데이터 수집 사용

다음 예제에서는 현재 사용자의 데이터 수집을 사용 하도록 설정 하는 방법을 보여 줍니다.

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
