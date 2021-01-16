---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 77299e9424f0a194776b1114146b76ef2be3329f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329055"
---
# <span data-ttu-id="6a834-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="6a834-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="6a834-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a834-102">SYNOPSIS</span></span>
<span data-ttu-id="6a834-103">Azure Synapse Analytics 풀의 감사 설정을 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6a834-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a834-104">SYNTAX</span></span>

### <span data-ttu-id="6a834-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a834-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a834-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a834-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a834-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a834-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a834-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a834-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a834-109">설명</span><span class="sxs-lookup"><span data-stu-id="6a834-109">DESCRIPTION</span></span>
<span data-ttu-id="6a834-110">**Reset-AzSynapseSqlPoolAuditSetting** cmdlet은 Azure Synapse Analytics 풀의 감사 설정을 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="6a834-111">예제</span><span class="sxs-lookup"><span data-stu-id="6a834-111">EXAMPLES</span></span>

### <span data-ttu-id="6a834-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a834-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="6a834-113">이 명령은 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6a834-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6a834-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="6a834-115">이 명령은 파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6a834-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a834-116">PARAMETERS</span></span>

### <span data-ttu-id="6a834-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a834-117">-AsJob</span></span>
<span data-ttu-id="6a834-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6a834-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a834-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a834-119">-DefaultProfile</span></span>
<span data-ttu-id="6a834-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a834-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a834-121">-InputObject</span></span>
<span data-ttu-id="6a834-122">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6a834-123">-Name</span></span>
<span data-ttu-id="6a834-124">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a834-125">-PassThru</span></span>
<span data-ttu-id="6a834-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6a834-127">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6a834-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a834-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a834-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a834-130">-ResourceId</span></span>
<span data-ttu-id="6a834-131">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a834-132">-WorkspaceName</span></span>
<span data-ttu-id="6a834-133">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a834-134">-WorkspaceObject</span></span>
<span data-ttu-id="6a834-135">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a834-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a834-136">-Confirm</span></span>
<span data-ttu-id="6a834-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a834-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a834-138">-WhatIf</span></span>
<span data-ttu-id="6a834-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6a834-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a834-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a834-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a834-141">CommonParameters</span></span>
<span data-ttu-id="6a834-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a834-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a834-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a834-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a834-144">입력</span><span class="sxs-lookup"><span data-stu-id="6a834-144">INPUTS</span></span>

### <span data-ttu-id="6a834-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a834-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6a834-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6a834-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6a834-147">출력</span><span class="sxs-lookup"><span data-stu-id="6a834-147">OUTPUTS</span></span>

### <span data-ttu-id="6a834-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a834-148">System.Boolean</span></span>

## <span data-ttu-id="6a834-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a834-149">NOTES</span></span>

## <span data-ttu-id="6a834-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a834-150">RELATED LINKS</span></span>
