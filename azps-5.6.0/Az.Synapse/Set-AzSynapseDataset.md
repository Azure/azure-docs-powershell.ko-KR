---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952971"
---
# <span data-ttu-id="e47c1-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="e47c1-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="e47c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e47c1-103">작업 영역의 데이터 세트를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="e47c1-104">구문</span><span class="sxs-lookup"><span data-stu-id="e47c1-104">SYNTAX</span></span>

### <span data-ttu-id="e47c1-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e47c1-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e47c1-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="e47c1-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e47c1-107">설명</span><span class="sxs-lookup"><span data-stu-id="e47c1-107">DESCRIPTION</span></span>
<span data-ttu-id="e47c1-108">**Set-AzSynapseDataset** cmdlet은 데이터 세트를 생성하거나 작업 영역의 기존 데이터 세트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="e47c1-109">예제</span><span class="sxs-lookup"><span data-stu-id="e47c1-109">EXAMPLES</span></span>

### <span data-ttu-id="e47c1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e47c1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="e47c1-111">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoDataset이라는 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="e47c1-112">명령은 데이터 세트를 on 파일의 Dataset.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="e47c1-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e47c1-113">PARAMETERS</span></span>

### <span data-ttu-id="e47c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e47c1-114">-AsJob</span></span>
<span data-ttu-id="e47c1-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e47c1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e47c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47c1-116">-DefaultProfile</span></span>
<span data-ttu-id="e47c1-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e47c1-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e47c1-118">-DefinitionFile</span></span>
<span data-ttu-id="e47c1-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e47c1-120">-Name</span></span>
<span data-ttu-id="e47c1-121">데이터 세트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c1-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e47c1-122">-WorkspaceName</span></span>
<span data-ttu-id="e47c1-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c1-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e47c1-124">-WorkspaceObject</span></span>
<span data-ttu-id="e47c1-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e47c1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e47c1-126">-Confirm</span></span>
<span data-ttu-id="e47c1-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e47c1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e47c1-128">-WhatIf</span></span>
<span data-ttu-id="e47c1-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e47c1-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e47c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47c1-131">CommonParameters</span></span>
<span data-ttu-id="e47c1-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e47c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47c1-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e47c1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47c1-134">입력</span><span class="sxs-lookup"><span data-stu-id="e47c1-134">INPUTS</span></span>

### <span data-ttu-id="e47c1-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e47c1-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e47c1-136">출력</span><span class="sxs-lookup"><span data-stu-id="e47c1-136">OUTPUTS</span></span>

### <span data-ttu-id="e47c1-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="e47c1-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="e47c1-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e47c1-138">NOTES</span></span>

## <span data-ttu-id="e47c1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e47c1-139">RELATED LINKS</span></span>
