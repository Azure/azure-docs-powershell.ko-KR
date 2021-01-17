---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491143"
---
# Get-AzSupportTicketCommunication

## SYNOPSIS
지원 티켓 통신을 받을 수 있습니다.

## 구문

### GetByNameParameterSet(기본값)
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

## 설명
지원 티켓에 대한 통신을 얻습니다. 다른 매개 변수를 지정하지 않으면 티켓에 대한 모든 통신을 검색합니다. Filter 매개 변수를 사용하여 CreatedDate 또는 CommunicationType을 통해 통신을 필터링할 수도 있습니다. 다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.


| 시나리오                                                        | 필터                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| 웹 통신을 얻습니다.                                          | "CommunicationType eq 'Web'"                               |
| 전화 통신을 받을 수 있습니다.                                        | "CommunicationType eq 'Phone'"                             |
| 2019년 12월 20일 이후에 생성된 통신을 얻습니다. | "CreatedDate ge 2019-12-20"                                |
| 2019년 12월 20일 이후에 생성된 통신을 얻습니다.       | "CreatedDate gt 2019-12-20"                                |
| 2019년 12월 20일 이후에 생성된 웹 통신을 얻습니다.            | "CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'" |


이 cmdlet은 First 및 Skip 매개 변수를 통한 파이징을 지원합니다.

통신 이름을 지정하여 단일 지원 티켓 통신을 검색할 수도 있습니다. 

## 예제

### 예제 1: 지원 티켓에 대한 모든 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### 예제 2: 지원 티켓의 이름으로 단일 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### 예제 3: 지원 티켓에 대한 처음 2개 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 4: 지원 티켓에 대한 처음 2개 통신을 건너뛰고 다음 2개 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### 예제 5: 지원 티켓에 대한 모든 웹 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 6: 지원 티켓에 대해 2019년 12월 20일 이후에 생성된 모든 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 7: 지원 티켓에 대해 2019년 12월 20일 이후에 생성된 모든 웹 통신 검색
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### 예제 8: 지원 티켓 개체를 파이핑하여 지원 티켓에 대한 모든 통신 검색
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
통신 이름입니다.

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
지원 티켓 이름입니다.

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
지원 티켓 개체입니다.

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
선택한 개체 다음에 데이터 집합(정수)의 총 개체 수를 보고합니다.
cmdlet에서 총 수를 확인할 수 없는 경우 "알 수 없는 총 수"가 표시됩니다. 정수에는 총 개수 값의 안정성을 나타내는 정확도 속성이 있습니다.
정확도의 값은 0.0에서 1.0 사이입니다. 여기서 0.0은 cmdlet이 개체 수를 계산할 수 없습니다. 1.0은 개수가 정확하다는 의미입니다. 0.0과 1.0 사이의 값은 점점 더 신뢰할 수 있는 추정값을 나타냅니다.

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
지정된 개체 수를 무시하고 나머지 개체를 얻습니다.
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
지정된 수의 개체만 얻습니다.
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## 출력

### Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication

## 참고 사항

## 관련 링크
