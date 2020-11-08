---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: bc21812003ca7e71b9f7fa726aea766e924d2519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041671"
---
# <span data-ttu-id="86638-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="86638-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="86638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86638-102">SYNOPSIS</span></span>
<span data-ttu-id="86638-103">클러스터에서 전체 노드 유형을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="86638-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86638-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86638-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86638-105">DESCRIPTION</span></span>
<span data-ttu-id="86638-106">**AzServiceFabricNodeType** 를 사용 하 여 특정 노드 형식 및 클러스터의 노드 유형에 서 모든 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="86638-107">이 명령은 기본 노드 유형을 삭제 하는 데 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="86638-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="86638-108">예제의</span><span class="sxs-lookup"><span data-stu-id="86638-108">EXAMPLES</span></span>

### <span data-ttu-id="86638-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="86638-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="86638-110">이 명령은 클러스터에서 NodeType ' nt1 '를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="86638-111">변수</span><span class="sxs-lookup"><span data-stu-id="86638-111">PARAMETERS</span></span>

### <span data-ttu-id="86638-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86638-112">-DefaultProfile</span></span>
<span data-ttu-id="86638-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86638-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86638-114">-이름</span><span class="sxs-lookup"><span data-stu-id="86638-114">-Name</span></span>
<span data-ttu-id="86638-115">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="86638-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="86638-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="86638-116">-NodeType</span></span>
<span data-ttu-id="86638-117">노드 형식 이름</span><span class="sxs-lookup"><span data-stu-id="86638-117">The node type name</span></span>

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

### <span data-ttu-id="86638-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86638-118">-ResourceGroupName</span></span>
<span data-ttu-id="86638-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="86638-120">-확인</span><span class="sxs-lookup"><span data-stu-id="86638-120">-Confirm</span></span>
<span data-ttu-id="86638-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86638-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86638-122">-WhatIf</span></span>
<span data-ttu-id="86638-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="86638-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86638-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86638-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86638-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86638-125">CommonParameters</span></span>
<span data-ttu-id="86638-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86638-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86638-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86638-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86638-128">입력</span><span class="sxs-lookup"><span data-stu-id="86638-128">INPUTS</span></span>

### <span data-ttu-id="86638-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="86638-129">System.String</span></span>

## <span data-ttu-id="86638-130">출력</span><span class="sxs-lookup"><span data-stu-id="86638-130">OUTPUTS</span></span>

### <span data-ttu-id="86638-131">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="86638-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="86638-132">상속자</span><span class="sxs-lookup"><span data-stu-id="86638-132">NOTES</span></span>

## <span data-ttu-id="86638-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86638-133">RELATED LINKS</span></span>