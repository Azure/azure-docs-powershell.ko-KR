---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198332"
---
# <span data-ttu-id="35f47-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="35f47-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="35f47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f47-102">SYNOPSIS</span></span>
<span data-ttu-id="35f47-103">작업 영역의 데이터 세트를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="35f47-104">구문</span><span class="sxs-lookup"><span data-stu-id="35f47-104">SYNTAX</span></span>

### <span data-ttu-id="35f47-105">SetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="35f47-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35f47-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="35f47-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f47-107">설명</span><span class="sxs-lookup"><span data-stu-id="35f47-107">DESCRIPTION</span></span>
<span data-ttu-id="35f47-108">**Set-AzSynapseDataset** cmdlet은 데이터 세트를 생성하거나 작업 영역의 기존 데이터 세트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="35f47-109">예제</span><span class="sxs-lookup"><span data-stu-id="35f47-109">EXAMPLES</span></span>

### <span data-ttu-id="35f47-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="35f47-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="35f47-111">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoDataset이라는 데이터 세트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="35f47-112">이 명령은 데이터 세트를 on 파일의 Dataset.js기반입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="35f47-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35f47-113">PARAMETERS</span></span>

### <span data-ttu-id="35f47-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f47-114">-AsJob</span></span>
<span data-ttu-id="35f47-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="35f47-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35f47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f47-116">-DefaultProfile</span></span>
<span data-ttu-id="35f47-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f47-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="35f47-118">-DefinitionFile</span></span>
<span data-ttu-id="35f47-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-119">The JSON file path.</span></span>

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

### <span data-ttu-id="35f47-120">-Name</span><span class="sxs-lookup"><span data-stu-id="35f47-120">-Name</span></span>
<span data-ttu-id="35f47-121">데이터 세트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-121">The dataset name.</span></span>

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

### <span data-ttu-id="35f47-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35f47-122">-WorkspaceName</span></span>
<span data-ttu-id="35f47-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="35f47-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35f47-124">-WorkspaceObject</span></span>
<span data-ttu-id="35f47-125">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="35f47-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35f47-126">-Confirm</span></span>
<span data-ttu-id="35f47-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f47-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f47-128">-WhatIf</span></span>
<span data-ttu-id="35f47-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="35f47-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f47-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f47-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f47-131">CommonParameters</span></span>
<span data-ttu-id="35f47-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35f47-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f47-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35f47-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f47-134">입력</span><span class="sxs-lookup"><span data-stu-id="35f47-134">INPUTS</span></span>

### <span data-ttu-id="35f47-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35f47-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="35f47-136">출력</span><span class="sxs-lookup"><span data-stu-id="35f47-136">OUTPUTS</span></span>

### <span data-ttu-id="35f47-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="35f47-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="35f47-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35f47-138">NOTES</span></span>

## <span data-ttu-id="35f47-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35f47-139">RELATED LINKS</span></span>
