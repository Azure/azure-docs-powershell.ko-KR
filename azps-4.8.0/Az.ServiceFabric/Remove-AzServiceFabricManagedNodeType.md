---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213306"
---
# <span data-ttu-id="a8ada-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a8ada-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="a8ada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ada-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ada-103">노드 형식 또는 노드 형식 내의 특정 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="a8ada-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8ada-104">SYNTAX</span></span>

### <span data-ttu-id="a8ada-105">DeleteNodeTypeByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8ada-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ada-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="a8ada-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ada-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="a8ada-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ada-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="a8ada-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8ada-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="a8ada-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ada-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="a8ada-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ada-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a8ada-111">DESCRIPTION</span></span>
<span data-ttu-id="a8ada-112">노드 형식 또는 노드 형식 내의 특정 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="a8ada-113">Paremter를 사용 하는 경우에는 지정 된 노드만 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="a8ada-114">예제의</span><span class="sxs-lookup"><span data-stu-id="a8ada-114">EXAMPLES</span></span>

### <span data-ttu-id="a8ada-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8ada-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="a8ada-116">노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-116">Remove node type.</span></span>

### <span data-ttu-id="a8ada-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="a8ada-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="a8ada-118">파이프를 사용 하 여 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="a8ada-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="a8ada-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="a8ada-120">노드 형식에서 노드 2 개를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="a8ada-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="a8ada-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="a8ada-122">노드 형식에서 파이프를 사용 하 여 노드 2 개를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="a8ada-123">변수</span><span class="sxs-lookup"><span data-stu-id="a8ada-123">PARAMETERS</span></span>

### <span data-ttu-id="a8ada-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ada-124">-AsJob</span></span>
<span data-ttu-id="a8ada-125">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a8ada-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a8ada-126">-ClusterName</span></span>
<span data-ttu-id="a8ada-127">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ada-128">-DefaultProfile</span></span>
<span data-ttu-id="a8ada-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ada-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="a8ada-130">-ForceRemoveNode</span></span>
<span data-ttu-id="a8ada-131">이 플래그를 사용 하면 서비스 패브릭이 노드를 사용 하지 않도록 설정할 수 없는 경우에도 강제로 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="a8ada-132">이로 인해 상태 저장 작업이 노드에서 실행 되는 경우 데이터가 손실 될 수 있으므로 주의를 기울여야 하며, op(부하) 후에 시드 노드가 부족 한 경우 클러스터를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ada-133">-InputObject</span></span>
<span data-ttu-id="a8ada-134">노드 형식 리소스</span><span class="sxs-lookup"><span data-stu-id="a8ada-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-135">-이름</span><span class="sxs-lookup"><span data-stu-id="a8ada-135">-Name</span></span>
<span data-ttu-id="a8ada-136">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a8ada-137">-NodeName</span></span>
<span data-ttu-id="a8ada-138">작업의 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ada-139">-PassThru</span></span>
<span data-ttu-id="a8ada-140">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a8ada-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a8ada-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ada-141">-ResourceGroupName</span></span>
<span data-ttu-id="a8ada-142">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ada-143">-ResourceId</span></span>
<span data-ttu-id="a8ada-144">노드 형식 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a8ada-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ada-145">-확인</span><span class="sxs-lookup"><span data-stu-id="a8ada-145">-Confirm</span></span>
<span data-ttu-id="a8ada-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ada-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ada-147">-WhatIf</span></span>
<span data-ttu-id="a8ada-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ada-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ada-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ada-150">CommonParameters</span></span>
<span data-ttu-id="a8ada-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8ada-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ada-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8ada-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ada-153">입력</span><span class="sxs-lookup"><span data-stu-id="a8ada-153">INPUTS</span></span>

### <span data-ttu-id="a8ada-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a8ada-154">System.String</span></span>

## <span data-ttu-id="a8ada-155">출력</span><span class="sxs-lookup"><span data-stu-id="a8ada-155">OUTPUTS</span></span>

### <span data-ttu-id="a8ada-156">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a8ada-156">System.Boolean</span></span>

## <span data-ttu-id="a8ada-157">상속자</span><span class="sxs-lookup"><span data-stu-id="a8ada-157">NOTES</span></span>

## <span data-ttu-id="a8ada-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8ada-158">RELATED LINKS</span></span>
