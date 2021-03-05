---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011792"
---
# <span data-ttu-id="a3eb6-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="a3eb6-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="a3eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3eb6-103">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="a3eb6-103">Create cluster</span></span>

## <span data-ttu-id="a3eb6-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3eb6-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3eb6-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3eb6-105">DESCRIPTION</span></span>

<span data-ttu-id="a3eb6-106">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="a3eb6-106">Create cluster</span></span>

## <span data-ttu-id="a3eb6-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3eb6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3eb6-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="a3eb6-109">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="a3eb6-109">Create cluster</span></span>

## <span data-ttu-id="a3eb6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="a3eb6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3eb6-111">-AsJob</span></span>
<span data-ttu-id="a3eb6-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a3eb6-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a3eb6-113">-ClusterName</span></span>
<span data-ttu-id="a3eb6-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3eb6-115">-DefaultProfile</span></span>
<span data-ttu-id="a3eb6-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a3eb6-117">-IdentityType</span></span>
<span data-ttu-id="a3eb6-118">ID 형식, 값은 'SystemAssigned', 'None'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a3eb6-119">-Location</span></span>
<span data-ttu-id="a3eb6-120">클러스터가 배포될 지리적 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3eb6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3eb6-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a3eb6-123">-SkuCapacity</span></span>
<span data-ttu-id="a3eb6-124">Sku 용량, 값은 100의 배수 및 1000-2000 범위에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a3eb6-125">-SkuName</span></span>
<span data-ttu-id="a3eb6-126">Sku 이름, 이제 'CapacityReservation'이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="a3eb6-127">-Tags</span></span>
<span data-ttu-id="a3eb6-128">클러스터의 태그</span><span class="sxs-lookup"><span data-stu-id="a3eb6-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a3eb6-129">-Confirm</span></span>
<span data-ttu-id="a3eb6-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3eb6-131">-WhatIf</span></span>
<span data-ttu-id="a3eb6-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3eb6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3eb6-134">CommonParameters</span></span>
<span data-ttu-id="a3eb6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3eb6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3eb6-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3eb6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3eb6-137">입력</span><span class="sxs-lookup"><span data-stu-id="a3eb6-137">INPUTS</span></span>

### <span data-ttu-id="a3eb6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a3eb6-138">System.String</span></span>

## <span data-ttu-id="a3eb6-139">출력</span><span class="sxs-lookup"><span data-stu-id="a3eb6-139">OUTPUTS</span></span>

### <span data-ttu-id="a3eb6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a3eb6-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="a3eb6-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3eb6-141">NOTES</span></span>

## <span data-ttu-id="a3eb6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3eb6-142">RELATED LINKS</span></span>
