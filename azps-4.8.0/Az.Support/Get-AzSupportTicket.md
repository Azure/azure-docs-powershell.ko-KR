---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204699"
---
# Get-AzSupportTicket

## SYNOPSIS
지원 티켓 받기

## 구문과

### ListParameterSet (기본값)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 설명은
지원 티켓 목록을 가져옵니다. 매개 변수를 지정 하지 않으면 모든 지원 티켓이 검색 됩니다. Filter 매개 변수를 사용 하 여 상태 또는 CreatedDate 지원 티켓을 필터링 할 수도 있습니다. 다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.

| 시나리오                                                         | 분류                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| 열린 상태인 티켓 가져오기                               | "상태 eq ' 열림 '"                               |
| 닫힌 상태의 티켓 가져오기                             | "상태 eq ' 닫힘"                             |
| 2019 년 12 월 20th 일 이후에 만들어진 티켓을 가져옵니다.         | "CreatedDate ge 2019-12-20"                      |
| 2019 년 12 월 20th 일 이후에 만들어진 티켓 가져오기               | "CreatedDate gt 2019-12-20"                      |
| 열림 상태인 2019 년 12 월 20th 이후 생성 된 티켓을 가져옵니다. | "CreatedDate gt 2019-12-20 및 상태 eq ' Open '" |


이 cmdlet은 First 및 Skip 매개 변수를 통해 페이징을 지원 합니다.

티켓 이름을 지정 하 여 단일 지원 티켓을 검색할 수도 있습니다. 

## 예제의

### 예제 1: 첫 2 개의 티켓 가져오기
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 2: 첫 2 티켓을 건너뛴 후 처음 2 개의 티켓 가져오기
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 3: 이름으로 지원 티켓 가져오기
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### 예제 4: 상태별로 필터링 된 처음 2 개의 지원 티켓 가져오기
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### 예제 5: 열려 있는 상태의 모든 지원 티켓을 가져오고 Dec 20th 이후 만든 2019
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
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

### -필터
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

### -이름
이 cmdlet이 가져오는 지원 티켓의 이름입니다.

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
데이터 집합 (정수)에 있는 개체의 총 수와 선택한 개체를 보고 합니다.
Cmdlet에서 총 개수를 확인할 수 없는 경우 "알 수 없는 총 개수"가 표시 됩니다. Integer에는 총 count 값의 안정성을 나타내는 정확도 속성이 있습니다.
정확도 값의 범위는 0.0에서 0.0 1.0는 cmdlet이 개체 수를 계산할 수 없음을 의미 하 고, 1.0에서는 카운트가 정확한 지를 의미 하며, 0.0 및 1.0 간의 값이 점차 안정적인 추정치를 나타냅니다.

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

### -생략
지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.
건너뛸 개체 수를 입력 합니다.

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

### -첫 번째
지정 된 수의 개체만 가져옵니다.
가져올 개체 수를 입력 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft. PSSupportTicket을 통해 지원 되는 모델

## 상속자

## 관련 링크
