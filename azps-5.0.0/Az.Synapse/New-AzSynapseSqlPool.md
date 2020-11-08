---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226012"
---
# <span data-ttu-id="bc2ce-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bc2ce-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="bc2ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2ce-103">Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bc2ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc2ce-104">SYNTAX</span></span>

### <span data-ttu-id="bc2ce-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc2ce-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc2ce-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc2ce-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc2ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc2ce-107">DESCRIPTION</span></span>
<span data-ttu-id="bc2ce-108">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bc2ce-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bc2ce-109">EXAMPLES</span></span>

### <span data-ttu-id="bc2ce-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc2ce-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="bc2ce-111">이 명령은 Azure Synapse Analytics SQL 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bc2ce-112">변수</span><span class="sxs-lookup"><span data-stu-id="bc2ce-112">PARAMETERS</span></span>

### <span data-ttu-id="bc2ce-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc2ce-113">-AsJob</span></span>
<span data-ttu-id="bc2ce-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bc2ce-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc2ce-115">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="bc2ce-115">-Collation</span></span>
<span data-ttu-id="bc2ce-116">데이터 정렬은 데이터를 정렬 및 비교 하는 규칙을 정의 하 고 SQL 풀을 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="bc2ce-117">기본 데이터 정렬은 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2ce-118">-DefaultProfile</span></span>
<span data-ttu-id="bc2ce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc2ce-120">-이름</span><span class="sxs-lookup"><span data-stu-id="bc2ce-120">-Name</span></span>
<span data-ttu-id="bc2ce-121">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="bc2ce-122">-PerformanceLevel</span></span>
<span data-ttu-id="bc2ce-123">SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="bc2ce-124">예를 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-124">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc2ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc2ce-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-127">태그</span><span class="sxs-lookup"><span data-stu-id="bc2ce-127">-Tag</span></span>
<span data-ttu-id="bc2ce-128">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-129">-버전</span><span class="sxs-lookup"><span data-stu-id="bc2ce-129">-Version</span></span>
<span data-ttu-id="bc2ce-130">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="bc2ce-131">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc2ce-132">-WorkspaceName</span></span>
<span data-ttu-id="bc2ce-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bc2ce-134">-WorkspaceObject</span></span>
<span data-ttu-id="bc2ce-135">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc2ce-136">-확인</span><span class="sxs-lookup"><span data-stu-id="bc2ce-136">-Confirm</span></span>
<span data-ttu-id="bc2ce-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc2ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc2ce-138">-WhatIf</span></span>
<span data-ttu-id="bc2ce-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc2ce-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc2ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2ce-141">CommonParameters</span></span>
<span data-ttu-id="bc2ce-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2ce-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2ce-144">입력</span><span class="sxs-lookup"><span data-stu-id="bc2ce-144">INPUTS</span></span>

### <span data-ttu-id="bc2ce-145">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bc2ce-146">출력</span><span class="sxs-lookup"><span data-stu-id="bc2ce-146">OUTPUTS</span></span>

### <span data-ttu-id="bc2ce-147">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="bc2ce-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bc2ce-148">상속자</span><span class="sxs-lookup"><span data-stu-id="bc2ce-148">NOTES</span></span>

## <span data-ttu-id="bc2ce-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc2ce-149">RELATED LINKS</span></span>
