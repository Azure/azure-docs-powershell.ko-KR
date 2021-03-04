---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981915"
---
# <span data-ttu-id="d0cd8-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="d0cd8-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="d0cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cd8-103">지원 티켓 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-103">Get support ticket communications.</span></span>

## <span data-ttu-id="d0cd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0cd8-104">SYNTAX</span></span>

### <span data-ttu-id="d0cd8-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d0cd8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0cd8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0cd8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0cd8-107">설명</span><span class="sxs-lookup"><span data-stu-id="d0cd8-107">DESCRIPTION</span></span>
<span data-ttu-id="d0cd8-108">지원 티켓에 대한 통신을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="d0cd8-109">다른 매개 변수를 지정하지 않으면 티켓에 대한 모든 통신을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="d0cd8-110">필터 매개 변수를 사용하여 CreatedDate 또는 CommunicationType을 사용하여 통신을 필터링할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="d0cd8-111">다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="d0cd8-112">시나리오</span><span class="sxs-lookup"><span data-stu-id="d0cd8-112">Scenario</span></span>                                                        | <span data-ttu-id="d0cd8-113">필터</span><span class="sxs-lookup"><span data-stu-id="d0cd8-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d0cd8-114">웹 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-114">Get Web communications</span></span>                                          | <span data-ttu-id="d0cd8-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="d0cd8-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="d0cd8-116">전화 통신하기</span><span class="sxs-lookup"><span data-stu-id="d0cd8-116">Get Phone communications</span></span>                                        | <span data-ttu-id="d0cd8-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="d0cd8-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="d0cd8-118">2019년 12월 20일 이후에 생성된 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="d0cd8-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="d0cd8-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="d0cd8-120">2019년 12월 20일 이후에 생성된 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="d0cd8-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="d0cd8-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="d0cd8-122">2019년 12월 20일 이후에 만든 웹 통신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="d0cd8-123">"CreatedDate gt 2019-12-20 및 CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="d0cd8-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="d0cd8-124">이 cmdlet은 First 및 Skip 매개 변수를 통해 파이징을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="d0cd8-125">통신 이름을 지정하여 단일 지원 티켓 통신을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="d0cd8-126">예제</span><span class="sxs-lookup"><span data-stu-id="d0cd8-126">EXAMPLES</span></span>

### <span data-ttu-id="d0cd8-127">예제 1: 지원 티켓에 대한 모든 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="d0cd8-128">예제 2: 지원 티켓의 이름으로 단일 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="d0cd8-129">예제 3: 지원 티켓에 대한 처음 2개 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d0cd8-130">예제 4: 지원 티켓에 대한 처음 2개 통신을 건너뛰고 나서 다음 2개 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d0cd8-131">예제 5: 지원 티켓에 대한 모든 웹 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d0cd8-132">예제 6: 지원 티켓에 대해 2019년 12월 20일 이후에 생성된 모든 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d0cd8-133">예제 7: 지원 티켓에 대해 2019년 12월 20일 이후에 생성된 모든 웹 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="d0cd8-134">예제 8: 지원 티켓 개체를 파이핑하여 지원 티켓에 대한 모든 통신 검색</span><span class="sxs-lookup"><span data-stu-id="d0cd8-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="d0cd8-135">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d0cd8-135">PARAMETERS</span></span>

### <span data-ttu-id="d0cd8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cd8-136">-DefaultProfile</span></span>
<span data-ttu-id="d0cd8-137">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0cd8-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="d0cd8-138">-Filter</span></span>
<span data-ttu-id="d0cd8-139">이 cmdlet의 결과에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="d0cd8-140">-Name</span><span class="sxs-lookup"><span data-stu-id="d0cd8-140">-Name</span></span>
<span data-ttu-id="d0cd8-141">통신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-141">Communication name.</span></span>

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

### <span data-ttu-id="d0cd8-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="d0cd8-142">-SupportTicketName</span></span>
<span data-ttu-id="d0cd8-143">티켓 이름을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-143">Support ticket name.</span></span>

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

### <span data-ttu-id="d0cd8-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="d0cd8-144">-SupportTicketObject</span></span>
<span data-ttu-id="d0cd8-145">티켓 개체를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-145">Support ticket object.</span></span>

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

### <span data-ttu-id="d0cd8-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d0cd8-146">-IncludeTotalCount</span></span>
<span data-ttu-id="d0cd8-147">데이터 집합의 총 개체 수(정수)와 선택한 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="d0cd8-148">cmdlet에서 총 수를 확인할 수 없는 경우 "알 수 없음 총 수"가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="d0cd8-149">정수에는 총 개수 값의 안정성을 나타내는 정확도 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="d0cd8-150">정확도 값은 0.0에서 1.0 사이입니다. 여기서 0.0은 cmdlet이 개체를 계산할 수 없습니다. 1.0은 개수가 정확하고 0.0과 1.0 사이의 값은 점점 더 신뢰할 수 있는 예측을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="d0cd8-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="d0cd8-151">-Skip</span></span>
<span data-ttu-id="d0cd8-152">지정된 개체 수를 무시한 다음 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="d0cd8-153">건너뛸 개체 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="d0cd8-154">-First</span><span class="sxs-lookup"><span data-stu-id="d0cd8-154">-First</span></span>
<span data-ttu-id="d0cd8-155">지정된 개체 수만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="d0cd8-156">얻을 개체 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="d0cd8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cd8-157">CommonParameters</span></span>
<span data-ttu-id="d0cd8-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0cd8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cd8-159">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0cd8-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cd8-160">입력</span><span class="sxs-lookup"><span data-stu-id="d0cd8-160">INPUTS</span></span>

### <span data-ttu-id="d0cd8-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="d0cd8-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="d0cd8-162">출력</span><span class="sxs-lookup"><span data-stu-id="d0cd8-162">OUTPUTS</span></span>

### <span data-ttu-id="d0cd8-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="d0cd8-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="d0cd8-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0cd8-164">NOTES</span></span>

## <span data-ttu-id="d0cd8-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0cd8-165">RELATED LINKS</span></span>
