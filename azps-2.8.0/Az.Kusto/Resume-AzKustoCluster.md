---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: ce2fbe2f598ca6d08033c397a988f140379fda96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689569"
---
# <span data-ttu-id="68cce-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="68cce-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="68cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68cce-102">SYNOPSIS</span></span>
<span data-ttu-id="68cce-103">일시 중단 된 Kusto 클러스터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="68cce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68cce-104">SYNTAX</span></span>

### <span data-ttu-id="68cce-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="68cce-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68cce-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="68cce-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68cce-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="68cce-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68cce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68cce-108">DESCRIPTION</span></span>
<span data-ttu-id="68cce-109">일시 중단 된 Kusto 클러스터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="68cce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68cce-110">EXAMPLES</span></span>

### <span data-ttu-id="68cce-111">예제 1-이름으로 일시 중지 된 Kusto 다시 시작</span><span class="sxs-lookup"><span data-stu-id="68cce-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="68cce-112">위의 명령으로 일시 중단 된 Kusto 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="68cce-113">예제 2-파이프에 따라 일시 중지 된 Kusto 클러스터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="68cce-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="68cce-114">위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 이라는 Kusto 클러스터를 가져온 `Get-AzKustoCluster` 다음 `Resume-AzKustoCluster` 다시 시작 하도록 결과를 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="68cce-115">변수</span><span class="sxs-lookup"><span data-stu-id="68cce-115">PARAMETERS</span></span>

### <span data-ttu-id="68cce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cce-116">-DefaultProfile</span></span>
<span data-ttu-id="68cce-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68cce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68cce-118">-InputObject</span></span>
<span data-ttu-id="68cce-119">클러스터 개체를 위한 kusto</span><span class="sxs-lookup"><span data-stu-id="68cce-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="68cce-120">-이름</span><span class="sxs-lookup"><span data-stu-id="68cce-120">-Name</span></span>
<span data-ttu-id="68cce-121">다시 시작할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="68cce-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68cce-122">-PassThru</span></span>
<span data-ttu-id="68cce-123">지정 된 클러스터가 성공적으로 다시 시작 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="68cce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68cce-124">-ResourceGroupName</span></span>
<span data-ttu-id="68cce-125">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68cce-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68cce-126">-ResourceId</span></span>
<span data-ttu-id="68cce-127">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="68cce-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="68cce-128">-확인</span><span class="sxs-lookup"><span data-stu-id="68cce-128">-Confirm</span></span>
<span data-ttu-id="68cce-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68cce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cce-130">-WhatIf</span></span>
<span data-ttu-id="68cce-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68cce-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68cce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cce-133">CommonParameters</span></span>
<span data-ttu-id="68cce-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cce-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68cce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cce-136">입력</span><span class="sxs-lookup"><span data-stu-id="68cce-136">INPUTS</span></span>

### <span data-ttu-id="68cce-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68cce-137">System.String</span></span>

### <span data-ttu-id="68cce-138">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="68cce-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="68cce-139">출력</span><span class="sxs-lookup"><span data-stu-id="68cce-139">OUTPUTS</span></span>

### <span data-ttu-id="68cce-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="68cce-140">System.Boolean</span></span>

## <span data-ttu-id="68cce-141">상속자</span><span class="sxs-lookup"><span data-stu-id="68cce-141">NOTES</span></span>

## <span data-ttu-id="68cce-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68cce-142">RELATED LINKS</span></span>
