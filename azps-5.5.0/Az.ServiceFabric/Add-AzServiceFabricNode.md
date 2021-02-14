---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208093"
---
# <span data-ttu-id="760c4-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="760c4-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="760c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="760c4-102">SYNOPSIS</span></span>
<span data-ttu-id="760c4-103">클러스터의 특정 노드 유형에 노드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="760c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="760c4-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="760c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="760c4-105">DESCRIPTION</span></span>
<span data-ttu-id="760c4-106">**Add-AzServiceFabricNode를** 사용하여 특정 노드 유형에 노드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="760c4-107">노드 유형에 추가하려는 노드 수만 지정하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="760c4-108">예제</span><span class="sxs-lookup"><span data-stu-id="760c4-108">EXAMPLES</span></span>

### <span data-ttu-id="760c4-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="760c4-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="760c4-110">이 명령은 노드 형식 'n1'에 2개 노드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="760c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="760c4-111">PARAMETERS</span></span>

### <span data-ttu-id="760c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760c4-112">-DefaultProfile</span></span>
<span data-ttu-id="760c4-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760c4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="760c4-114">-Name</span></span>
<span data-ttu-id="760c4-115">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="760c4-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="760c4-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="760c4-116">-NodeType</span></span>
<span data-ttu-id="760c4-117">노드 유형 이름</span><span class="sxs-lookup"><span data-stu-id="760c4-117">Node type name</span></span>

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

### <span data-ttu-id="760c4-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="760c4-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="760c4-119">추가할 노드 수</span><span class="sxs-lookup"><span data-stu-id="760c4-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="760c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="760c4-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="760c4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="760c4-122">-Confirm</span></span>
<span data-ttu-id="760c4-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="760c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="760c4-124">-WhatIf</span></span>
<span data-ttu-id="760c4-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="760c4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="760c4-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="760c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760c4-127">CommonParameters</span></span>
<span data-ttu-id="760c4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="760c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760c4-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="760c4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760c4-130">입력</span><span class="sxs-lookup"><span data-stu-id="760c4-130">INPUTS</span></span>

### <span data-ttu-id="760c4-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="760c4-131">System.Int32</span></span>

### <span data-ttu-id="760c4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="760c4-132">System.String</span></span>

## <span data-ttu-id="760c4-133">출력</span><span class="sxs-lookup"><span data-stu-id="760c4-133">OUTPUTS</span></span>

### <span data-ttu-id="760c4-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="760c4-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="760c4-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="760c4-135">NOTES</span></span>

## <span data-ttu-id="760c4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="760c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="760c4-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="760c4-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
