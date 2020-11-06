---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535128"
---
# <span data-ttu-id="c6193-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c6193-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="c6193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6193-102">SYNOPSIS</span></span>
<span data-ttu-id="c6193-103">클러스터에서 전체 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6193-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6193-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6193-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6193-105">DESCRIPTION</span></span>
<span data-ttu-id="c6193-106">**AzureRmServiceFabricNodeType** 를 사용 하 여 특정 노드 형식 및 클러스터의 노드 유형에 서 모든 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="c6193-107">이 명령은 기본 노드 유형을 삭제 하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="c6193-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c6193-108">EXAMPLES</span></span>

### <span data-ttu-id="c6193-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6193-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="c6193-110">이 명령은 클러스터에서 NodeType ' nt1 '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="c6193-111">변수</span><span class="sxs-lookup"><span data-stu-id="c6193-111">PARAMETERS</span></span>

### <span data-ttu-id="c6193-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6193-112">-DefaultProfile</span></span>
<span data-ttu-id="c6193-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6193-114">-이름</span><span class="sxs-lookup"><span data-stu-id="c6193-114">-Name</span></span>
<span data-ttu-id="c6193-115">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c6193-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c6193-116">-NodeType</span></span>
<span data-ttu-id="c6193-117">노드 형식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-117">The node type name.</span></span>

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

### <span data-ttu-id="c6193-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6193-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6193-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c6193-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c6193-120">-Confirm</span></span>
<span data-ttu-id="c6193-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6193-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6193-122">-WhatIf</span></span>
<span data-ttu-id="c6193-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6193-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6193-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6193-125">CommonParameters</span></span>
<span data-ttu-id="c6193-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6193-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6193-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6193-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6193-128">입력</span><span class="sxs-lookup"><span data-stu-id="c6193-128">INPUTS</span></span>

### <span data-ttu-id="c6193-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6193-129">System.String</span></span>
<span data-ttu-id="c6193-130">매개 변수: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c6193-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="c6193-131">출력</span><span class="sxs-lookup"><span data-stu-id="c6193-131">OUTPUTS</span></span>

### <span data-ttu-id="c6193-132">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="c6193-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c6193-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c6193-133">NOTES</span></span>

## <span data-ttu-id="c6193-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6193-134">RELATED LINKS</span></span>
