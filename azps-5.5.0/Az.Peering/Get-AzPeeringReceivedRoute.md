---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184049"
---
# <span data-ttu-id="ee0f3-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="ee0f3-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="ee0f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0f3-103">피어링에 대해 수신된 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="ee0f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee0f3-104">SYNTAX</span></span>

### <span data-ttu-id="ee0f3-105">ByResourceGroupAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee0f3-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee0f3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee0f3-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee0f3-107">설명</span><span class="sxs-lookup"><span data-stu-id="ee0f3-107">DESCRIPTION</span></span>
<span data-ttu-id="ee0f3-108">피어링에서 받은 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="ee0f3-109">예제</span><span class="sxs-lookup"><span data-stu-id="ee0f3-109">EXAMPLES</span></span>

### <span data-ttu-id="ee0f3-110">피어링에 대해 받은 상위 100개 경로 나열</span><span class="sxs-lookup"><span data-stu-id="ee0f3-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="ee0f3-111">피어링에 대해 수신된 모든 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="ee0f3-112">AS 경로로 필터링</span><span class="sxs-lookup"><span data-stu-id="ee0f3-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="ee0f3-113">AS에 필터가 있는 피어링에 대해 수신된 모든 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="ee0f3-114">RPKIValidationState로 필터링</span><span class="sxs-lookup"><span data-stu-id="ee0f3-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="ee0f3-115">RPKIValidationState에 필터가 있는 피어링에 대해 수신된 모든 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="ee0f3-116">OriginAsValidationState로 필터링</span><span class="sxs-lookup"><span data-stu-id="ee0f3-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="ee0f3-117">OriginAsValidationState에서 필터를 사용하여 피어링에 대해 수신된 모든 경로를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="ee0f3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee0f3-118">PARAMETERS</span></span>

### <span data-ttu-id="ee0f3-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="ee0f3-119">-AsPath</span></span>
<span data-ttu-id="ee0f3-120">AS 경로로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-120">Filter by AS Path.</span></span>
<span data-ttu-id="ee0f3-121">예: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="ee0f3-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="ee0f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0f3-122">-DefaultProfile</span></span>
<span data-ttu-id="ee0f3-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee0f3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0f3-124">-Name</span></span>
<span data-ttu-id="ee0f3-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0f3-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="ee0f3-126">-OriginAsValidationState</span></span>
<span data-ttu-id="ee0f3-127">원본 AS 유효성 검사 상태로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="ee0f3-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ee0f3-128">-Prefix</span></span>
<span data-ttu-id="ee0f3-129">연결선으로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="ee0f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="ee0f3-131">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0f3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee0f3-132">-ResourceId</span></span>
<span data-ttu-id="ee0f3-133">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee0f3-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="ee0f3-134">-RPKIValidationState</span></span>
<span data-ttu-id="ee0f3-135">RPKI 유효성 검사 상태를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="ee0f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0f3-136">CommonParameters</span></span>
<span data-ttu-id="ee0f3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0f3-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee0f3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0f3-139">입력</span><span class="sxs-lookup"><span data-stu-id="ee0f3-139">INPUTS</span></span>

### <span data-ttu-id="ee0f3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee0f3-140">System.String</span></span>

## <span data-ttu-id="ee0f3-141">출력</span><span class="sxs-lookup"><span data-stu-id="ee0f3-141">OUTPUTS</span></span>

### <span data-ttu-id="ee0f3-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="ee0f3-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="ee0f3-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee0f3-143">NOTES</span></span>

## <span data-ttu-id="ee0f3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee0f3-144">RELATED LINKS</span></span>
