---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329244"
---
# <span data-ttu-id="4e72c-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="4e72c-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="4e72c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e72c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e72c-103">주어진 클러스터에 대한 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="4e72c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e72c-104">SYNTAX</span></span>

### <span data-ttu-id="4e72c-105">ClusterPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4e72c-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e72c-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e72c-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e72c-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e72c-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e72c-108">설명</span><span class="sxs-lookup"><span data-stu-id="4e72c-108">DESCRIPTION</span></span>
<span data-ttu-id="4e72c-109">이 Set-AzEventHubCluster cmdlet은 주어진 클러스터의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="4e72c-110">예제</span><span class="sxs-lookup"><span data-stu-id="4e72c-110">EXAMPLES</span></span>

### <span data-ttu-id="4e72c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e72c-111">Example 1</span></span>
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

<span data-ttu-id="4e72c-112">주어진 클러스터의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="4e72c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e72c-113">PARAMETERS</span></span>

### <span data-ttu-id="4e72c-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="4e72c-114">-Capacity</span></span>
<span data-ttu-id="4e72c-115">CU(클러스터 용량), curerntrly, 허용되는 값 = 1</span><span class="sxs-lookup"><span data-stu-id="4e72c-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="4e72c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e72c-116">-DefaultProfile</span></span>
<span data-ttu-id="4e72c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e72c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e72c-118">-InputObject</span></span>
<span data-ttu-id="4e72c-119">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="4e72c-119">Cluster Name</span></span>

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

### <span data-ttu-id="4e72c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="4e72c-120">-Location</span></span>
<span data-ttu-id="4e72c-121">클러스터의 위치</span><span class="sxs-lookup"><span data-stu-id="4e72c-121">Location of Cluster</span></span>

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

### <span data-ttu-id="4e72c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4e72c-122">-Name</span></span>
<span data-ttu-id="4e72c-123">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="4e72c-123">Cluster Name</span></span>

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

### <span data-ttu-id="4e72c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e72c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e72c-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4e72c-125">Resource Group Name</span></span>

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

### <span data-ttu-id="4e72c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e72c-126">-ResourceId</span></span>
<span data-ttu-id="4e72c-127">클러스터의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4e72c-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="4e72c-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e72c-128">-Tag</span></span>
<span data-ttu-id="4e72c-129">클러스터에 대한 리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="4e72c-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="4e72c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e72c-130">-Confirm</span></span>
<span data-ttu-id="4e72c-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e72c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e72c-132">-WhatIf</span></span>
<span data-ttu-id="4e72c-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e72c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e72c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e72c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e72c-135">CommonParameters</span></span>
<span data-ttu-id="4e72c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e72c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e72c-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e72c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e72c-138">입력</span><span class="sxs-lookup"><span data-stu-id="4e72c-138">INPUTS</span></span>

### <span data-ttu-id="4e72c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4e72c-139">System.String</span></span>

### <span data-ttu-id="4e72c-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4e72c-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4e72c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="4e72c-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="4e72c-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4e72c-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4e72c-143">출력</span><span class="sxs-lookup"><span data-stu-id="4e72c-143">OUTPUTS</span></span>

### <span data-ttu-id="4e72c-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="4e72c-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="4e72c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e72c-145">NOTES</span></span>

## <span data-ttu-id="4e72c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e72c-146">RELATED LINKS</span></span>
