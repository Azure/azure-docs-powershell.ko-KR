---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535132"
---
# <span data-ttu-id="0888d-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0888d-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="0888d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0888d-102">SYNOPSIS</span></span>
<span data-ttu-id="0888d-103">클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0888d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0888d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0888d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0888d-105">DESCRIPTION</span></span>
<span data-ttu-id="0888d-106">**Remove-AzureRmServiceFabricNode** 를 사용 하 여 클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="0888d-107">클러스터 상태 메트릭을 충족 하는 경우에만 제거가 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="0888d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0888d-108">EXAMPLES</span></span>

### <span data-ttu-id="0888d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0888d-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="0888d-110">이 명령은 NodeType ' nt1 '에서 2 개의 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="0888d-111">변수</span><span class="sxs-lookup"><span data-stu-id="0888d-111">PARAMETERS</span></span>

### <span data-ttu-id="0888d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0888d-112">-DefaultProfile</span></span>
<span data-ttu-id="0888d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0888d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="0888d-114">-Name</span></span>
<span data-ttu-id="0888d-115">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0888d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0888d-116">-NodeType</span></span>
<span data-ttu-id="0888d-117">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-117">Node type name.</span></span>

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

### <span data-ttu-id="0888d-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="0888d-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="0888d-119">제거할 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="0888d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0888d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0888d-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0888d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0888d-122">-Confirm</span></span>
<span data-ttu-id="0888d-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0888d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0888d-124">-WhatIf</span></span>
<span data-ttu-id="0888d-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0888d-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0888d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0888d-127">CommonParameters</span></span>
<span data-ttu-id="0888d-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0888d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0888d-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0888d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0888d-130">입력</span><span class="sxs-lookup"><span data-stu-id="0888d-130">INPUTS</span></span>

### <span data-ttu-id="0888d-131">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="0888d-131">System.Int32</span></span>
<span data-ttu-id="0888d-132">매개 변수: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0888d-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="0888d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0888d-133">System.String</span></span>
<span data-ttu-id="0888d-134">매개 변수: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0888d-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="0888d-135">출력</span><span class="sxs-lookup"><span data-stu-id="0888d-135">OUTPUTS</span></span>

### <span data-ttu-id="0888d-136">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="0888d-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0888d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0888d-137">NOTES</span></span>

## <span data-ttu-id="0888d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0888d-138">RELATED LINKS</span></span>

[<span data-ttu-id="0888d-139">추가-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0888d-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
