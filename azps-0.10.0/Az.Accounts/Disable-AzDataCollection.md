---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875309"
---
# Disable-AzDataCollection

## SYNOPSIS
Opts에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 개선 했습니다. 명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

## 구문과

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
데이터 수집을 통해 Microsoft 클라우드 및 Azure PowerShell을 사용 하는 환경을 개선할 수 있습니다.
Azure PowerShell이 동의 하지 않고 데이터를 수집 하지 않음-AzDataCollection를 실행 하 여 명시적으로 옵트인 하거나 cmdlet을 처음 실행할 때 Azure PowerShell에 데이터 수집에 대 한 메시지가 표시 되 면 예를 사용 하 여 사용자에 게 응답 합니다.
Microsoft는 일반적인 문제를 식별 하 고 Azure PowerShell을 사용 하는 환경을 개선 하기 위해 사용 패턴을 식별 하기 위해 수집 된 데이터를 집계 합니다.
Microsoft Azure PowerShell은 개인 데이터 또는 개인 식별이 가능한 정보를 수집 하지 않습니다.
Disable-AzDataCollection cmdlet을 실행 하 여 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 합니다.
이렇게 하면 첫 번째 cmdlet이 실행 될 때 현재 사용자에 게 데이터 수집에 대 한 메시지가 표시 되지 않습니다.
현재 사용자에 대해 데이터 수집을 사용 하도록 설정 하려면 Enable-AzDataCollection cmdlet을 실행 합니다.

## 예제의

### 예제 1: 현재 사용자에 대해 데이터 수집을 사용 하지 않도록 설정
```
PS C:\> Disable-AzDataCollection
```

이 예제에서는 현재 사용자의 데이터 수집을 사용 하지 않도록 설정 하는 방법을 보여 줍니다. 

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### 시스템. i a o

## 상속자

## 관련 링크

[Enable-AzDataCollection](./Enable-AzDataCollection.md)

