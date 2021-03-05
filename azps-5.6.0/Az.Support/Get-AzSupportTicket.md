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
# <span data-ttu-id="12ca8-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="12ca8-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="12ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="12ca8-103">지원 티켓을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-103">Get support tickets.</span></span>

## <span data-ttu-id="12ca8-104">구문</span><span class="sxs-lookup"><span data-stu-id="12ca8-104">SYNTAX</span></span>

### <span data-ttu-id="12ca8-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="12ca8-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="12ca8-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12ca8-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="12ca8-107">설명</span><span class="sxs-lookup"><span data-stu-id="12ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="12ca8-108">지원 티켓 목록을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-108">Gets the list of support tickets.</span></span> <span data-ttu-id="12ca8-109">매개 변수를 지정하지 않으면 모든 지원 티켓을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="12ca8-110">필터 매개 변수를 사용하여 상태 또는 CreatedDate로 지원 티켓을 필터링할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="12ca8-111">다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="12ca8-112">시나리오</span><span class="sxs-lookup"><span data-stu-id="12ca8-112">Scenario</span></span>                                                         | <span data-ttu-id="12ca8-113">필터</span><span class="sxs-lookup"><span data-stu-id="12ca8-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="12ca8-114">열려 있는 티켓을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="12ca8-115">"상태 eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="12ca8-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="12ca8-116">닫힌 상태의 티켓을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="12ca8-117">"상태 eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="12ca8-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="12ca8-118">2019년 12월 20일 이후에 만든 티켓을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="12ca8-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="12ca8-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="12ca8-120">2019년 12월 20일 이후에 만든 티켓을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="12ca8-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="12ca8-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="12ca8-122">열려 있는 2019년 12월 20일 이후에 만든 티켓을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="12ca8-123">"CreatedDate gt 2019-12-20 및 Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="12ca8-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="12ca8-124">이 cmdlet은 First 및 Skip 매개 변수를 통해 파이징을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="12ca8-125">티켓 이름을 지정하여 단일 지원 티켓을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="12ca8-126">예제</span><span class="sxs-lookup"><span data-stu-id="12ca8-126">EXAMPLES</span></span>

### <span data-ttu-id="12ca8-127">예제 1: 처음 2개 티켓을 얻다</span><span class="sxs-lookup"><span data-stu-id="12ca8-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12ca8-128">예제 2: 처음 2를 건너뛰고 나서 첫 2 티켓을 얻게 합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12ca8-129">예제 3: 이름에 의해 지원 티켓을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12ca8-130">예제 4: 상태로 필터링된 첫 번째 2개 지원 티켓을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="12ca8-131">예제 5: 열려 있는 상태의 모든 지원 티켓을 2019년 12월 20일 이후에 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="12ca8-132">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12ca8-132">PARAMETERS</span></span>

### <span data-ttu-id="12ca8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ca8-133">-DefaultProfile</span></span>
<span data-ttu-id="12ca8-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ca8-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="12ca8-135">-Filter</span></span>
<span data-ttu-id="12ca8-136">이 cmdlet의 결과에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="12ca8-137">-Name</span><span class="sxs-lookup"><span data-stu-id="12ca8-137">-Name</span></span>
<span data-ttu-id="12ca8-138">이 cmdlet이 얻을 지원 티켓의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12ca8-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="12ca8-139">-IncludeTotalCount</span></span>
<span data-ttu-id="12ca8-140">데이터 집합의 총 개체 수(정수)와 선택한 개체 수를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="12ca8-141">cmdlet에서 총 수를 확인할 수 없는 경우 "알 수 없음 총 수"가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="12ca8-142">정수에는 총 개수 값의 안정성을 나타내는 정확도 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="12ca8-143">정확도 값은 0.0에서 1.0 사이입니다. 여기서 0.0은 cmdlet이 개체를 계산할 수 없습니다. 1.0은 개수가 정확하고 0.0과 1.0 사이의 값은 점점 더 신뢰할 수 있는 예측을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="12ca8-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="12ca8-144">-Skip</span></span>
<span data-ttu-id="12ca8-145">지정된 개체 수를 무시한 다음 나머지 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="12ca8-146">건너뛸 개체 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="12ca8-147">-First</span><span class="sxs-lookup"><span data-stu-id="12ca8-147">-First</span></span>
<span data-ttu-id="12ca8-148">지정된 개체 수만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="12ca8-149">얻을 개체 수를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="12ca8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ca8-150">CommonParameters</span></span>
<span data-ttu-id="12ca8-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12ca8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ca8-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12ca8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ca8-153">입력</span><span class="sxs-lookup"><span data-stu-id="12ca8-153">INPUTS</span></span>

### <span data-ttu-id="12ca8-154">없음</span><span class="sxs-lookup"><span data-stu-id="12ca8-154">None</span></span>

## <span data-ttu-id="12ca8-155">출력</span><span class="sxs-lookup"><span data-stu-id="12ca8-155">OUTPUTS</span></span>

### <span data-ttu-id="12ca8-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="12ca8-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="12ca8-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12ca8-157">NOTES</span></span>

## <span data-ttu-id="12ca8-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12ca8-158">RELATED LINKS</span></span>
