---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: fbdca80b33dd15e34a958cb63a41377b400d03ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207616"
---
# <span data-ttu-id="6a227-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a227-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="6a227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a227-102">SYNOPSIS</span></span>
<span data-ttu-id="6a227-103">Synapse Analytics 작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="6a227-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a227-104">SYNTAX</span></span>

### <span data-ttu-id="6a227-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6a227-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a227-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a227-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a227-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a227-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a227-108">설명</span><span class="sxs-lookup"><span data-stu-id="6a227-108">DESCRIPTION</span></span>
<span data-ttu-id="6a227-109">**Remove-AzSynapseWorkspace** cmdlet은 Azure Synapse Analytics 작업 영역이 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="6a227-110">예제</span><span class="sxs-lookup"><span data-stu-id="6a227-110">EXAMPLES</span></span>

### <span data-ttu-id="6a227-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a227-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="6a227-112">이 명령은 Azure Synapse Analytics 작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="6a227-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6a227-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="6a227-114">이 명령은 파이프라인을 통해 Azure Synapse Analytics 작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="6a227-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6a227-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="6a227-116">이 명령은 지정된 리소스 ID를 사용하여 파이프라인을 통해 Azure Synapse Analytics 작업 영역이 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="6a227-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a227-117">PARAMETERS</span></span>

### <span data-ttu-id="6a227-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a227-118">-AsJob</span></span>
<span data-ttu-id="6a227-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6a227-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a227-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a227-120">-DefaultProfile</span></span>
<span data-ttu-id="6a227-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a227-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6a227-122">-Force</span></span>
<span data-ttu-id="6a227-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6a227-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a227-124">-InputObject</span></span>
<span data-ttu-id="6a227-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a227-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6a227-126">-Name</span></span>
<span data-ttu-id="6a227-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a227-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a227-128">-PassThru</span></span>
<span data-ttu-id="6a227-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-129">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6a227-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6a227-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a227-131">-ResourceGroupName</span></span>
<span data-ttu-id="6a227-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a227-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a227-133">-ResourceId</span></span>
<span data-ttu-id="6a227-134">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a227-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a227-135">-Confirm</span></span>
<span data-ttu-id="6a227-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a227-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a227-137">-WhatIf</span></span>
<span data-ttu-id="6a227-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6a227-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a227-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a227-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a227-140">CommonParameters</span></span>
<span data-ttu-id="6a227-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a227-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a227-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a227-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a227-143">입력</span><span class="sxs-lookup"><span data-stu-id="6a227-143">INPUTS</span></span>

### <span data-ttu-id="6a227-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a227-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6a227-145">출력</span><span class="sxs-lookup"><span data-stu-id="6a227-145">OUTPUTS</span></span>

### <span data-ttu-id="6a227-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6a227-146">System.Boolean</span></span>

## <span data-ttu-id="6a227-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a227-147">NOTES</span></span>

## <span data-ttu-id="6a227-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a227-148">RELATED LINKS</span></span>
