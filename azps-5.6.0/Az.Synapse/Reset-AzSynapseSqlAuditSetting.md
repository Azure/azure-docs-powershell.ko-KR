---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973707"
---
# <span data-ttu-id="e4645-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="e4645-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="e4645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4645-102">SYNOPSIS</span></span>
<span data-ttu-id="e4645-103">Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e4645-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4645-104">SYNTAX</span></span>

### <span data-ttu-id="e4645-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e4645-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4645-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4645-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4645-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4645-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4645-108">설명</span><span class="sxs-lookup"><span data-stu-id="e4645-108">DESCRIPTION</span></span>
<span data-ttu-id="e4645-109">**Reset-AzSynapseSqlAuditSetting** cmdlet은 Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e4645-110">예제</span><span class="sxs-lookup"><span data-stu-id="e4645-110">EXAMPLES</span></span>

### <span data-ttu-id="e4645-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e4645-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e4645-112">이 명령은 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e4645-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e4645-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="e4645-114">이 명령은 파이프라인을 통해 ContosoWorkspace라는 Azure Synapse Analytics 작업 영역의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e4645-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4645-115">PARAMETERS</span></span>

### <span data-ttu-id="e4645-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4645-116">-AsJob</span></span>
<span data-ttu-id="e4645-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e4645-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4645-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4645-118">-DefaultProfile</span></span>
<span data-ttu-id="e4645-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4645-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4645-120">-InputObject</span></span>
<span data-ttu-id="e4645-121">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e4645-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4645-122">-PassThru</span></span>
<span data-ttu-id="e4645-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e4645-124">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e4645-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4645-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4645-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-126">Resource group name.</span></span>

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

### <span data-ttu-id="e4645-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4645-127">-ResourceId</span></span>
<span data-ttu-id="e4645-128">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="e4645-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e4645-129">-WorkspaceName</span></span>
<span data-ttu-id="e4645-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e4645-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e4645-131">-Confirm</span></span>
<span data-ttu-id="e4645-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4645-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4645-133">-WhatIf</span></span>
<span data-ttu-id="e4645-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4645-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4645-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4645-136">CommonParameters</span></span>
<span data-ttu-id="e4645-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4645-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4645-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4645-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4645-139">입력</span><span class="sxs-lookup"><span data-stu-id="e4645-139">INPUTS</span></span>

### <span data-ttu-id="e4645-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e4645-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e4645-141">출력</span><span class="sxs-lookup"><span data-stu-id="e4645-141">OUTPUTS</span></span>

### <span data-ttu-id="e4645-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4645-142">System.Boolean</span></span>

## <span data-ttu-id="e4645-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4645-143">NOTES</span></span>

## <span data-ttu-id="e4645-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4645-144">RELATED LINKS</span></span>
