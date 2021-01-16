---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 997132e201864653307af3d072920d36b19d5af3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367172"
---
# <span data-ttu-id="32bd1-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="32bd1-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="32bd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="32bd1-103">Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="32bd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="32bd1-104">SYNTAX</span></span>

### <span data-ttu-id="32bd1-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="32bd1-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bd1-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32bd1-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bd1-107">설명</span><span class="sxs-lookup"><span data-stu-id="32bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="32bd1-108">**New-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="32bd1-109">예제</span><span class="sxs-lookup"><span data-stu-id="32bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="32bd1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="32bd1-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="32bd1-111">이 명령은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="32bd1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32bd1-112">PARAMETERS</span></span>

### <span data-ttu-id="32bd1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32bd1-113">-AsJob</span></span>
<span data-ttu-id="32bd1-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32bd1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32bd1-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="32bd1-115">-Collation</span></span>
<span data-ttu-id="32bd1-116">데이터 정렬은 데이터를 정렬하고 비교하는 규칙을 정의하며 풀을 생성한 후에 변경할 SQL 없습니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="32bd1-117">기본 데이터 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="32bd1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bd1-118">-DefaultProfile</span></span>
<span data-ttu-id="32bd1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bd1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="32bd1-120">-Name</span></span>
<span data-ttu-id="32bd1-121">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="32bd1-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="32bd1-122">-PerformanceLevel</span></span>
<span data-ttu-id="32bd1-123">SQL 풀에 할당할 SQL 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="32bd1-124">예를 들어 DW2000c입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="32bd1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bd1-125">-ResourceGroupName</span></span>
<span data-ttu-id="32bd1-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-126">Resource group name.</span></span>

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

### <span data-ttu-id="32bd1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="32bd1-127">-Tag</span></span>
<span data-ttu-id="32bd1-128">리소스와 연결된 태그의 문자열 사전 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="32bd1-129">-Version</span><span class="sxs-lookup"><span data-stu-id="32bd1-129">-Version</span></span>
<span data-ttu-id="32bd1-130">Synapse SQL 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="32bd1-131">예를 들어 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="32bd1-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="32bd1-132">-WorkspaceName</span></span>
<span data-ttu-id="32bd1-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="32bd1-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="32bd1-134">-WorkspaceObject</span></span>
<span data-ttu-id="32bd1-135">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="32bd1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32bd1-136">-Confirm</span></span>
<span data-ttu-id="32bd1-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32bd1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bd1-138">-WhatIf</span></span>
<span data-ttu-id="32bd1-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32bd1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32bd1-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32bd1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bd1-141">CommonParameters</span></span>
<span data-ttu-id="32bd1-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32bd1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bd1-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32bd1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bd1-144">입력</span><span class="sxs-lookup"><span data-stu-id="32bd1-144">INPUTS</span></span>

### <span data-ttu-id="32bd1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="32bd1-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="32bd1-146">출력</span><span class="sxs-lookup"><span data-stu-id="32bd1-146">OUTPUTS</span></span>

### <span data-ttu-id="32bd1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="32bd1-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="32bd1-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32bd1-148">NOTES</span></span>

## <span data-ttu-id="32bd1-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32bd1-149">RELATED LINKS</span></span>
