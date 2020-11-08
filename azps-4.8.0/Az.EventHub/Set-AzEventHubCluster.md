---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212777"
---
# <span data-ttu-id="3ae9e-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="3ae9e-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="3ae9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae9e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae9e-103">지정 된 클러스터의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="3ae9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ae9e-104">SYNTAX</span></span>

### <span data-ttu-id="3ae9e-105">Cluster속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ae9e-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ae9e-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ae9e-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ae9e-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ae9e-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae9e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3ae9e-108">DESCRIPTION</span></span>
<span data-ttu-id="3ae9e-109">Set-AzEventHubCluster cmdlet은 지정 된 클러스터의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="3ae9e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3ae9e-110">EXAMPLES</span></span>

### <span data-ttu-id="3ae9e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ae9e-111">Example 1</span></span>
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

<span data-ttu-id="3ae9e-112">지정 된 클러스터의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="3ae9e-113">변수</span><span class="sxs-lookup"><span data-stu-id="3ae9e-113">PARAMETERS</span></span>

### <span data-ttu-id="3ae9e-114">용량</span><span class="sxs-lookup"><span data-stu-id="3ae9e-114">-Capacity</span></span>
<span data-ttu-id="3ae9e-115">클러스터 용량 (CU (), curerntrly, 허용 값 = 1</span><span class="sxs-lookup"><span data-stu-id="3ae9e-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="3ae9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae9e-116">-DefaultProfile</span></span>
<span data-ttu-id="3ae9e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae9e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ae9e-118">-InputObject</span></span>
<span data-ttu-id="3ae9e-119">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="3ae9e-119">Cluster Name</span></span>

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

### <span data-ttu-id="3ae9e-120">-위치</span><span class="sxs-lookup"><span data-stu-id="3ae9e-120">-Location</span></span>
<span data-ttu-id="3ae9e-121">클러스터 위치</span><span class="sxs-lookup"><span data-stu-id="3ae9e-121">Location of Cluster</span></span>

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

### <span data-ttu-id="3ae9e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3ae9e-122">-Name</span></span>
<span data-ttu-id="3ae9e-123">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="3ae9e-123">Cluster Name</span></span>

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

### <span data-ttu-id="3ae9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ae9e-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ae9e-125">Resource Group Name</span></span>

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

### <span data-ttu-id="3ae9e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ae9e-126">-ResourceId</span></span>
<span data-ttu-id="3ae9e-127">클러스터의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3ae9e-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="3ae9e-128">태그</span><span class="sxs-lookup"><span data-stu-id="3ae9e-128">-Tag</span></span>
<span data-ttu-id="3ae9e-129">클러스터에 대 한 리소스 태그를 나타내는 Hashtables</span><span class="sxs-lookup"><span data-stu-id="3ae9e-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="3ae9e-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3ae9e-130">-Confirm</span></span>
<span data-ttu-id="3ae9e-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae9e-132">-WhatIf</span></span>
<span data-ttu-id="3ae9e-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae9e-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae9e-135">CommonParameters</span></span>
<span data-ttu-id="3ae9e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae9e-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ae9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae9e-138">입력</span><span class="sxs-lookup"><span data-stu-id="3ae9e-138">INPUTS</span></span>

### <span data-ttu-id="3ae9e-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ae9e-139">System.String</span></span>

### <span data-ttu-id="3ae9e-140">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="3ae9e-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="3ae9e-141">PSEventHubClusterAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="3ae9e-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="3ae9e-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3ae9e-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3ae9e-143">출력</span><span class="sxs-lookup"><span data-stu-id="3ae9e-143">OUTPUTS</span></span>

### <span data-ttu-id="3ae9e-144">PSEventHubClusterAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="3ae9e-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="3ae9e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3ae9e-145">NOTES</span></span>

## <span data-ttu-id="3ae9e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ae9e-146">RELATED LINKS</span></span>
