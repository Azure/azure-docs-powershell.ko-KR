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
# <span data-ttu-id="7f40b-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7f40b-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="7f40b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f40b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f40b-103">지원 티켓 받기</span><span class="sxs-lookup"><span data-stu-id="7f40b-103">Get support tickets.</span></span>

## <span data-ttu-id="7f40b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f40b-104">SYNTAX</span></span>

### <span data-ttu-id="7f40b-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f40b-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7f40b-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f40b-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7f40b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7f40b-107">DESCRIPTION</span></span>
<span data-ttu-id="7f40b-108">지원 티켓 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-108">Gets the list of support tickets.</span></span> <span data-ttu-id="7f40b-109">매개 변수를 지정 하지 않으면 모든 지원 티켓이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="7f40b-110">Filter 매개 변수를 사용 하 여 상태 또는 CreatedDate 지원 티켓을 필터링 할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="7f40b-111">다음은 지정할 수 있는 필터 값의 몇 가지 예입니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="7f40b-112">시나리오</span><span class="sxs-lookup"><span data-stu-id="7f40b-112">Scenario</span></span>                                                         | <span data-ttu-id="7f40b-113">분류</span><span class="sxs-lookup"><span data-stu-id="7f40b-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="7f40b-114">열린 상태인 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="7f40b-115">"상태 eq ' 열림 '"</span><span class="sxs-lookup"><span data-stu-id="7f40b-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="7f40b-116">닫힌 상태의 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="7f40b-117">"상태 eq ' 닫힘"</span><span class="sxs-lookup"><span data-stu-id="7f40b-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="7f40b-118">2019 년 12 월 20th 일 이후에 만들어진 티켓을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="7f40b-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7f40b-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="7f40b-120">2019 년 12 월 20th 일 이후에 만들어진 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="7f40b-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="7f40b-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="7f40b-122">열림 상태인 2019 년 12 월 20th 이후 생성 된 티켓을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="7f40b-123">"CreatedDate gt 2019-12-20 및 상태 eq ' Open '"</span><span class="sxs-lookup"><span data-stu-id="7f40b-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="7f40b-124">이 cmdlet은 First 및 Skip 매개 변수를 통해 페이징을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="7f40b-125">티켓 이름을 지정 하 여 단일 지원 티켓을 검색할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="7f40b-126">예제의</span><span class="sxs-lookup"><span data-stu-id="7f40b-126">EXAMPLES</span></span>

### <span data-ttu-id="7f40b-127">예제 1: 첫 2 개의 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f40b-128">예제 2: 첫 2 티켓을 건너뛴 후 처음 2 개의 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f40b-129">예제 3: 이름으로 지원 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f40b-130">예제 4: 상태별로 필터링 된 처음 2 개의 지원 티켓 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f40b-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7f40b-131">예제 5: 열려 있는 상태의 모든 지원 티켓을 가져오고 Dec 20th 이후 만든 2019</span><span class="sxs-lookup"><span data-stu-id="7f40b-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="7f40b-132">변수</span><span class="sxs-lookup"><span data-stu-id="7f40b-132">PARAMETERS</span></span>

### <span data-ttu-id="7f40b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f40b-133">-DefaultProfile</span></span>
<span data-ttu-id="7f40b-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f40b-135">-필터</span><span class="sxs-lookup"><span data-stu-id="7f40b-135">-Filter</span></span>
<span data-ttu-id="7f40b-136">이 cmdlet의 결과에 적용할 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="7f40b-137">-이름</span><span class="sxs-lookup"><span data-stu-id="7f40b-137">-Name</span></span>
<span data-ttu-id="7f40b-138">이 cmdlet이 가져오는 지원 티켓의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7f40b-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7f40b-139">-IncludeTotalCount</span></span>
<span data-ttu-id="7f40b-140">데이터 집합 (정수)에 있는 개체의 총 수와 선택한 개체를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="7f40b-141">Cmdlet에서 총 개수를 확인할 수 없는 경우 "알 수 없는 총 개수"가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="7f40b-142">Integer에는 총 count 값의 안정성을 나타내는 정확도 속성이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="7f40b-143">정확도 값의 범위는 0.0에서 0.0 1.0는 cmdlet이 개체 수를 계산할 수 없음을 의미 하 고, 1.0에서는 카운트가 정확한 지를 의미 하며, 0.0 및 1.0 간의 값이 점차 안정적인 추정치를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="7f40b-144">-생략</span><span class="sxs-lookup"><span data-stu-id="7f40b-144">-Skip</span></span>
<span data-ttu-id="7f40b-145">지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="7f40b-146">건너뛸 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="7f40b-147">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="7f40b-147">-First</span></span>
<span data-ttu-id="7f40b-148">지정 된 수의 개체만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="7f40b-149">가져올 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="7f40b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f40b-150">CommonParameters</span></span>
<span data-ttu-id="7f40b-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f40b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f40b-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f40b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f40b-153">입력</span><span class="sxs-lookup"><span data-stu-id="7f40b-153">INPUTS</span></span>

### <span data-ttu-id="7f40b-154">않아야</span><span class="sxs-lookup"><span data-stu-id="7f40b-154">None</span></span>

## <span data-ttu-id="7f40b-155">출력</span><span class="sxs-lookup"><span data-stu-id="7f40b-155">OUTPUTS</span></span>

### <span data-ttu-id="7f40b-156">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="7f40b-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7f40b-157">상속자</span><span class="sxs-lookup"><span data-stu-id="7f40b-157">NOTES</span></span>

## <span data-ttu-id="7f40b-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f40b-158">RELATED LINKS</span></span>
