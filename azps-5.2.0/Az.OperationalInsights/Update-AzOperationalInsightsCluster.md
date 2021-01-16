---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364757"
---
# <span data-ttu-id="fea31-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="fea31-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="fea31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea31-102">SYNOPSIS</span></span>
<span data-ttu-id="fea31-103">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="fea31-103">update cluster</span></span>

## <span data-ttu-id="fea31-104">구문</span><span class="sxs-lookup"><span data-stu-id="fea31-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea31-105">설명</span><span class="sxs-lookup"><span data-stu-id="fea31-105">DESCRIPTION</span></span>
<span data-ttu-id="fea31-106">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="fea31-106">update cluster</span></span>

## <span data-ttu-id="fea31-107">예제</span><span class="sxs-lookup"><span data-stu-id="fea31-107">EXAMPLES</span></span>

### <span data-ttu-id="fea31-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fea31-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="fea31-109">키 자격 증명 모음 속성 및 SKU를 사용하여 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="fea31-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="fea31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fea31-110">PARAMETERS</span></span>

### <span data-ttu-id="fea31-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fea31-111">-AsJob</span></span>
<span data-ttu-id="fea31-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fea31-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fea31-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fea31-113">-ClusterName</span></span>
<span data-ttu-id="fea31-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-114">The cluster name.</span></span>

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

### <span data-ttu-id="fea31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea31-115">-DefaultProfile</span></span>
<span data-ttu-id="fea31-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea31-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fea31-117">-KeyName</span></span>
<span data-ttu-id="fea31-118">키 이름</span><span class="sxs-lookup"><span data-stu-id="fea31-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="fea31-119">-KeyVaultUri</span></span>
<span data-ttu-id="fea31-120">Key Vault Uri, "제거 보호" 및 "소프트 삭제"를 이 키 자격 증명 모음에 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="fea31-121">-KeyVersion</span></span>
<span data-ttu-id="fea31-122">키 버전</span><span class="sxs-lookup"><span data-stu-id="fea31-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea31-123">-ResourceGroupName</span></span>
<span data-ttu-id="fea31-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-124">The resource group name.</span></span>

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

### <span data-ttu-id="fea31-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fea31-125">-SkuCapacity</span></span>
<span data-ttu-id="fea31-126">SKU 용량</span><span class="sxs-lookup"><span data-stu-id="fea31-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea31-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fea31-127">-SkuName</span></span>
<span data-ttu-id="fea31-128">SKU 이름, 이제 'CapacityReservation'만 가능</span><span class="sxs-lookup"><span data-stu-id="fea31-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="fea31-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="fea31-129">-Tags</span></span>
<span data-ttu-id="fea31-130">클러스터의 태그</span><span class="sxs-lookup"><span data-stu-id="fea31-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="fea31-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fea31-131">-Confirm</span></span>
<span data-ttu-id="fea31-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fea31-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea31-133">-WhatIf</span></span>
<span data-ttu-id="fea31-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fea31-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea31-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fea31-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea31-136">CommonParameters</span></span>
<span data-ttu-id="fea31-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fea31-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea31-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fea31-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea31-139">입력</span><span class="sxs-lookup"><span data-stu-id="fea31-139">INPUTS</span></span>

### <span data-ttu-id="fea31-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fea31-140">System.String</span></span>

## <span data-ttu-id="fea31-141">출력</span><span class="sxs-lookup"><span data-stu-id="fea31-141">OUTPUTS</span></span>

### <span data-ttu-id="fea31-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="fea31-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="fea31-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fea31-143">NOTES</span></span>

## <span data-ttu-id="fea31-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fea31-144">RELATED LINKS</span></span>
