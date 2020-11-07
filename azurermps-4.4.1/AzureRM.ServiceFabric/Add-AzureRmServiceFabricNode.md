---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703615"
---
# <span data-ttu-id="43b67-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="43b67-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="43b67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43b67-102">SYNOPSIS</span></span>
<span data-ttu-id="43b67-103">클러스터의 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43b67-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43b67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="43b67-105">DESCRIPTION</span></span>
<span data-ttu-id="43b67-106">**Add-AzureRmServiceFabricNode** 를 사용 하 여 특정 노드 형식에 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="43b67-107">노드 형식에 추가 하려는 노드 수를 지정 하기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="43b67-108">예제의</span><span class="sxs-lookup"><span data-stu-id="43b67-108">EXAMPLES</span></span>

### <span data-ttu-id="43b67-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="43b67-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="43b67-110">이 명령은 노드 형식 ' n1 '에 2 개의 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="43b67-111">변수</span><span class="sxs-lookup"><span data-stu-id="43b67-111">PARAMETERS</span></span>

### <span data-ttu-id="43b67-112">-이름</span><span class="sxs-lookup"><span data-stu-id="43b67-112">-Name</span></span>
<span data-ttu-id="43b67-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="43b67-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="43b67-114">-NodeType</span></span>
<span data-ttu-id="43b67-115">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-115">Node type name.</span></span>

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

### <span data-ttu-id="43b67-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="43b67-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="43b67-117">VM 인스턴스 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-117">VM instance number.</span></span>

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

### <span data-ttu-id="43b67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b67-118">-ResourceGroupName</span></span>
<span data-ttu-id="43b67-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="43b67-120">-확인</span><span class="sxs-lookup"><span data-stu-id="43b67-120">-Confirm</span></span>
<span data-ttu-id="43b67-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b67-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b67-122">-WhatIf</span></span>
<span data-ttu-id="43b67-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43b67-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b67-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b67-125">-DefaultProfile</span></span>
<span data-ttu-id="43b67-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b67-127">CommonParameters</span></span>
<span data-ttu-id="43b67-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43b67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b67-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b67-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b67-130">입력</span><span class="sxs-lookup"><span data-stu-id="43b67-130">INPUTS</span></span>

### <span data-ttu-id="43b67-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="43b67-131">System.String</span></span>

## <span data-ttu-id="43b67-132">출력</span><span class="sxs-lookup"><span data-stu-id="43b67-132">OUTPUTS</span></span>

### <span data-ttu-id="43b67-133">System. 개체</span><span class="sxs-lookup"><span data-stu-id="43b67-133">System.Object</span></span>

## <span data-ttu-id="43b67-134">상속자</span><span class="sxs-lookup"><span data-stu-id="43b67-134">NOTES</span></span>

## <span data-ttu-id="43b67-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43b67-135">RELATED LINKS</span></span>

[<span data-ttu-id="43b67-136">제거-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="43b67-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
