---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963456"
---
# <span data-ttu-id="d74ec-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="d74ec-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="d74ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d74ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d74ec-103">작업 영역에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="d74ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="d74ec-104">SYNTAX</span></span>

### <span data-ttu-id="d74ec-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d74ec-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74ec-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d74ec-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74ec-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="d74ec-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74ec-108">설명</span><span class="sxs-lookup"><span data-stu-id="d74ec-108">DESCRIPTION</span></span>
<span data-ttu-id="d74ec-109">**Remove-AzSynapseDataset** cmdlet은 작업 영역에서 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="d74ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="d74ec-110">EXAMPLES</span></span>

### <span data-ttu-id="d74ec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d74ec-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="d74ec-112">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoDataset이라는 데이터 세트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d74ec-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d74ec-113">PARAMETERS</span></span>

### <span data-ttu-id="d74ec-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74ec-114">-AsJob</span></span>
<span data-ttu-id="d74ec-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d74ec-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74ec-116">-DefaultProfile</span></span>
<span data-ttu-id="d74ec-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74ec-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d74ec-118">-Force</span></span>
<span data-ttu-id="d74ec-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d74ec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74ec-120">-InputObject</span></span>
<span data-ttu-id="d74ec-121">데이터 세트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-121">The dataset object.</span></span>

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

### <span data-ttu-id="d74ec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d74ec-122">-Name</span></span>
<span data-ttu-id="d74ec-123">데이터 세트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-123">The dataset name.</span></span>

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

### <span data-ttu-id="d74ec-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d74ec-124">-PassThru</span></span>
<span data-ttu-id="d74ec-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d74ec-126">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d74ec-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d74ec-127">-WorkspaceName</span></span>
<span data-ttu-id="d74ec-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d74ec-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d74ec-129">-WorkspaceObject</span></span>
<span data-ttu-id="d74ec-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d74ec-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d74ec-131">-Confirm</span></span>
<span data-ttu-id="d74ec-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74ec-133">-WhatIf</span></span>
<span data-ttu-id="d74ec-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74ec-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74ec-136">CommonParameters</span></span>
<span data-ttu-id="d74ec-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d74ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74ec-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d74ec-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74ec-139">입력</span><span class="sxs-lookup"><span data-stu-id="d74ec-139">INPUTS</span></span>

### <span data-ttu-id="d74ec-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d74ec-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d74ec-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="d74ec-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="d74ec-142">출력</span><span class="sxs-lookup"><span data-stu-id="d74ec-142">OUTPUTS</span></span>

### <span data-ttu-id="d74ec-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d74ec-143">System.Boolean</span></span>

## <span data-ttu-id="d74ec-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d74ec-144">NOTES</span></span>

## <span data-ttu-id="d74ec-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d74ec-145">RELATED LINKS</span></span>
