---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523408"
---
# Enable-AzureRmDataCollection

## SYNOPSIS
Azure PowerShell에서 데이터를 수집 하 여 AzurePowerShell cmdlet을 사용 하 여 사용자 환경을 향상 시킬 수 있습니다.
현재 컴퓨터의 현재 사용자에 대 한 데이터 수집에 opts cmdlet을 실행 합니다.
명시적으로 옵트인 하지 않는 한 데이터는 수집 되지 않습니다.

## 구문과

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
데이터 수집을 통해 Microsoft 클라우드 및 Azure PowerShell을 사용 하는 환경을 개선할 수 있습니다.
Azure PowerShell이 동의 하지 않고 데이터를 수집 하지 않음-AzureRmDataCollection를 실행 하 여 명시적으로 옵트인 하거나 cmdlet을 처음 실행할 때 Azure PowerShell에 데이터 수집에 대 한 메시지가 표시 되 면 예를 사용 하 여 사용자에 게 응답 합니다.
Microsoft는 일반적인 문제를 식별 하 고 Azure PowerShell을 사용 하는 환경을 개선 하기 위해 사용 패턴을 식별 하기 위해 수집 된 데이터를 집계 합니다.
Microsoft Azure PowerShell은 개인 데이터 또는 개인 식별이 가능한 정보를 수집 하지 않습니다.

현재 컴퓨터에서 현재 사용자의 데이터 수집을 사용 하도록 설정 하려면 Enable-AzureRMDataCollection cmdlet을 실행 합니다.
이렇게 하면 첫 번째 cmdlet이 실행 될 때 현재 사용자에 게 데이터 수집에 대 한 메시지가 표시 되지 않습니다.

현재 사용자에 대 한 데이터 수집을 사용 하지 않도록 설정 하려면 Disable-AzureRmDataCollection cmdlet을 실행 합니다.

## 예제의

### 예제 1: 현재 사용자의 데이터 수집 사용
```
PS C:\> Enable-AzureRmDataCollection
```

이 예제에서는 현재 사용자의 데이터 수집을 사용 하도록 설정 하는 방법을 보여 줍니다.

## 변수

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### 않아야

## 상속자

## 관련 링크

[Disable-AzureRmDataCollection]()

