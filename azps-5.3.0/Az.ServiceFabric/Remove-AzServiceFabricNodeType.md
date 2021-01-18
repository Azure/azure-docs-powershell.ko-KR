---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494746"
---
# <span data-ttu-id="e7d66-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e7d66-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="e7d66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d66-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d66-103">클러스터에서 전체 노드 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="e7d66-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7d66-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d66-105">설명</span><span class="sxs-lookup"><span data-stu-id="e7d66-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d66-106">**Remove-AzServiceFabricNodeType을** 사용하여 클러스터의 특정 노드 유형 및 노드 형식에서 모든 노드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="e7d66-107">이 명령은 주 노드 형식을 삭제하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="e7d66-108">예제</span><span class="sxs-lookup"><span data-stu-id="e7d66-108">EXAMPLES</span></span>

### <span data-ttu-id="e7d66-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7d66-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="e7d66-110">이 명령은 클러스터에서 NodeType 'nt1'을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="e7d66-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7d66-111">PARAMETERS</span></span>

### <span data-ttu-id="e7d66-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d66-112">-DefaultProfile</span></span>
<span data-ttu-id="e7d66-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d66-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d66-114">-Name</span></span>
<span data-ttu-id="e7d66-115">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="e7d66-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e7d66-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e7d66-116">-NodeType</span></span>
<span data-ttu-id="e7d66-117">노드 유형 이름</span><span class="sxs-lookup"><span data-stu-id="e7d66-117">The node type name</span></span>

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

### <span data-ttu-id="e7d66-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d66-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7d66-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e7d66-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d66-120">-Confirm</span></span>
<span data-ttu-id="e7d66-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d66-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d66-122">-WhatIf</span></span>
<span data-ttu-id="e7d66-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e7d66-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d66-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d66-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d66-125">CommonParameters</span></span>
<span data-ttu-id="e7d66-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7d66-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d66-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7d66-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d66-128">입력</span><span class="sxs-lookup"><span data-stu-id="e7d66-128">INPUTS</span></span>

### <span data-ttu-id="e7d66-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d66-129">System.String</span></span>

## <span data-ttu-id="e7d66-130">출력</span><span class="sxs-lookup"><span data-stu-id="e7d66-130">OUTPUTS</span></span>

### <span data-ttu-id="e7d66-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e7d66-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e7d66-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7d66-132">NOTES</span></span>

## <span data-ttu-id="e7d66-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7d66-133">RELATED LINKS</span></span>
