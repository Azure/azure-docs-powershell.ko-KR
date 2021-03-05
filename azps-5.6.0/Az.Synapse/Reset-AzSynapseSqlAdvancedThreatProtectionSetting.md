---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9b4e55f701b956fc653cf08cddb87997a998315e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987471"
---
# <span data-ttu-id="7a2f2-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7a2f2-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="7a2f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a2f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2f2-103">작업 영역에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="7a2f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a2f2-104">SYNTAX</span></span>

### <span data-ttu-id="7a2f2-105">ClearByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a2f2-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2f2-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a2f2-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a2f2-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a2f2-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a2f2-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a2f2-108">DESCRIPTION</span></span>
<span data-ttu-id="7a2f2-109">**Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics 작업 영역의 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="7a2f2-110">예제</span><span class="sxs-lookup"><span data-stu-id="7a2f2-110">EXAMPLES</span></span>

### <span data-ttu-id="7a2f2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a2f2-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7a2f2-112">이 명령은 ContosoWorkspace라는 작업 영역에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7a2f2-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a2f2-113">PARAMETERS</span></span>

### <span data-ttu-id="7a2f2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a2f2-114">-AsJob</span></span>
<span data-ttu-id="7a2f2-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a2f2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a2f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2f2-116">-DefaultProfile</span></span>
<span data-ttu-id="7a2f2-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a2f2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a2f2-118">-InputObject</span></span>
<span data-ttu-id="7a2f2-119">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a2f2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a2f2-120">-PassThru</span></span>
<span data-ttu-id="7a2f2-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7a2f2-122">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7a2f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a2f2-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-124">Resource group name.</span></span>

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

### <span data-ttu-id="7a2f2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a2f2-125">-ResourceId</span></span>
<span data-ttu-id="7a2f2-126">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="7a2f2-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a2f2-127">-WorkspaceName</span></span>
<span data-ttu-id="7a2f2-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7a2f2-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7a2f2-129">-Confirm</span></span>
<span data-ttu-id="7a2f2-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2f2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2f2-131">-WhatIf</span></span>
<span data-ttu-id="7a2f2-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2f2-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a2f2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2f2-134">CommonParameters</span></span>
<span data-ttu-id="7a2f2-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2f2-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a2f2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2f2-137">입력</span><span class="sxs-lookup"><span data-stu-id="7a2f2-137">INPUTS</span></span>

### <span data-ttu-id="7a2f2-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a2f2-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7a2f2-139">출력</span><span class="sxs-lookup"><span data-stu-id="7a2f2-139">OUTPUTS</span></span>

### <span data-ttu-id="7a2f2-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a2f2-140">System.Boolean</span></span>

## <span data-ttu-id="7a2f2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a2f2-141">NOTES</span></span>

## <span data-ttu-id="7a2f2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a2f2-142">RELATED LINKS</span></span>
