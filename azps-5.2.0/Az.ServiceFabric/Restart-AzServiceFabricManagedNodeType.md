---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330501"
---
# <span data-ttu-id="5bc3c-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5bc3c-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="5bc3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc3c-103">노드 형식에서 특정 노드를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="5bc3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bc3c-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bc3c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5bc3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc3c-106">노드 형식에서 특정 노드를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="5bc3c-107">VM을 다시 시작하기 전에 서비스 패브릭 노드를 사용하지 않도록 설정하고 다시 돌아오면 다시 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="5bc3c-108">주 노드 유형에서 이 작업을 수행하면 모든 노드를 동시에 다시 시작하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="5bc3c-109">서비스 패브릭이 노드를 비활성화할 수 없지만 상태 저장 워크로드가 노드에서 실행되는 경우 데이터 손실이 발생할 수 있는 경우에도 -ForceRestart를 사용하여 작업을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="5bc3c-110">예제</span><span class="sxs-lookup"><span data-stu-id="5bc3c-110">EXAMPLES</span></span>

### <span data-ttu-id="5bc3c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bc3c-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="5bc3c-112">노드 형식에서 노드 0 및 3을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="5bc3c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bc3c-113">PARAMETERS</span></span>

### <span data-ttu-id="5bc3c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bc3c-114">-AsJob</span></span>
<span data-ttu-id="5bc3c-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5bc3c-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5bc3c-116">-ClusterName</span></span>
<span data-ttu-id="5bc3c-117">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5bc3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc3c-118">-DefaultProfile</span></span>
<span data-ttu-id="5bc3c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc3c-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="5bc3c-120">-ForceRestart</span></span>
<span data-ttu-id="5bc3c-121">서비스 패브릭이 노드를 사용하지 않도록 설정할 수 없는 경우에도 이 플래그를 사용하여 노드를 강제로 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="5bc3c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5bc3c-122">-Name</span></span>
<span data-ttu-id="5bc3c-123">노드 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc3c-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="5bc3c-124">-NodeName</span></span>
<span data-ttu-id="5bc3c-125">작업에 대한 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc3c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bc3c-126">-PassThru</span></span>
<span data-ttu-id="5bc3c-127">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="5bc3c-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5bc3c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc3c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5bc3c-129">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc3c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bc3c-130">-Confirm</span></span>
<span data-ttu-id="5bc3c-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc3c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc3c-132">-WhatIf</span></span>
<span data-ttu-id="5bc3c-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5bc3c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc3c-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc3c-135">CommonParameters</span></span>
<span data-ttu-id="5bc3c-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc3c-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bc3c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc3c-138">입력</span><span class="sxs-lookup"><span data-stu-id="5bc3c-138">INPUTS</span></span>

### <span data-ttu-id="5bc3c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc3c-139">System.String</span></span>

## <span data-ttu-id="5bc3c-140">출력</span><span class="sxs-lookup"><span data-stu-id="5bc3c-140">OUTPUTS</span></span>

### <span data-ttu-id="5bc3c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5bc3c-141">System.Boolean</span></span>

## <span data-ttu-id="5bc3c-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bc3c-142">NOTES</span></span>

## <span data-ttu-id="5bc3c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bc3c-143">RELATED LINKS</span></span>
