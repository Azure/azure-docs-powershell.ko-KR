---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 425b9c74fac1cd17b8e2c86045fbb4fcd8875b67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979088"
---
# <span data-ttu-id="e2d8c-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e2d8c-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e2d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d8c-103">모든 풀에서 고급 위협 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="e2d8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2d8c-104">SYNTAX</span></span>

### <span data-ttu-id="e2d8c-105">ClearByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2d8c-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2d8c-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2d8c-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2d8c-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2d8c-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2d8c-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2d8c-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d8c-109">설명</span><span class="sxs-lookup"><span data-stu-id="e2d8c-109">DESCRIPTION</span></span>
<span data-ttu-id="e2d8c-110">**Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e2d8c-111">예제</span><span class="sxs-lookup"><span data-stu-id="e2d8c-111">EXAMPLES</span></span>

### <span data-ttu-id="e2d8c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2d8c-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e2d8c-113">이 명령은 ContosoWorkspace라는 작업 영역 아래에서 ContosoSqlPool이라는 SQL 풀에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e2d8c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2d8c-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d8c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2d8c-115">-AsJob</span></span>
<span data-ttu-id="e2d8c-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e2d8c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2d8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d8c-117">-DefaultProfile</span></span>
<span data-ttu-id="e2d8c-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2d8c-119">-InputObject</span></span>
<span data-ttu-id="e2d8c-120">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e2d8c-121">-Name</span></span>
<span data-ttu-id="e2d8c-122">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2d8c-123">-PassThru</span></span>
<span data-ttu-id="e2d8c-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e2d8c-125">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e2d8c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d8c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2d8c-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2d8c-128">-ResourceId</span></span>
<span data-ttu-id="e2d8c-129">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2d8c-130">-WorkspaceName</span></span>
<span data-ttu-id="e2d8c-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2d8c-132">-WorkspaceObject</span></span>
<span data-ttu-id="e2d8c-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d8c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="e2d8c-134">-Confirm</span></span>
<span data-ttu-id="e2d8c-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d8c-136">-WhatIf</span></span>
<span data-ttu-id="e2d8c-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d8c-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d8c-139">CommonParameters</span></span>
<span data-ttu-id="e2d8c-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2d8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d8c-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2d8c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d8c-142">입력</span><span class="sxs-lookup"><span data-stu-id="e2d8c-142">INPUTS</span></span>

### <span data-ttu-id="e2d8c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e2d8c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e2d8c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e2d8c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e2d8c-145">출력</span><span class="sxs-lookup"><span data-stu-id="e2d8c-145">OUTPUTS</span></span>

### <span data-ttu-id="e2d8c-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e2d8c-146">System.Boolean</span></span>

## <span data-ttu-id="e2d8c-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2d8c-147">NOTES</span></span>

## <span data-ttu-id="e2d8c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2d8c-148">RELATED LINKS</span></span>
