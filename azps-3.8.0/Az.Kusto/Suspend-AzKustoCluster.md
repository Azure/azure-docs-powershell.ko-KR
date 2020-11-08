---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 17c730fb65e50aeeff33e616b7be596745d67ac0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034584"
---
# <span data-ttu-id="ceb3d-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ceb3d-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="ceb3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb3d-103">기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="ceb3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ceb3d-104">SYNTAX</span></span>

### <span data-ttu-id="ceb3d-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="ceb3d-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb3d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ceb3d-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceb3d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ceb3d-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceb3d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ceb3d-108">DESCRIPTION</span></span>
<span data-ttu-id="ceb3d-109">기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="ceb3d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ceb3d-110">EXAMPLES</span></span>

### <span data-ttu-id="ceb3d-111">예제 1-이름으로 기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="ceb3d-112">위의 명령은 리소스 그룹 "testrg"에 있는 "mykustocluster" 이라는 이름으로 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="ceb3d-113">예제 2-파이프에 따라 기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="ceb3d-114">위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 이라는 Kusto 클러스터를 가져온 `Get-AzKustoCluster` 다음 해당 결과를 일시 중단으로 파이프 합니다 `Suspend-AzKustoCluster` .</span><span class="sxs-lookup"><span data-stu-id="ceb3d-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="ceb3d-115">변수</span><span class="sxs-lookup"><span data-stu-id="ceb3d-115">PARAMETERS</span></span>

### <span data-ttu-id="ceb3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb3d-116">-DefaultProfile</span></span>
<span data-ttu-id="ceb3d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceb3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceb3d-118">-InputObject</span></span>
<span data-ttu-id="ceb3d-119">클러스터 개체를 위한 kusto</span><span class="sxs-lookup"><span data-stu-id="ceb3d-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb3d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ceb3d-120">-Name</span></span>
<span data-ttu-id="ceb3d-121">일시 중단할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-121">Name of cluster to be suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb3d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ceb3d-122">-PassThru</span></span>
<span data-ttu-id="ceb3d-123">지정 된 클러스터가 성공적으로 일시 중단 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-123">Return whether the specified cluster was successfully suspended or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb3d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb3d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ceb3d-125">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceb3d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceb3d-126">-ResourceId</span></span>
<span data-ttu-id="ceb3d-127">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="ceb3d-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb3d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ceb3d-128">-Confirm</span></span>
<span data-ttu-id="ceb3d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceb3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceb3d-130">-WhatIf</span></span>
<span data-ttu-id="ceb3d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceb3d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceb3d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb3d-133">CommonParameters</span></span>
<span data-ttu-id="ceb3d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb3d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb3d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb3d-136">입력</span><span class="sxs-lookup"><span data-stu-id="ceb3d-136">INPUTS</span></span>

### <span data-ttu-id="ceb3d-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ceb3d-137">System.String</span></span>

### <span data-ttu-id="ceb3d-138">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ceb3d-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="ceb3d-139">출력</span><span class="sxs-lookup"><span data-stu-id="ceb3d-139">OUTPUTS</span></span>

### <span data-ttu-id="ceb3d-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ceb3d-140">System.Boolean</span></span>

## <span data-ttu-id="ceb3d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ceb3d-141">NOTES</span></span>

## <span data-ttu-id="ceb3d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ceb3d-142">RELATED LINKS</span></span>
