---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384133"
---
# <span data-ttu-id="b7d4a-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b7d4a-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="b7d4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d4a-103">작업 영역의 고급 데이터 보안을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="b7d4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7d4a-104">SYNTAX</span></span>

### <span data-ttu-id="b7d4a-105">EnableByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7d4a-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7d4a-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d4a-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7d4a-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d4a-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7d4a-108">설명</span><span class="sxs-lookup"><span data-stu-id="b7d4a-108">DESCRIPTION</span></span>
<span data-ttu-id="b7d4a-109">**Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet을 사용하면 작업 영역의 고급 데이터 보안을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="b7d4a-110">고급 데이터 보안은 작업 영역의 데이터 분류, 취약성 평가 및 Advanced Threat Protection을 포함하는 통합 보안 패키지입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="b7d4a-111">(취약성 평가를 저장하기 위해 새 저장소 계정이 자동으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="b7d4a-112">저장소 계정이 이 용도로 이전에 만들어진 경우 대신 사용됩니다.)</span><span class="sxs-lookup"><span data-stu-id="b7d4a-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="b7d4a-113">예제</span><span class="sxs-lookup"><span data-stu-id="b7d4a-113">EXAMPLES</span></span>

### <span data-ttu-id="b7d4a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7d4a-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b7d4a-115">이 명령은 작업 영역 Advanced Data Security를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="b7d4a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="b7d4a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="b7d4a-117">이 명령은 파이프라인을 통해 작업 영역 Advanced Data Security를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="b7d4a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="b7d4a-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="b7d4a-119">이 명령은 파이프라인을 통해 작업 영역 Advanced Data Security를 사용하도록 설정하고 취약성 평가를 자동으로 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="b7d4a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d4a-120">PARAMETERS</span></span>

### <span data-ttu-id="b7d4a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7d4a-121">-AsJob</span></span>
<span data-ttu-id="b7d4a-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b7d4a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7d4a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d4a-123">-DefaultProfile</span></span>
<span data-ttu-id="b7d4a-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d4a-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b7d4a-125">-DeploymentName</span></span>
<span data-ttu-id="b7d4a-126">고급 데이터 보안 배포에 대한 사용자 지정 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="b7d4a-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="b7d4a-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="b7d4a-128">취약성 평가를 자동으로 사용하도록 설정하지 않습니다(저장소 계정은 만들지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="b7d4a-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="b7d4a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7d4a-129">-InputObject</span></span>
<span data-ttu-id="b7d4a-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d4a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d4a-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7d4a-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d4a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7d4a-133">-ResourceId</span></span>
<span data-ttu-id="b7d4a-134">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d4a-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b7d4a-135">-WorkspaceName</span></span>
<span data-ttu-id="b7d4a-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d4a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7d4a-137">-Confirm</span></span>
<span data-ttu-id="b7d4a-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d4a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d4a-139">-WhatIf</span></span>
<span data-ttu-id="b7d4a-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7d4a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d4a-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d4a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d4a-142">CommonParameters</span></span>
<span data-ttu-id="b7d4a-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d4a-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7d4a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d4a-145">입력</span><span class="sxs-lookup"><span data-stu-id="b7d4a-145">INPUTS</span></span>

### <span data-ttu-id="b7d4a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b7d4a-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b7d4a-147">출력</span><span class="sxs-lookup"><span data-stu-id="b7d4a-147">OUTPUTS</span></span>

### <span data-ttu-id="b7d4a-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7d4a-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b7d4a-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7d4a-149">NOTES</span></span>

## <span data-ttu-id="b7d4a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7d4a-150">RELATED LINKS</span></span>
