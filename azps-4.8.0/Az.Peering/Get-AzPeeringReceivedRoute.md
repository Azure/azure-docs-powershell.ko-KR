---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214299"
---
# <span data-ttu-id="65f89-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="65f89-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="65f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f89-102">SYNOPSIS</span></span>
<span data-ttu-id="65f89-103">피어 링에 대해 수신 된 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="65f89-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65f89-104">SYNTAX</span></span>

### <span data-ttu-id="65f89-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="65f89-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65f89-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65f89-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65f89-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65f89-107">DESCRIPTION</span></span>
<span data-ttu-id="65f89-108">피어 링에서 수신 된 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="65f89-109">예제의</span><span class="sxs-lookup"><span data-stu-id="65f89-109">EXAMPLES</span></span>

### <span data-ttu-id="65f89-110">목록 상위 100에서 피어 링에 대 한 경로를 수신 했습니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="65f89-111">피어 링에 대해 수신 된 모든 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="65f89-112">경로로 필터링</span><span class="sxs-lookup"><span data-stu-id="65f89-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="65f89-113">다음으로 필터를 사용 하 여 피어 링에 대해 수신 된 모든 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="65f89-114">RPKIValidationState로 필터링</span><span class="sxs-lookup"><span data-stu-id="65f89-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="65f89-115">RPKIValidationState에서 필터를 사용 하 여 피어 링에 대해 수신 된 모든 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="65f89-116">OriginAsValidationState로 필터링</span><span class="sxs-lookup"><span data-stu-id="65f89-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="65f89-117">OriginAsValidationState에서 필터를 사용 하 여 피어 링에 대해 수신 된 모든 경로를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="65f89-118">변수</span><span class="sxs-lookup"><span data-stu-id="65f89-118">PARAMETERS</span></span>

### <span data-ttu-id="65f89-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="65f89-119">-AsPath</span></span>
<span data-ttu-id="65f89-120">경로로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-120">Filter by AS Path.</span></span>
<span data-ttu-id="65f89-121">예: ' 9342 1234 4567 '</span><span class="sxs-lookup"><span data-stu-id="65f89-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="65f89-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f89-122">-DefaultProfile</span></span>
<span data-ttu-id="65f89-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f89-124">-이름</span><span class="sxs-lookup"><span data-stu-id="65f89-124">-Name</span></span>
<span data-ttu-id="65f89-125">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="65f89-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="65f89-126">-OriginAsValidationState</span></span>
<span data-ttu-id="65f89-127">원점을 기준으로 유효성 검사 상태로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="65f89-128">-접두사</span><span class="sxs-lookup"><span data-stu-id="65f89-128">-Prefix</span></span>
<span data-ttu-id="65f89-129">접두사로 필터링</span><span class="sxs-lookup"><span data-stu-id="65f89-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="65f89-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65f89-130">-ResourceGroupName</span></span>
<span data-ttu-id="65f89-131">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="65f89-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65f89-132">-ResourceId</span></span>
<span data-ttu-id="65f89-133">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-133">The resource id string name.</span></span>

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

### <span data-ttu-id="65f89-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="65f89-134">-RPKIValidationState</span></span>
<span data-ttu-id="65f89-135">RPKI 유효성 검사 상태별로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="65f89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f89-136">CommonParameters</span></span>
<span data-ttu-id="65f89-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65f89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f89-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="65f89-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f89-139">입력</span><span class="sxs-lookup"><span data-stu-id="65f89-139">INPUTS</span></span>

### <span data-ttu-id="65f89-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65f89-140">System.String</span></span>

## <span data-ttu-id="65f89-141">출력</span><span class="sxs-lookup"><span data-stu-id="65f89-141">OUTPUTS</span></span>

### <span data-ttu-id="65f89-142">PSPeeringReceivedRoute (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="65f89-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="65f89-143">상속자</span><span class="sxs-lookup"><span data-stu-id="65f89-143">NOTES</span></span>

## <span data-ttu-id="65f89-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65f89-144">RELATED LINKS</span></span>
