---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702444"
---
# <span data-ttu-id="1236c-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1236c-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="1236c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1236c-102">SYNOPSIS</span></span>
<span data-ttu-id="1236c-103">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1236c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1236c-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1236c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1236c-105">DESCRIPTION</span></span>
<span data-ttu-id="1236c-106">**Add-AzureRmServiceFabricNode** 를 사용 하 여 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="1236c-107">노드 형식에 추가 하려는 노드 수를 지정 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="1236c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1236c-108">EXAMPLES</span></span>

### <span data-ttu-id="1236c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1236c-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="1236c-110">이 명령은 노드 형식 ' n1 '에 2 개의 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="1236c-111">변수</span><span class="sxs-lookup"><span data-stu-id="1236c-111">PARAMETERS</span></span>

### <span data-ttu-id="1236c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1236c-112">-DefaultProfile</span></span>
<span data-ttu-id="1236c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1236c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="1236c-114">-Name</span></span>
<span data-ttu-id="1236c-115">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1236c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1236c-116">-NodeType</span></span>
<span data-ttu-id="1236c-117">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-117">Node type name.</span></span>

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

### <span data-ttu-id="1236c-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="1236c-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="1236c-119">VM 인스턴스 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-119">VM instance number.</span></span>

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

### <span data-ttu-id="1236c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1236c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1236c-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1236c-122">-확인</span><span class="sxs-lookup"><span data-stu-id="1236c-122">-Confirm</span></span>
<span data-ttu-id="1236c-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1236c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1236c-124">-WhatIf</span></span>
<span data-ttu-id="1236c-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1236c-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1236c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1236c-127">CommonParameters</span></span>
<span data-ttu-id="1236c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1236c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1236c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1236c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1236c-130">입력</span><span class="sxs-lookup"><span data-stu-id="1236c-130">INPUTS</span></span>

### <span data-ttu-id="1236c-131">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="1236c-131">System.Int32</span></span>
<span data-ttu-id="1236c-132">매개 변수: NumberOfNodesToAdd (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1236c-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="1236c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1236c-133">System.String</span></span>
<span data-ttu-id="1236c-134">매개 변수: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1236c-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="1236c-135">출력</span><span class="sxs-lookup"><span data-stu-id="1236c-135">OUTPUTS</span></span>

### <span data-ttu-id="1236c-136">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="1236c-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1236c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1236c-137">NOTES</span></span>

## <span data-ttu-id="1236c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1236c-138">RELATED LINKS</span></span>

[<span data-ttu-id="1236c-139">제거-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="1236c-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
