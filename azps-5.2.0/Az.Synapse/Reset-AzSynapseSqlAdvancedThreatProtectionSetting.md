---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334694"
---
# <span data-ttu-id="2bbe8-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="2bbe8-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="2bbe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bbe8-102">SYNOPSIS</span></span>
<span data-ttu-id="2bbe8-103">작업 영역의 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="2bbe8-104">구문</span><span class="sxs-lookup"><span data-stu-id="2bbe8-104">SYNTAX</span></span>

### <span data-ttu-id="2bbe8-105">ClearByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2bbe8-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bbe8-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bbe8-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bbe8-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bbe8-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bbe8-108">설명</span><span class="sxs-lookup"><span data-stu-id="2bbe8-108">DESCRIPTION</span></span>
<span data-ttu-id="2bbe8-109">**Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse 분석 작업 영역에서 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="2bbe8-110">예제</span><span class="sxs-lookup"><span data-stu-id="2bbe8-110">EXAMPLES</span></span>

### <span data-ttu-id="2bbe8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2bbe8-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2bbe8-112">이 명령은 ContosoWorkspace라는 작업 영역의 고급 위협 보호 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2bbe8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bbe8-113">PARAMETERS</span></span>

### <span data-ttu-id="2bbe8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bbe8-114">-AsJob</span></span>
<span data-ttu-id="2bbe8-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2bbe8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bbe8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bbe8-116">-DefaultProfile</span></span>
<span data-ttu-id="2bbe8-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bbe8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bbe8-118">-InputObject</span></span>
<span data-ttu-id="2bbe8-119">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2bbe8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bbe8-120">-PassThru</span></span>
<span data-ttu-id="2bbe8-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="2bbe8-122">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2bbe8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bbe8-123">-ResourceGroupName</span></span>
<span data-ttu-id="2bbe8-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-124">Resource group name.</span></span>

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

### <span data-ttu-id="2bbe8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bbe8-125">-ResourceId</span></span>
<span data-ttu-id="2bbe8-126">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="2bbe8-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2bbe8-127">-WorkspaceName</span></span>
<span data-ttu-id="2bbe8-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2bbe8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bbe8-129">-Confirm</span></span>
<span data-ttu-id="2bbe8-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bbe8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bbe8-131">-WhatIf</span></span>
<span data-ttu-id="2bbe8-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2bbe8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bbe8-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bbe8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bbe8-134">CommonParameters</span></span>
<span data-ttu-id="2bbe8-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bbe8-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2bbe8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bbe8-137">입력</span><span class="sxs-lookup"><span data-stu-id="2bbe8-137">INPUTS</span></span>

### <span data-ttu-id="2bbe8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bbe8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2bbe8-139">출력</span><span class="sxs-lookup"><span data-stu-id="2bbe8-139">OUTPUTS</span></span>

### <span data-ttu-id="2bbe8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bbe8-140">System.Boolean</span></span>

## <span data-ttu-id="2bbe8-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2bbe8-141">NOTES</span></span>

## <span data-ttu-id="2bbe8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bbe8-142">RELATED LINKS</span></span>
