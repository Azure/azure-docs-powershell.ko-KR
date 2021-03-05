---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998326"
---
# <span data-ttu-id="e28e3-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="e28e3-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="e28e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e28e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e28e3-103">주어진 클러스터에 대한 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="e28e3-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="e28e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e28e3-104">SYNTAX</span></span>

### <span data-ttu-id="e28e3-105">ClusterPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e28e3-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e28e3-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e28e3-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e28e3-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e28e3-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e28e3-108">설명</span><span class="sxs-lookup"><span data-stu-id="e28e3-108">DESCRIPTION</span></span>
<span data-ttu-id="e28e3-109">Set-AzEventHubCluster cmdlet은 지정한 클러스터의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="e28e3-110">예제</span><span class="sxs-lookup"><span data-stu-id="e28e3-110">EXAMPLES</span></span>

### <span data-ttu-id="e28e3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e28e3-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="e28e3-112">주어진 클러스터의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="e28e3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e28e3-113">PARAMETERS</span></span>

### <span data-ttu-id="e28e3-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="e28e3-114">-Capacity</span></span>
<span data-ttu-id="e28e3-115">CU(클러스터 용량), curerntrly, 허용된 값 = 1</span><span class="sxs-lookup"><span data-stu-id="e28e3-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e28e3-116">-DefaultProfile</span></span>
<span data-ttu-id="e28e3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e28e3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e28e3-118">-InputObject</span></span>
<span data-ttu-id="e28e3-119">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="e28e3-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-120">-Location</span><span class="sxs-lookup"><span data-stu-id="e28e3-120">-Location</span></span>
<span data-ttu-id="e28e3-121">클러스터 위치</span><span class="sxs-lookup"><span data-stu-id="e28e3-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e28e3-122">-Name</span></span>
<span data-ttu-id="e28e3-123">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="e28e3-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e28e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e28e3-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e28e3-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e28e3-126">-ResourceId</span></span>
<span data-ttu-id="e28e3-127">클러스터의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e28e3-127">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="e28e3-128">-Tag</span></span>
<span data-ttu-id="e28e3-129">클러스터에 대한 리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="e28e3-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e28e3-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e28e3-130">-Confirm</span></span>
<span data-ttu-id="e28e3-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e28e3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e28e3-132">-WhatIf</span></span>
<span data-ttu-id="e28e3-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e28e3-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e28e3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e28e3-135">CommonParameters</span></span>
<span data-ttu-id="e28e3-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e28e3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e28e3-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e28e3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e28e3-138">입력</span><span class="sxs-lookup"><span data-stu-id="e28e3-138">INPUTS</span></span>

### <span data-ttu-id="e28e3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e28e3-139">System.String</span></span>

### <span data-ttu-id="e28e3-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e28e3-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e28e3-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="e28e3-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="e28e3-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e28e3-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e28e3-143">출력</span><span class="sxs-lookup"><span data-stu-id="e28e3-143">OUTPUTS</span></span>

### <span data-ttu-id="e28e3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="e28e3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="e28e3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e28e3-145">NOTES</span></span>

## <span data-ttu-id="e28e3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e28e3-146">RELATED LINKS</span></span>
