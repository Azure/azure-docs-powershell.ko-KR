---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529132"
---
# <span data-ttu-id="01dbf-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="01dbf-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="01dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="01dbf-103">클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01dbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01dbf-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01dbf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="01dbf-106">**Remove-AzureRmServiceFabricNode** 를 사용 하 여 클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="01dbf-107">클러스터 상태 메트릭을 충족 하는 경우에만 제거가 진행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="01dbf-108">예제의</span><span class="sxs-lookup"><span data-stu-id="01dbf-108">EXAMPLES</span></span>

### <span data-ttu-id="01dbf-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="01dbf-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="01dbf-110">이 명령은 NodeType ' nt1 '에서 2 개의 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="01dbf-111">변수</span><span class="sxs-lookup"><span data-stu-id="01dbf-111">PARAMETERS</span></span>

### <span data-ttu-id="01dbf-112">-이름</span><span class="sxs-lookup"><span data-stu-id="01dbf-112">-Name</span></span>
<span data-ttu-id="01dbf-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="01dbf-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="01dbf-114">-NodeType</span></span>
<span data-ttu-id="01dbf-115">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-115">Node type name.</span></span>

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

### <span data-ttu-id="01dbf-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="01dbf-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="01dbf-117">제거할 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="01dbf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01dbf-118">-ResourceGroupName</span></span>
<span data-ttu-id="01dbf-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="01dbf-120">-확인</span><span class="sxs-lookup"><span data-stu-id="01dbf-120">-Confirm</span></span>
<span data-ttu-id="01dbf-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01dbf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01dbf-122">-WhatIf</span></span>
<span data-ttu-id="01dbf-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01dbf-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01dbf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dbf-125">-DefaultProfile</span></span>
<span data-ttu-id="01dbf-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01dbf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dbf-127">CommonParameters</span></span>
<span data-ttu-id="01dbf-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01dbf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dbf-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01dbf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dbf-130">입력</span><span class="sxs-lookup"><span data-stu-id="01dbf-130">INPUTS</span></span>

### <span data-ttu-id="01dbf-131">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="01dbf-131">System.Int32</span></span>
<span data-ttu-id="01dbf-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01dbf-132">System.String</span></span>

## <span data-ttu-id="01dbf-133">출력</span><span class="sxs-lookup"><span data-stu-id="01dbf-133">OUTPUTS</span></span>

### <span data-ttu-id="01dbf-134">System. 개체</span><span class="sxs-lookup"><span data-stu-id="01dbf-134">System.Object</span></span>

## <span data-ttu-id="01dbf-135">상속자</span><span class="sxs-lookup"><span data-stu-id="01dbf-135">NOTES</span></span>

## <span data-ttu-id="01dbf-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01dbf-136">RELATED LINKS</span></span>

[<span data-ttu-id="01dbf-137">추가-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="01dbf-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
