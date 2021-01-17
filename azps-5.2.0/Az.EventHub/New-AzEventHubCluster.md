---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323994"
---
# <span data-ttu-id="d376a-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="d376a-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="d376a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d376a-102">SYNOPSIS</span></span>
<span data-ttu-id="d376a-103">새 전용 eventhub 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="d376a-104">구문</span><span class="sxs-lookup"><span data-stu-id="d376a-104">SYNTAX</span></span>

### <span data-ttu-id="d376a-105">ClusterPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d376a-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d376a-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d376a-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d376a-107">설명</span><span class="sxs-lookup"><span data-stu-id="d376a-107">DESCRIPTION</span></span>
<span data-ttu-id="d376a-108">New-AzEventHubCluster cmdlet은 주어진 리소스 그룹에 전용 eventhub 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="d376a-109">예제</span><span class="sxs-lookup"><span data-stu-id="d376a-109">EXAMPLES</span></span>

### <span data-ttu-id="d376a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d376a-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="d376a-111">위치 southcentralus 및 용량이 1인 리소스 그룹 'RSG-Cluster27651'에 'Eventhub-Cluster-5557' 전용 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="d376a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d376a-112">PARAMETERS</span></span>

### <span data-ttu-id="d376a-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="d376a-113">-Capacity</span></span>
<span data-ttu-id="d376a-114">CU(클러스터 용량), curerntrly, 허용되는 값 = 1</span><span class="sxs-lookup"><span data-stu-id="d376a-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="d376a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d376a-115">-DefaultProfile</span></span>
<span data-ttu-id="d376a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d376a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d376a-117">-Location</span></span>
<span data-ttu-id="d376a-118">클러스터의 위치</span><span class="sxs-lookup"><span data-stu-id="d376a-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d376a-119">-Name</span></span>
<span data-ttu-id="d376a-120">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="d376a-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d376a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d376a-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d376a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d376a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d376a-123">-ResourceId</span></span>
<span data-ttu-id="d376a-124">클러스터의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d376a-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="d376a-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d376a-125">-Tag</span></span>
<span data-ttu-id="d376a-126">클러스터에 대한 리소스 태그를 나타내는 해시테이블</span><span class="sxs-lookup"><span data-stu-id="d376a-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d376a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d376a-127">-Confirm</span></span>
<span data-ttu-id="d376a-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d376a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d376a-129">-WhatIf</span></span>
<span data-ttu-id="d376a-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d376a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d376a-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d376a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d376a-132">CommonParameters</span></span>
<span data-ttu-id="d376a-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d376a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d376a-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d376a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d376a-135">입력</span><span class="sxs-lookup"><span data-stu-id="d376a-135">INPUTS</span></span>

### <span data-ttu-id="d376a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d376a-136">System.String</span></span>

### <span data-ttu-id="d376a-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d376a-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d376a-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d376a-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d376a-139">출력</span><span class="sxs-lookup"><span data-stu-id="d376a-139">OUTPUTS</span></span>

### <span data-ttu-id="d376a-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="d376a-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="d376a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d376a-141">NOTES</span></span>

## <span data-ttu-id="d376a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d376a-142">RELATED LINKS</span></span>
