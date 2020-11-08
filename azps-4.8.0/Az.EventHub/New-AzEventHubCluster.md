---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212238"
---
# <span data-ttu-id="e09d6-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="e09d6-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="e09d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09d6-102">SYNOPSIS</span></span>
<span data-ttu-id="e09d6-103">새 전용 eventhub 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="e09d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e09d6-104">SYNTAX</span></span>

### <span data-ttu-id="e09d6-105">Cluster속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e09d6-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e09d6-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e09d6-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e09d6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e09d6-107">DESCRIPTION</span></span>
<span data-ttu-id="e09d6-108">New-AzEventHubCluster cmdlet은 지정 된 리소스 그룹에 전용 eventhub 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="e09d6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e09d6-109">EXAMPLES</span></span>

### <span data-ttu-id="e09d6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e09d6-110">Example 1</span></span>
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

<span data-ttu-id="e09d6-111">위치 southcentralus와 용량을 1로 하 여 resourcegroup ' RSG-Cluster27651 ' 전용 클러스터에 ' Eventhub-클러스터-5557 ' 전용 클러스터가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="e09d6-112">변수</span><span class="sxs-lookup"><span data-stu-id="e09d6-112">PARAMETERS</span></span>

### <span data-ttu-id="e09d6-113">용량</span><span class="sxs-lookup"><span data-stu-id="e09d6-113">-Capacity</span></span>
<span data-ttu-id="e09d6-114">클러스터 용량 (CU (), curerntrly, 허용 값 = 1</span><span class="sxs-lookup"><span data-stu-id="e09d6-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="e09d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09d6-115">-DefaultProfile</span></span>
<span data-ttu-id="e09d6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e09d6-117">-위치</span><span class="sxs-lookup"><span data-stu-id="e09d6-117">-Location</span></span>
<span data-ttu-id="e09d6-118">클러스터 위치</span><span class="sxs-lookup"><span data-stu-id="e09d6-118">Location of Cluster</span></span>

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

### <span data-ttu-id="e09d6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e09d6-119">-Name</span></span>
<span data-ttu-id="e09d6-120">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="e09d6-120">Cluster Name</span></span>

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

### <span data-ttu-id="e09d6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09d6-121">-ResourceGroupName</span></span>
<span data-ttu-id="e09d6-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e09d6-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e09d6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e09d6-123">-ResourceId</span></span>
<span data-ttu-id="e09d6-124">클러스터의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e09d6-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="e09d6-125">태그</span><span class="sxs-lookup"><span data-stu-id="e09d6-125">-Tag</span></span>
<span data-ttu-id="e09d6-126">클러스터의 리소스 태그를 나타내는 Hashtables</span><span class="sxs-lookup"><span data-stu-id="e09d6-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="e09d6-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e09d6-127">-Confirm</span></span>
<span data-ttu-id="e09d6-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e09d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e09d6-129">-WhatIf</span></span>
<span data-ttu-id="e09d6-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e09d6-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e09d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09d6-132">CommonParameters</span></span>
<span data-ttu-id="e09d6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e09d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09d6-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e09d6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09d6-135">입력</span><span class="sxs-lookup"><span data-stu-id="e09d6-135">INPUTS</span></span>

### <span data-ttu-id="e09d6-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e09d6-136">System.String</span></span>

### <span data-ttu-id="e09d6-137">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="e09d6-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e09d6-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e09d6-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e09d6-139">출력</span><span class="sxs-lookup"><span data-stu-id="e09d6-139">OUTPUTS</span></span>

### <span data-ttu-id="e09d6-140">PSEventHubClusterAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="e09d6-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="e09d6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e09d6-141">NOTES</span></span>

## <span data-ttu-id="e09d6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e09d6-142">RELATED LINKS</span></span>
