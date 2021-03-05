---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 829227e47c0c68ac8ebe44f1a365898baa6e123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990724"
---
# <span data-ttu-id="85a15-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="85a15-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="85a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a15-102">SYNOPSIS</span></span>
<span data-ttu-id="85a15-103">Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="85a15-104">구문</span><span class="sxs-lookup"><span data-stu-id="85a15-104">SYNTAX</span></span>

### <span data-ttu-id="85a15-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="85a15-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85a15-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85a15-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85a15-107">설명</span><span class="sxs-lookup"><span data-stu-id="85a15-107">DESCRIPTION</span></span>
<span data-ttu-id="85a15-108">**New-AzSynapseSqlPool** cmdlet은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="85a15-109">예제</span><span class="sxs-lookup"><span data-stu-id="85a15-109">EXAMPLES</span></span>

### <span data-ttu-id="85a15-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="85a15-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="85a15-111">이 명령은 Azure Synapse Analytics SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="85a15-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85a15-112">PARAMETERS</span></span>

### <span data-ttu-id="85a15-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85a15-113">-AsJob</span></span>
<span data-ttu-id="85a15-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="85a15-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85a15-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="85a15-115">-Collation</span></span>
<span data-ttu-id="85a15-116">데이터 정렬은 데이터를 정렬하고 비교하는 규칙을 정의하며 풀을 생성한 후에 변경할 SQL 없습니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="85a15-117">기본 데이터 SQL_Latin1_General_CP1_CI_AS입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="85a15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a15-118">-DefaultProfile</span></span>
<span data-ttu-id="85a15-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a15-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85a15-120">-Name</span></span>
<span data-ttu-id="85a15-121">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="85a15-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="85a15-122">-PerformanceLevel</span></span>
<span data-ttu-id="85a15-123">SQL 풀에 할당할 서비스 계층 및 SQL 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="85a15-124">예를 들어 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="85a15-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="85a15-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a15-125">-ResourceGroupName</span></span>
<span data-ttu-id="85a15-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-126">Resource group name.</span></span>

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

### <span data-ttu-id="85a15-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="85a15-127">-Tag</span></span>
<span data-ttu-id="85a15-128">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="85a15-129">-Version</span><span class="sxs-lookup"><span data-stu-id="85a15-129">-Version</span></span>
<span data-ttu-id="85a15-130">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="85a15-131">예를 들어 2 또는 3.</span><span class="sxs-lookup"><span data-stu-id="85a15-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="85a15-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85a15-132">-WorkspaceName</span></span>
<span data-ttu-id="85a15-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="85a15-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="85a15-134">-WorkspaceObject</span></span>
<span data-ttu-id="85a15-135">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="85a15-136">-확인</span><span class="sxs-lookup"><span data-stu-id="85a15-136">-Confirm</span></span>
<span data-ttu-id="85a15-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85a15-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85a15-138">-WhatIf</span></span>
<span data-ttu-id="85a15-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85a15-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85a15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a15-141">CommonParameters</span></span>
<span data-ttu-id="85a15-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85a15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a15-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85a15-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a15-144">입력</span><span class="sxs-lookup"><span data-stu-id="85a15-144">INPUTS</span></span>

### <span data-ttu-id="85a15-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="85a15-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="85a15-146">출력</span><span class="sxs-lookup"><span data-stu-id="85a15-146">OUTPUTS</span></span>

### <span data-ttu-id="85a15-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="85a15-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="85a15-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85a15-148">NOTES</span></span>

## <span data-ttu-id="85a15-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85a15-149">RELATED LINKS</span></span>
