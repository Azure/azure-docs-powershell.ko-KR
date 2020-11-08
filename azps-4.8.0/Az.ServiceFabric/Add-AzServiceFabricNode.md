---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204848"
---
# <span data-ttu-id="7430a-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7430a-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="7430a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7430a-102">SYNOPSIS</span></span>
<span data-ttu-id="7430a-103">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="7430a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7430a-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7430a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7430a-105">DESCRIPTION</span></span>
<span data-ttu-id="7430a-106">**Add-AzServiceFabricNode** 를 사용 하 여 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="7430a-107">노드 형식에 추가 하려는 노드 수를 지정 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="7430a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7430a-108">EXAMPLES</span></span>

### <span data-ttu-id="7430a-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7430a-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="7430a-110">이 명령은 노드 형식 ' n1 '에 2 개의 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="7430a-111">변수</span><span class="sxs-lookup"><span data-stu-id="7430a-111">PARAMETERS</span></span>

### <span data-ttu-id="7430a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7430a-112">-DefaultProfile</span></span>
<span data-ttu-id="7430a-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7430a-114">-이름</span><span class="sxs-lookup"><span data-stu-id="7430a-114">-Name</span></span>
<span data-ttu-id="7430a-115">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="7430a-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="7430a-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7430a-116">-NodeType</span></span>
<span data-ttu-id="7430a-117">노드 형식 이름</span><span class="sxs-lookup"><span data-stu-id="7430a-117">Node type name</span></span>

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

### <span data-ttu-id="7430a-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="7430a-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="7430a-119">추가할 노드 수</span><span class="sxs-lookup"><span data-stu-id="7430a-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="7430a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7430a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7430a-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7430a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="7430a-122">-Confirm</span></span>
<span data-ttu-id="7430a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7430a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7430a-124">-WhatIf</span></span>
<span data-ttu-id="7430a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7430a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7430a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7430a-127">CommonParameters</span></span>
<span data-ttu-id="7430a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7430a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7430a-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7430a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7430a-130">입력</span><span class="sxs-lookup"><span data-stu-id="7430a-130">INPUTS</span></span>

### <span data-ttu-id="7430a-131">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7430a-131">System.Int32</span></span>

### <span data-ttu-id="7430a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7430a-132">System.String</span></span>

## <span data-ttu-id="7430a-133">출력</span><span class="sxs-lookup"><span data-stu-id="7430a-133">OUTPUTS</span></span>

### <span data-ttu-id="7430a-134">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="7430a-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7430a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7430a-135">NOTES</span></span>

## <span data-ttu-id="7430a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7430a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7430a-137">제거-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7430a-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
