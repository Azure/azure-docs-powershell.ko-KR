---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383566"
---
# <span data-ttu-id="4e4a2-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="4e4a2-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="4e4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4a2-103">Azure Synapse Analytics 풀에 새 복원 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4e4a2-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e4a2-104">SYNTAX</span></span>

### <span data-ttu-id="4e4a2-105">CreateByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4e4a2-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e4a2-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e4a2-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e4a2-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e4a2-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e4a2-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e4a2-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e4a2-109">설명</span><span class="sxs-lookup"><span data-stu-id="4e4a2-109">DESCRIPTION</span></span>
<span data-ttu-id="4e4a2-110">**New-AzSynapseSqlPoolRestorePoint** cmdlet은 Azure Synapse Analytics SQL 복원할 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="4e4a2-111">예제</span><span class="sxs-lookup"><span data-stu-id="4e4a2-111">EXAMPLES</span></span>

### <span data-ttu-id="4e4a2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e4a2-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="4e4a2-113">이 명령은 작업 영역 ContosoWorkspace에서 contosoSqlPool이라는 SQL 풀에 대한 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="4e4a2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e4a2-114">PARAMETERS</span></span>

### <span data-ttu-id="4e4a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e4a2-115">-AsJob</span></span>
<span data-ttu-id="4e4a2-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4e4a2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e4a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4a2-117">-DefaultProfile</span></span>
<span data-ttu-id="4e4a2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e4a2-119">-InputObject</span></span>
<span data-ttu-id="4e4a2-120">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e4a2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4e4a2-121">-Name</span></span>
<span data-ttu-id="4e4a2-122">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="4e4a2-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-124">Resource group name.</span></span>

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

### <span data-ttu-id="4e4a2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e4a2-125">-ResourceId</span></span>
<span data-ttu-id="4e4a2-126">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4a2-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="4e4a2-127">-RestorePointLabel</span></span>
<span data-ttu-id="4e4a2-128">복원 지점을 연결한 레이블은 고유하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="4e4a2-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4e4a2-129">-WorkspaceName</span></span>
<span data-ttu-id="4e4a2-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4e4a2-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4e4a2-131">-WorkspaceObject</span></span>
<span data-ttu-id="4e4a2-132">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4e4a2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e4a2-133">-Confirm</span></span>
<span data-ttu-id="4e4a2-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4a2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4a2-135">-WhatIf</span></span>
<span data-ttu-id="4e4a2-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e4a2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4a2-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4a2-138">CommonParameters</span></span>
<span data-ttu-id="4e4a2-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4a2-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e4a2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4a2-141">입력</span><span class="sxs-lookup"><span data-stu-id="4e4a2-141">INPUTS</span></span>

### <span data-ttu-id="4e4a2-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4e4a2-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4e4a2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4e4a2-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4e4a2-144">출력</span><span class="sxs-lookup"><span data-stu-id="4e4a2-144">OUTPUTS</span></span>

### <span data-ttu-id="4e4a2-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="4e4a2-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="4e4a2-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e4a2-146">NOTES</span></span>

## <span data-ttu-id="4e4a2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e4a2-147">RELATED LINKS</span></span>
