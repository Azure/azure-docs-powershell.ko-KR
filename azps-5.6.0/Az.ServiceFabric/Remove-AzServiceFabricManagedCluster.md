---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: a9e3f5f8305733329f7ff9e34eadde151d873c6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005499"
---
# <span data-ttu-id="4f6b3-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="4f6b3-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="4f6b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6b3-103">클러스터 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-103">Remove cluster resource.</span></span>

## <span data-ttu-id="4f6b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f6b3-104">SYNTAX</span></span>

### <span data-ttu-id="4f6b3-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="4f6b3-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6b3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4f6b3-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6b3-107">ById</span><span class="sxs-lookup"><span data-stu-id="4f6b3-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f6b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="4f6b3-108">DESCRIPTION</span></span>
<span data-ttu-id="4f6b3-109">클러스터를 제거하면 클러스터 아래 노드 형식도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="4f6b3-110">예제</span><span class="sxs-lookup"><span data-stu-id="4f6b3-110">EXAMPLES</span></span>

### <span data-ttu-id="4f6b3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f6b3-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="4f6b3-112">클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-112">Remove cluster.</span></span>

### <span data-ttu-id="4f6b3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4f6b3-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="4f6b3-114">배관을 사용하여 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="4f6b3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4f6b3-115">PARAMETERS</span></span>

### <span data-ttu-id="4f6b3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f6b3-116">-AsJob</span></span>
<span data-ttu-id="4f6b3-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6b3-118">-DefaultProfile</span></span>
<span data-ttu-id="4f6b3-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f6b3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f6b3-120">-InputObject</span></span>
<span data-ttu-id="4f6b3-121">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="4f6b3-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4f6b3-122">-Name</span></span>
<span data-ttu-id="4f6b3-123">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f6b3-124">-PassThru</span></span>
<span data-ttu-id="4f6b3-125">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="4f6b3-125">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f6b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="4f6b3-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f6b3-128">-ResourceId</span></span>
<span data-ttu-id="4f6b3-129">관리되는 클러스터 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4f6b3-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6b3-130">-확인</span><span class="sxs-lookup"><span data-stu-id="4f6b3-130">-Confirm</span></span>
<span data-ttu-id="4f6b3-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f6b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f6b3-132">-WhatIf</span></span>
<span data-ttu-id="4f6b3-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f6b3-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f6b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6b3-135">CommonParameters</span></span>
<span data-ttu-id="4f6b3-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f6b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6b3-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f6b3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6b3-138">입력</span><span class="sxs-lookup"><span data-stu-id="4f6b3-138">INPUTS</span></span>

### <span data-ttu-id="4f6b3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4f6b3-139">System.String</span></span>

## <span data-ttu-id="4f6b3-140">출력</span><span class="sxs-lookup"><span data-stu-id="4f6b3-140">OUTPUTS</span></span>

### <span data-ttu-id="4f6b3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f6b3-141">System.Boolean</span></span>

## <span data-ttu-id="4f6b3-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f6b3-142">NOTES</span></span>

## <span data-ttu-id="4f6b3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f6b3-143">RELATED LINKS</span></span>
