---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878393"
---
# Get-AzSupportTicketCommunication

## SYNOPSIS
지원 티켓 통신을 받습니다.

## 구문과

### GetByNameParameterSet (기본값)
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### GetByParentObjectParameterSet
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## 설명은
지원 티켓에 대 한 통신을 가져옵니다. 다른 매개 변수를 지정 하지 않으면 티켓에 대 한 모든 통신을 검색 하 게 됩니다. Filter 매개 변수를 사용 하 여 CreatedDate 또는 CommunicationType 통신을 필터링 할 수도 있습니다. 다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.


| 시나리오                                                        | 분류                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| 웹 통신 받기                                          | "CommunicationType eq ' Web '"                               |
| 전화 통신 받기                                        | "CommunicationType eq ' 휴대폰 '"                             |
| 2019 년 12 월 20th 일 이후에 만들어진 통신을 다운로드 합니다. | "CreatedDate ge 2019-12-20"                                |
| 2019 년 12 월 20th 일 이후에 만든 커뮤니케이션 받기       | "CreatedDate gt 2019-12-20"                                |
| 2019 년 12 월 20th 일 이후에 만들어진 웹 통신을 가져옵니다.            | "CreatedDate gt 2019-12-20 및 CommunicationType eq ' 웹 '" |


이 cmdlet은 First 및 Skip 매개 변수를 통해 페이징을 지원 합니다.

통신 이름을 지정 하 여 단일 지원 티켓 통신을 검색할 수도 있습니다. 

## 예제의

### 예제 1: 지원 티켓에 대 한 모든 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### 예제 2: 지원 티켓의 이름으로 단일 통신을 검색 합니다.
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### 예제 3: 지원 티켓에 대 한 처음 2 개의 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 4: 지원 티켓에 대 한 처음 2 개의 통신을 건너뛴 후 다음 2 개의 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### 예제 5: 지원 티켓에 대 한 모든 웹 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 6: 지원 티켓에 대해 2019 년 12 월 20th 일에 만들어진 모든 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 7: 지원 티켓에 대해 2019 년 12 월 20th 일에 만든 모든 웹 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 8: 지원 티켓에 대 한 모든 통신을 파이핑 지원 티켓 개체를 통해 검색
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
통신 이름.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
티켓 이름을 지원 합니다.

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

### -SupportTicketObject
티켓 개체를 지원 합니다.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft. PSSupportTicket을 통해 지원 되는 모델

## 출력

### PSSupportTicketCommunication를 지원 합니다.

## 상속자

## 관련 링크
