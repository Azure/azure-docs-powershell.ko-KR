---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308051"
---
# <span data-ttu-id="745c3-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="745c3-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="745c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745c3-102">SYNOPSIS</span></span>
<span data-ttu-id="745c3-103">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="745c3-103">Create cluster</span></span>

## <span data-ttu-id="745c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="745c3-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="745c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="745c3-105">DESCRIPTION</span></span>

<span data-ttu-id="745c3-106">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="745c3-106">Create cluster</span></span>

## <span data-ttu-id="745c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="745c3-107">EXAMPLES</span></span>

### <span data-ttu-id="745c3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="745c3-108">Example 1</span></span>
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

<span data-ttu-id="745c3-109">클러스터 만들기</span><span class="sxs-lookup"><span data-stu-id="745c3-109">Create cluster</span></span>

## <span data-ttu-id="745c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="745c3-110">PARAMETERS</span></span>

### <span data-ttu-id="745c3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="745c3-111">-AsJob</span></span>
<span data-ttu-id="745c3-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="745c3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="745c3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="745c3-113">-ClusterName</span></span>
<span data-ttu-id="745c3-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-114">The cluster name.</span></span>

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

### <span data-ttu-id="745c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745c3-115">-DefaultProfile</span></span>
<span data-ttu-id="745c3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="745c3-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="745c3-117">-IdentityType</span></span>
<span data-ttu-id="745c3-118">id 형식, 값은 ' SystemAssigned ', ' n o ' 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="745c3-119">-위치</span><span class="sxs-lookup"><span data-stu-id="745c3-119">-Location</span></span>
<span data-ttu-id="745c3-120">클러스터가 배포 될 지리적 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="745c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="745c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="745c3-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-122">The resource group name.</span></span>

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

### <span data-ttu-id="745c3-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="745c3-123">-SkuCapacity</span></span>
<span data-ttu-id="745c3-124">Sku 용량, 값은 100의 배수 여야 하며 1000-2000 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="745c3-125">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="745c3-125">-SkuName</span></span>
<span data-ttu-id="745c3-126">Sku 이름-이제 ' CapacityReservation ' 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="745c3-127">태그</span><span class="sxs-lookup"><span data-stu-id="745c3-127">-Tags</span></span>
<span data-ttu-id="745c3-128">클러스터의 태그</span><span class="sxs-lookup"><span data-stu-id="745c3-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="745c3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="745c3-129">-Confirm</span></span>
<span data-ttu-id="745c3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="745c3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745c3-131">-WhatIf</span></span>
<span data-ttu-id="745c3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745c3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="745c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745c3-134">CommonParameters</span></span>
<span data-ttu-id="745c3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="745c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745c3-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="745c3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745c3-137">입력</span><span class="sxs-lookup"><span data-stu-id="745c3-137">INPUTS</span></span>

### <span data-ttu-id="745c3-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="745c3-138">System.String</span></span>

## <span data-ttu-id="745c3-139">출력</span><span class="sxs-lookup"><span data-stu-id="745c3-139">OUTPUTS</span></span>

### <span data-ttu-id="745c3-140">OperationalInsights 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="745c3-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="745c3-141">상속자</span><span class="sxs-lookup"><span data-stu-id="745c3-141">NOTES</span></span>

## <span data-ttu-id="745c3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="745c3-142">RELATED LINKS</span></span>
