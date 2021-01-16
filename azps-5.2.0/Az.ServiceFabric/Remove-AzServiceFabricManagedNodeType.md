---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357939"
---
# <span data-ttu-id="d9b89-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d9b89-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="d9b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b89-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b89-103">노드 유형 내에서 노드 유형 또는 특정 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="d9b89-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9b89-104">SYNTAX</span></span>

### <span data-ttu-id="d9b89-105">DeleteNodeTypeByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9b89-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="d9b89-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="d9b89-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="d9b89-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9b89-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="d9b89-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9b89-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="d9b89-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b89-111">설명</span><span class="sxs-lookup"><span data-stu-id="d9b89-111">DESCRIPTION</span></span>
<span data-ttu-id="d9b89-112">노드 유형 내에서 노드 유형 또는 특정 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="d9b89-113">paremter -NodeName을 사용하는 경우 지정된 노드만 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="d9b89-114">예제</span><span class="sxs-lookup"><span data-stu-id="d9b89-114">EXAMPLES</span></span>

### <span data-ttu-id="d9b89-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9b89-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="d9b89-116">노드 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-116">Remove node type.</span></span>

### <span data-ttu-id="d9b89-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="d9b89-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="d9b89-118">파이핑을 사용하여 노드 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="d9b89-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="d9b89-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="d9b89-120">노드 유형에서 2개 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="d9b89-121">예제 4</span><span class="sxs-lookup"><span data-stu-id="d9b89-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="d9b89-122">파이핑을 사용하여 노드 유형에서 2개 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="d9b89-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9b89-123">PARAMETERS</span></span>

### <span data-ttu-id="d9b89-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9b89-124">-AsJob</span></span>
<span data-ttu-id="d9b89-125">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d9b89-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9b89-126">-ClusterName</span></span>
<span data-ttu-id="d9b89-127">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d9b89-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b89-128">-DefaultProfile</span></span>
<span data-ttu-id="d9b89-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b89-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="d9b89-130">-ForceRemoveNode</span></span>
<span data-ttu-id="d9b89-131">서비스 패브릭이 노드를 사용하지 않도록 설정할 수 없는 경우에도 이 플래그를 사용하여 제거를 강제합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="d9b89-132">상태 저장 워크로드가 노드에서 실행되는 경우 데이터 손실을 발생하거나 opearion 후 시드 노드가 충분하지 않은 경우 클러스터를 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="d9b89-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b89-133">-InputObject</span></span>
<span data-ttu-id="d9b89-134">노드 유형 리소스</span><span class="sxs-lookup"><span data-stu-id="d9b89-134">Node type resource</span></span>

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

### <span data-ttu-id="d9b89-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d9b89-135">-Name</span></span>
<span data-ttu-id="d9b89-136">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="d9b89-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d9b89-137">-NodeName</span></span>
<span data-ttu-id="d9b89-138">작업에 대한 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="d9b89-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9b89-139">-PassThru</span></span>
<span data-ttu-id="d9b89-140">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="d9b89-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d9b89-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b89-141">-ResourceGroupName</span></span>
<span data-ttu-id="d9b89-142">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d9b89-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9b89-143">-ResourceId</span></span>
<span data-ttu-id="d9b89-144">노드 유형 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d9b89-144">Node type resource id</span></span>

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

### <span data-ttu-id="d9b89-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b89-145">-Confirm</span></span>
<span data-ttu-id="d9b89-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b89-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b89-147">-WhatIf</span></span>
<span data-ttu-id="d9b89-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9b89-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b89-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b89-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b89-150">CommonParameters</span></span>
<span data-ttu-id="d9b89-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b89-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b89-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9b89-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b89-153">입력</span><span class="sxs-lookup"><span data-stu-id="d9b89-153">INPUTS</span></span>

### <span data-ttu-id="d9b89-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d9b89-154">System.String</span></span>

## <span data-ttu-id="d9b89-155">출력</span><span class="sxs-lookup"><span data-stu-id="d9b89-155">OUTPUTS</span></span>

### <span data-ttu-id="d9b89-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9b89-156">System.Boolean</span></span>

## <span data-ttu-id="d9b89-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9b89-157">NOTES</span></span>

## <span data-ttu-id="d9b89-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9b89-158">RELATED LINKS</span></span>
