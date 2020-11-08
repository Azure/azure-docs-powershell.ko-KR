---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213172"
---
# <span data-ttu-id="3960c-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="3960c-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="3960c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3960c-102">SYNOPSIS</span></span>
<span data-ttu-id="3960c-103">지원 티켓 통신을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-103">Get support ticket communications.</span></span>

## <span data-ttu-id="3960c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3960c-104">SYNTAX</span></span>

### <span data-ttu-id="3960c-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3960c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="3960c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3960c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="3960c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3960c-107">DESCRIPTION</span></span>
<span data-ttu-id="3960c-108">지원 티켓에 대 한 통신을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="3960c-109">다른 매개 변수를 지정 하지 않으면 티켓에 대 한 모든 통신을 검색 하 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="3960c-110">Filter 매개 변수를 사용 하 여 CreatedDate 또는 CommunicationType 통신을 필터링 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="3960c-111">다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="3960c-112">시나리오</span><span class="sxs-lookup"><span data-stu-id="3960c-112">Scenario</span></span>                                                        | <span data-ttu-id="3960c-113">분류</span><span class="sxs-lookup"><span data-stu-id="3960c-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3960c-114">웹 통신 받기</span><span class="sxs-lookup"><span data-stu-id="3960c-114">Get Web communications</span></span>                                          | <span data-ttu-id="3960c-115">"CommunicationType eq ' Web '"</span><span class="sxs-lookup"><span data-stu-id="3960c-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="3960c-116">전화 통신 받기</span><span class="sxs-lookup"><span data-stu-id="3960c-116">Get Phone communications</span></span>                                        | <span data-ttu-id="3960c-117">"CommunicationType eq ' 휴대폰 '"</span><span class="sxs-lookup"><span data-stu-id="3960c-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="3960c-118">2019 년 12 월 20th 일 이후에 만들어진 통신을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="3960c-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="3960c-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="3960c-120">2019 년 12 월 20th 일 이후에 만든 커뮤니케이션 받기</span><span class="sxs-lookup"><span data-stu-id="3960c-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="3960c-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="3960c-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="3960c-122">2019 년 12 월 20th 일 이후에 만들어진 웹 통신을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="3960c-123">"CreatedDate gt 2019-12-20 및 CommunicationType eq ' 웹 '"</span><span class="sxs-lookup"><span data-stu-id="3960c-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="3960c-124">이 cmdlet은 First 및 Skip 매개 변수를 통해 페이징을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="3960c-125">통신 이름을 지정 하 여 단일 지원 티켓 통신을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="3960c-126">예제의</span><span class="sxs-lookup"><span data-stu-id="3960c-126">EXAMPLES</span></span>

### <span data-ttu-id="3960c-127">예제 1: 지원 티켓에 대 한 모든 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="3960c-128">예제 2: 지원 티켓의 이름으로 단일 통신을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="3960c-129">예제 3: 지원 티켓에 대 한 처음 2 개의 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="3960c-130">예제 4: 지원 티켓에 대 한 처음 2 개의 통신을 건너뛴 후 다음 2 개의 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="3960c-131">예제 5: 지원 티켓에 대 한 모든 웹 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="3960c-132">예제 6: 지원 티켓에 대해 2019 년 12 월 20th 일에 만들어진 모든 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="3960c-133">예제 7: 지원 티켓에 대해 2019 년 12 월 20th 일에 만든 모든 웹 통신 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="3960c-134">예제 8: 지원 티켓에 대 한 모든 통신을 파이핑 지원 티켓 개체를 통해 검색</span><span class="sxs-lookup"><span data-stu-id="3960c-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="3960c-135">변수</span><span class="sxs-lookup"><span data-stu-id="3960c-135">PARAMETERS</span></span>

### <span data-ttu-id="3960c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3960c-136">-DefaultProfile</span></span>
<span data-ttu-id="3960c-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3960c-138">-필터</span><span class="sxs-lookup"><span data-stu-id="3960c-138">-Filter</span></span>
<span data-ttu-id="3960c-139">이 cmdlet의 결과에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="3960c-140">-이름</span><span class="sxs-lookup"><span data-stu-id="3960c-140">-Name</span></span>
<span data-ttu-id="3960c-141">통신 이름.</span><span class="sxs-lookup"><span data-stu-id="3960c-141">Communication name.</span></span>

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

### <span data-ttu-id="3960c-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="3960c-142">-SupportTicketName</span></span>
<span data-ttu-id="3960c-143">티켓 이름을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-143">Support ticket name.</span></span>

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

### <span data-ttu-id="3960c-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="3960c-144">-SupportTicketObject</span></span>
<span data-ttu-id="3960c-145">티켓 개체를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-145">Support ticket object.</span></span>

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

### <span data-ttu-id="3960c-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3960c-146">-IncludeTotalCount</span></span>
<span data-ttu-id="3960c-147">데이터 집합 (정수)에 있는 개체의 총 수와 선택한 개체를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="3960c-148">Cmdlet에서 총 개수를 확인할 수 없는 경우 "알 수 없는 총 개수"가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="3960c-149">Integer에는 총 count 값의 안정성을 나타내는 정확도 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="3960c-150">정확도 값의 범위는 0.0에서 0.0 1.0는 cmdlet이 개체 수를 계산할 수 없음을 의미 하 고, 1.0에서는 카운트가 정확한 지를 의미 하며, 0.0 및 1.0 간의 값이 점차 안정적인 추정치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="3960c-151">-생략</span><span class="sxs-lookup"><span data-stu-id="3960c-151">-Skip</span></span>
<span data-ttu-id="3960c-152">지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="3960c-153">건너뛸 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="3960c-154">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="3960c-154">-First</span></span>
<span data-ttu-id="3960c-155">지정 된 수의 개체만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="3960c-156">가져올 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="3960c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3960c-157">CommonParameters</span></span>
<span data-ttu-id="3960c-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3960c-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3960c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3960c-160">입력</span><span class="sxs-lookup"><span data-stu-id="3960c-160">INPUTS</span></span>

### <span data-ttu-id="3960c-161">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="3960c-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="3960c-162">출력</span><span class="sxs-lookup"><span data-stu-id="3960c-162">OUTPUTS</span></span>

### <span data-ttu-id="3960c-163">PSSupportTicketCommunication를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3960c-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="3960c-164">상속자</span><span class="sxs-lookup"><span data-stu-id="3960c-164">NOTES</span></span>

## <span data-ttu-id="3960c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3960c-165">RELATED LINKS</span></span>
