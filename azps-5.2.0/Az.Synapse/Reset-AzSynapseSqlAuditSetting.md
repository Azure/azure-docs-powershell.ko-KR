---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333818"
---
# <span data-ttu-id="6d09a-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="6d09a-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="6d09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d09a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d09a-103">Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="6d09a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d09a-104">SYNTAX</span></span>

### <span data-ttu-id="6d09a-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6d09a-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d09a-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d09a-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d09a-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d09a-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d09a-108">설명</span><span class="sxs-lookup"><span data-stu-id="6d09a-108">DESCRIPTION</span></span>
<span data-ttu-id="6d09a-109">**Reset-AzSynapseSqlAuditSetting** cmdlet은 Azure Synapse 분석 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="6d09a-110">예제</span><span class="sxs-lookup"><span data-stu-id="6d09a-110">EXAMPLES</span></span>

### <span data-ttu-id="6d09a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d09a-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6d09a-112">이 명령은 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6d09a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6d09a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="6d09a-114">이 명령은 파이프라인을 통해 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="6d09a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d09a-115">PARAMETERS</span></span>

### <span data-ttu-id="6d09a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d09a-116">-AsJob</span></span>
<span data-ttu-id="6d09a-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d09a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d09a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d09a-118">-DefaultProfile</span></span>
<span data-ttu-id="6d09a-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d09a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d09a-120">-InputObject</span></span>
<span data-ttu-id="6d09a-121">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d09a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d09a-122">-PassThru</span></span>
<span data-ttu-id="6d09a-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6d09a-124">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6d09a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d09a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d09a-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-126">Resource group name.</span></span>

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

### <span data-ttu-id="6d09a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d09a-127">-ResourceId</span></span>
<span data-ttu-id="6d09a-128">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="6d09a-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d09a-129">-WorkspaceName</span></span>
<span data-ttu-id="6d09a-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6d09a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d09a-131">-Confirm</span></span>
<span data-ttu-id="6d09a-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d09a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d09a-133">-WhatIf</span></span>
<span data-ttu-id="6d09a-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6d09a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d09a-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d09a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d09a-136">CommonParameters</span></span>
<span data-ttu-id="6d09a-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d09a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d09a-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d09a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d09a-139">입력</span><span class="sxs-lookup"><span data-stu-id="6d09a-139">INPUTS</span></span>

### <span data-ttu-id="6d09a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d09a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6d09a-141">출력</span><span class="sxs-lookup"><span data-stu-id="6d09a-141">OUTPUTS</span></span>

### <span data-ttu-id="6d09a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d09a-142">System.Boolean</span></span>

## <span data-ttu-id="6d09a-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d09a-143">NOTES</span></span>

## <span data-ttu-id="6d09a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d09a-144">RELATED LINKS</span></span>
