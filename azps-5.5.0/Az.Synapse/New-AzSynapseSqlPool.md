---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182753"
---
# <span data-ttu-id="0a154-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a154-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="0a154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a154-102">SYNOPSIS</span></span>
<span data-ttu-id="0a154-103">Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a154-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a154-104">SYNTAX</span></span>

### <span data-ttu-id="0a154-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a154-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a154-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a154-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a154-107">설명</span><span class="sxs-lookup"><span data-stu-id="0a154-107">DESCRIPTION</span></span>
<span data-ttu-id="0a154-108">**New-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a154-109">예제</span><span class="sxs-lookup"><span data-stu-id="0a154-109">EXAMPLES</span></span>

### <span data-ttu-id="0a154-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a154-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="0a154-111">이 명령은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0a154-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a154-112">PARAMETERS</span></span>

### <span data-ttu-id="0a154-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a154-113">-AsJob</span></span>
<span data-ttu-id="0a154-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0a154-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a154-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="0a154-115">-Collation</span></span>
<span data-ttu-id="0a154-116">데이터 정렬은 데이터를 정렬하고 비교하는 규칙을 정의하며 풀을 생성한 후에 변경할 SQL 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="0a154-117">기본 데이터 데이터 데이터 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="0a154-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a154-118">-DefaultProfile</span></span>
<span data-ttu-id="0a154-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a154-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0a154-120">-Name</span></span>
<span data-ttu-id="0a154-121">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a154-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="0a154-122">-PerformanceLevel</span></span>
<span data-ttu-id="0a154-123">SQL 풀에 할당할 SQL 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="0a154-124">예를 들어 DW2000c입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="0a154-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a154-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a154-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-126">Resource group name.</span></span>

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

### <span data-ttu-id="0a154-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a154-127">-Tag</span></span>
<span data-ttu-id="0a154-128">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="0a154-129">-Version</span><span class="sxs-lookup"><span data-stu-id="0a154-129">-Version</span></span>
<span data-ttu-id="0a154-130">Synapse SQL 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="0a154-131">예를 들어 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="0a154-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a154-132">-WorkspaceName</span></span>
<span data-ttu-id="0a154-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0a154-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a154-134">-WorkspaceObject</span></span>
<span data-ttu-id="0a154-135">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a154-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a154-136">-Confirm</span></span>
<span data-ttu-id="0a154-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a154-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a154-138">-WhatIf</span></span>
<span data-ttu-id="0a154-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a154-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a154-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a154-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a154-141">CommonParameters</span></span>
<span data-ttu-id="0a154-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a154-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a154-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a154-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a154-144">입력</span><span class="sxs-lookup"><span data-stu-id="0a154-144">INPUTS</span></span>

### <span data-ttu-id="0a154-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a154-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0a154-146">출력</span><span class="sxs-lookup"><span data-stu-id="0a154-146">OUTPUTS</span></span>

### <span data-ttu-id="0a154-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0a154-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0a154-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a154-148">NOTES</span></span>

## <span data-ttu-id="0a154-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a154-149">RELATED LINKS</span></span>
