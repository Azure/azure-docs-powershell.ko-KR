---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: c5f68e947af383787b3ed1e7d9c9c3983c45769b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008283"
---
# Get-AzSupportTicket

## SYNOPSIS
지원 티켓을 얻습니다.

## 구문

### ListParameterSet(기본값)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 설명
지원 티켓 목록을 받습니다. 매개 변수를 지정하지 않으면 모든 지원 티켓을 검색합니다. 필터 매개 변수를 사용하여 상태 또는 CreatedDate로 지원 티켓을 필터링할 수도 있습니다. 다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.

| 시나리오                                                         | 필터                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| 열려 있는 티켓을 얻게 됩니다.                               | "상태 eq 'Open'"                               |
| 닫힌 상태의 티켓을 얻습니다.                             | "상태 eq 'Closed'"                             |
| 2019년 12월 20일 이후에 만든 티켓을 얻게 됩니다.         | "CreatedDate ge 2019-12-20"                      |
| 2019년 12월 20일 이후에 만든 티켓을 얻게 됩니다.               | "CreatedDate gt 2019-12-20"                      |
| 열려 있는 2019년 12월 20일 이후에 만든 티켓을 얻습니다. | "CreatedDate gt 2019-12-20 및 Status eq 'Open'" |


이 cmdlet은 First 및 Skip 매개 변수를 통해 파이징을 지원합니다.

티켓 이름을 지정하여 단일 지원 티켓을 검색할 수도 있습니다. 

## 예제

### 예제 1: 처음 2개 티켓을 얻다
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 2: 처음 2를 건너뛰고 나서 첫 2 티켓을 얻게 합니다.
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 3: 이름에 의해 지원 티켓을 얻게 됩니다.
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### 예제 4: 상태로 필터링된 첫 번째 2개 지원 티켓을 얻게 됩니다.
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 5: 열려 있는 상태의 모든 지원 티켓을 2019년 12월 20일 이후에 만들 수 있습니다.
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
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

### -Filter
이 cmdlet의 결과에 적용할 필터입니다.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
이 cmdlet이 얻을 지원 티켓의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
데이터 집합의 총 개체 수(정수)와 선택한 개체 수를 보고합니다.
cmdlet에서 총 수를 확인할 수 없는 경우 "알 수 없음 총 수"가 표시됩니다. 정수에는 총 개수 값의 안정성을 나타내는 정확도 속성이 있습니다.
정확도 값은 0.0에서 1.0 사이입니다. 여기서 0.0은 cmdlet이 개체를 계산할 수 없습니다. 1.0은 개수가 정확하고 0.0과 1.0 사이의 값은 점점 더 신뢰할 수 있는 예측을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
지정된 개체 수를 무시한 다음 나머지 개체를 얻습니다.
건너뛸 개체 수를 입력합니다.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
지정된 개체 수만 얻습니다.
얻을 개체 수를 입력합니다.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

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

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## 참고 사항

## 관련 링크
