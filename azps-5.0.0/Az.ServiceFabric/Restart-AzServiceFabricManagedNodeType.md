---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215853"
---
# <span data-ttu-id="6bdce-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6bdce-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="6bdce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdce-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdce-103">노드 형식에서 특정 노드를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="6bdce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6bdce-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bdce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6bdce-105">DESCRIPTION</span></span>
<span data-ttu-id="6bdce-106">노드 형식에서 특정 노드를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="6bdce-107">Vm을 다시 시작 하기 전에 service fabric 노드가 비활성화 되 고 다시 도착 하면 다시 다시 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="6bdce-108">기본 노드 형식에서이 작업을 수행 하는 경우에는 동시에 모든 노드를 다시 시작 하지 않을 수 있으므로 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="6bdce-109">Use-ForceRestart는 서비스 패브릭이 노드를 사용 하지 않도록 설정할 수 없지만,이로 인해 노드에서 상태 저장 작업이 실행 되는 경우 데이터가 손실 될 수 있으므로 주의 해 서 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="6bdce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6bdce-110">EXAMPLES</span></span>

### <span data-ttu-id="6bdce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6bdce-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="6bdce-112">노드 형식에서 노드 0 및 3을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="6bdce-113">변수</span><span class="sxs-lookup"><span data-stu-id="6bdce-113">PARAMETERS</span></span>

### <span data-ttu-id="6bdce-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bdce-114">-AsJob</span></span>
<span data-ttu-id="6bdce-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6bdce-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6bdce-116">-ClusterName</span></span>
<span data-ttu-id="6bdce-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6bdce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdce-118">-DefaultProfile</span></span>
<span data-ttu-id="6bdce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bdce-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="6bdce-120">-ForceRestart</span></span>
<span data-ttu-id="6bdce-121">이 플래그를 사용 하 여 서비스 패브릭이 노드를 사용 하지 않도록 설정할 수 없는 경우에도 노드가 다시 시작 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="6bdce-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6bdce-122">-Name</span></span>
<span data-ttu-id="6bdce-123">노드 형식의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="6bdce-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="6bdce-124">-NodeName</span></span>
<span data-ttu-id="6bdce-125">작업의 노드 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="6bdce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bdce-126">-PassThru</span></span>
<span data-ttu-id="6bdce-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="6bdce-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6bdce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bdce-128">-ResourceGroupName</span></span>
<span data-ttu-id="6bdce-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6bdce-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6bdce-130">-Confirm</span></span>
<span data-ttu-id="6bdce-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bdce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bdce-132">-WhatIf</span></span>
<span data-ttu-id="6bdce-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bdce-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bdce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdce-135">CommonParameters</span></span>
<span data-ttu-id="6bdce-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bdce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdce-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6bdce-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdce-138">입력</span><span class="sxs-lookup"><span data-stu-id="6bdce-138">INPUTS</span></span>

### <span data-ttu-id="6bdce-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6bdce-139">System.String</span></span>

## <span data-ttu-id="6bdce-140">출력</span><span class="sxs-lookup"><span data-stu-id="6bdce-140">OUTPUTS</span></span>

### <span data-ttu-id="6bdce-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6bdce-141">System.Boolean</span></span>

## <span data-ttu-id="6bdce-142">상속자</span><span class="sxs-lookup"><span data-stu-id="6bdce-142">NOTES</span></span>

## <span data-ttu-id="6bdce-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bdce-143">RELATED LINKS</span></span>
