---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 68da67d2a29b6f05ed50adc9eb8aef343a7e973b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182732"
---
# <span data-ttu-id="4c54d-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="4c54d-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="4c54d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c54d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c54d-103">작업 영역의 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="4c54d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c54d-104">SYNTAX</span></span>

### <span data-ttu-id="4c54d-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4c54d-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c54d-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="4c54d-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c54d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4c54d-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c54d-108">설명</span><span class="sxs-lookup"><span data-stu-id="4c54d-108">DESCRIPTION</span></span>
<span data-ttu-id="4c54d-109">**Remove-AzSynapseDataset** cmdlet은 작업 영역의 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="4c54d-110">예제</span><span class="sxs-lookup"><span data-stu-id="4c54d-110">EXAMPLES</span></span>

### <span data-ttu-id="4c54d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c54d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="4c54d-112">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoDataset이라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4c54d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c54d-113">PARAMETERS</span></span>

### <span data-ttu-id="4c54d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c54d-114">-AsJob</span></span>
<span data-ttu-id="4c54d-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4c54d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c54d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c54d-116">-DefaultProfile</span></span>
<span data-ttu-id="4c54d-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c54d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4c54d-118">-Force</span></span>
<span data-ttu-id="4c54d-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4c54d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c54d-120">-InputObject</span></span>
<span data-ttu-id="4c54d-121">데이터 세트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c54d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4c54d-122">-Name</span></span>
<span data-ttu-id="4c54d-123">데이터 세트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c54d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c54d-124">-PassThru</span></span>
<span data-ttu-id="4c54d-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4c54d-126">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4c54d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4c54d-127">-WorkspaceName</span></span>
<span data-ttu-id="4c54d-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c54d-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4c54d-129">-WorkspaceObject</span></span>
<span data-ttu-id="4c54d-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c54d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c54d-131">-Confirm</span></span>
<span data-ttu-id="4c54d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c54d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c54d-133">-WhatIf</span></span>
<span data-ttu-id="4c54d-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4c54d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c54d-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c54d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c54d-136">CommonParameters</span></span>
<span data-ttu-id="4c54d-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c54d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c54d-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c54d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c54d-139">입력</span><span class="sxs-lookup"><span data-stu-id="4c54d-139">INPUTS</span></span>

### <span data-ttu-id="4c54d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4c54d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4c54d-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="4c54d-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="4c54d-142">출력</span><span class="sxs-lookup"><span data-stu-id="4c54d-142">OUTPUTS</span></span>

### <span data-ttu-id="4c54d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c54d-143">System.Boolean</span></span>

## <span data-ttu-id="4c54d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c54d-144">NOTES</span></span>

## <span data-ttu-id="4c54d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c54d-145">RELATED LINKS</span></span>
