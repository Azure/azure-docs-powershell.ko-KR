---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191476"
---
# <span data-ttu-id="0b43b-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="0b43b-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="0b43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b43b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b43b-103">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="0b43b-103">update cluster</span></span>

## <span data-ttu-id="0b43b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b43b-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b43b-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b43b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b43b-106">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="0b43b-106">update cluster</span></span>

## <span data-ttu-id="0b43b-107">예제</span><span class="sxs-lookup"><span data-stu-id="0b43b-107">EXAMPLES</span></span>

### <span data-ttu-id="0b43b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b43b-108">Example 1</span></span>
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

<span data-ttu-id="0b43b-109">키 자격 증명 모음 속성 및 SKU를 사용하여 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="0b43b-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="0b43b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b43b-110">PARAMETERS</span></span>

### <span data-ttu-id="0b43b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b43b-111">-AsJob</span></span>
<span data-ttu-id="0b43b-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0b43b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b43b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0b43b-113">-ClusterName</span></span>
<span data-ttu-id="0b43b-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-114">The cluster name.</span></span>

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

### <span data-ttu-id="0b43b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b43b-115">-DefaultProfile</span></span>
<span data-ttu-id="0b43b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b43b-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b43b-117">-KeyName</span></span>
<span data-ttu-id="0b43b-118">키 이름</span><span class="sxs-lookup"><span data-stu-id="0b43b-118">Key Name</span></span>

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

### <span data-ttu-id="0b43b-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="0b43b-119">-KeyVaultUri</span></span>
<span data-ttu-id="0b43b-120">Key Vault Uri, "제거 보호" 및 "소프트 삭제"를 이 키 자격 증명 모음에 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="0b43b-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="0b43b-121">-KeyVersion</span></span>
<span data-ttu-id="0b43b-122">키 버전</span><span class="sxs-lookup"><span data-stu-id="0b43b-122">Key Version</span></span>

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

### <span data-ttu-id="0b43b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b43b-123">-ResourceGroupName</span></span>
<span data-ttu-id="0b43b-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-124">The resource group name.</span></span>

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

### <span data-ttu-id="0b43b-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0b43b-125">-SkuCapacity</span></span>
<span data-ttu-id="0b43b-126">SKU 용량</span><span class="sxs-lookup"><span data-stu-id="0b43b-126">Sku Capacity</span></span>

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

### <span data-ttu-id="0b43b-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0b43b-127">-SkuName</span></span>
<span data-ttu-id="0b43b-128">SKU 이름, 이제 'CapacityReservation'만 가능</span><span class="sxs-lookup"><span data-stu-id="0b43b-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="0b43b-129">-Tags</span><span class="sxs-lookup"><span data-stu-id="0b43b-129">-Tags</span></span>
<span data-ttu-id="0b43b-130">클러스터의 태그</span><span class="sxs-lookup"><span data-stu-id="0b43b-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="0b43b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b43b-131">-Confirm</span></span>
<span data-ttu-id="0b43b-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b43b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b43b-133">-WhatIf</span></span>
<span data-ttu-id="0b43b-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0b43b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b43b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b43b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b43b-136">CommonParameters</span></span>
<span data-ttu-id="0b43b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b43b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b43b-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b43b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b43b-139">입력</span><span class="sxs-lookup"><span data-stu-id="0b43b-139">INPUTS</span></span>

### <span data-ttu-id="0b43b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0b43b-140">System.String</span></span>

## <span data-ttu-id="0b43b-141">출력</span><span class="sxs-lookup"><span data-stu-id="0b43b-141">OUTPUTS</span></span>

### <span data-ttu-id="0b43b-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0b43b-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="0b43b-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b43b-143">NOTES</span></span>

## <span data-ttu-id="0b43b-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b43b-144">RELATED LINKS</span></span>
