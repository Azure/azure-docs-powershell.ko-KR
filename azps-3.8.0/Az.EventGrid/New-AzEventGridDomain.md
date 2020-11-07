---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878302"
---
# <span data-ttu-id="89a41-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="89a41-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="89a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a41-102">SYNOPSIS</span></span>
<span data-ttu-id="89a41-103">새 Azure 이벤트 그리드 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="89a41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89a41-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89a41-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89a41-105">DESCRIPTION</span></span>
<span data-ttu-id="89a41-106">새 Azure 이벤트 그리드 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="89a41-107">도메인을 만든 후에는 응용 프로그램에서 항목 끝점에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="89a41-108">예제의</span><span class="sxs-lookup"><span data-stu-id="89a41-108">EXAMPLES</span></span>

### <span data-ttu-id="89a41-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="89a41-109">Example 1</span></span>

<span data-ttu-id="89a41-110">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 westus2에 이벤트 \` 그리드 도메인 Domain1을 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="89a41-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="89a41-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="89a41-111">Example 2</span></span>

<span data-ttu-id="89a41-112">지정 된 \` \` \` \` \` \` 태그 "부서" 및 "환경"이 있는 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 westus2에 이벤트 그리드 도메인 Domain1을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="89a41-113">변수</span><span class="sxs-lookup"><span data-stu-id="89a41-113">PARAMETERS</span></span>

### <span data-ttu-id="89a41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a41-114">-DefaultProfile</span></span>
<span data-ttu-id="89a41-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89a41-116">-위치</span><span class="sxs-lookup"><span data-stu-id="89a41-116">-Location</span></span>
<span data-ttu-id="89a41-117">도메인의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-117">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-118">-이름</span><span class="sxs-lookup"><span data-stu-id="89a41-118">-Name</span></span>
<span data-ttu-id="89a41-119">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89a41-120">-ResourceGroupName</span></span>
<span data-ttu-id="89a41-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-122">태그</span><span class="sxs-lookup"><span data-stu-id="89a41-122">-Tag</span></span>
<span data-ttu-id="89a41-123">리소스 태그를 나타내는 Hashtable</span><span class="sxs-lookup"><span data-stu-id="89a41-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-124">-확인</span><span class="sxs-lookup"><span data-stu-id="89a41-124">-Confirm</span></span>
<span data-ttu-id="89a41-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a41-126">-WhatIf</span></span>
<span data-ttu-id="89a41-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a41-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89a41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a41-129">CommonParameters</span></span>
<span data-ttu-id="89a41-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89a41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a41-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a41-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a41-132">입력</span><span class="sxs-lookup"><span data-stu-id="89a41-132">INPUTS</span></span>

### <span data-ttu-id="89a41-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89a41-133">System.String</span></span>

### <span data-ttu-id="89a41-134">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="89a41-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="89a41-135">출력</span><span class="sxs-lookup"><span data-stu-id="89a41-135">OUTPUTS</span></span>

### <span data-ttu-id="89a41-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="89a41-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="89a41-137">상속자</span><span class="sxs-lookup"><span data-stu-id="89a41-137">NOTES</span></span>

## <span data-ttu-id="89a41-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89a41-138">RELATED LINKS</span></span>
