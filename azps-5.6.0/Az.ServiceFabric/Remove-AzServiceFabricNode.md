---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005435"
---
# <span data-ttu-id="bfb6d-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="bfb6d-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="bfb6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfb6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb6d-103">클러스터에서 특정 노드 유형에서 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="bfb6d-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfb6d-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfb6d-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfb6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bfb6d-106">**Remove-AzServiceFabricNode를** 사용하여 클러스터에서 특정 노드 유형에서 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="bfb6d-107">제거는 클러스터 상태 메트릭을 충족하는 경우만 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="bfb6d-108">예제</span><span class="sxs-lookup"><span data-stu-id="bfb6d-108">EXAMPLES</span></span>

### <span data-ttu-id="bfb6d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfb6d-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="bfb6d-110">이 명령은 NodeType 'nt1'에서 2개 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="bfb6d-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfb6d-111">PARAMETERS</span></span>

### <span data-ttu-id="bfb6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb6d-112">-DefaultProfile</span></span>
<span data-ttu-id="bfb6d-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfb6d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bfb6d-114">-Name</span></span>
<span data-ttu-id="bfb6d-115">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="bfb6d-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb6d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bfb6d-116">-NodeType</span></span>
<span data-ttu-id="bfb6d-117">노드 형식 이름</span><span class="sxs-lookup"><span data-stu-id="bfb6d-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb6d-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="bfb6d-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="bfb6d-119">추가할 노드 수</span><span class="sxs-lookup"><span data-stu-id="bfb6d-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb6d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfb6d-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfb6d-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bfb6d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="bfb6d-122">-Confirm</span></span>
<span data-ttu-id="bfb6d-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfb6d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfb6d-124">-WhatIf</span></span>
<span data-ttu-id="bfb6d-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfb6d-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfb6d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb6d-127">CommonParameters</span></span>
<span data-ttu-id="bfb6d-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfb6d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb6d-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfb6d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb6d-130">입력</span><span class="sxs-lookup"><span data-stu-id="bfb6d-130">INPUTS</span></span>

### <span data-ttu-id="bfb6d-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="bfb6d-131">System.Int32</span></span>

### <span data-ttu-id="bfb6d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bfb6d-132">System.String</span></span>

## <span data-ttu-id="bfb6d-133">출력</span><span class="sxs-lookup"><span data-stu-id="bfb6d-133">OUTPUTS</span></span>

### <span data-ttu-id="bfb6d-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="bfb6d-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bfb6d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfb6d-135">NOTES</span></span>

## <span data-ttu-id="bfb6d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfb6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="bfb6d-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="bfb6d-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
