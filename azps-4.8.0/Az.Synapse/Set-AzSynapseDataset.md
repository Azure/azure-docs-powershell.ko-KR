---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213458"
---
# <span data-ttu-id="d2aca-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="d2aca-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="d2aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2aca-102">SYNOPSIS</span></span>
<span data-ttu-id="d2aca-103">작업 영역에서 데이터 집합을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="d2aca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2aca-104">SYNTAX</span></span>

### <span data-ttu-id="d2aca-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2aca-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2aca-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="d2aca-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2aca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2aca-107">DESCRIPTION</span></span>
<span data-ttu-id="d2aca-108">**AzSynapseDataset** cmdlet은 작업 영역에서 데이터 집합을 만들거나 기존 데이터 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="d2aca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2aca-109">EXAMPLES</span></span>

### <span data-ttu-id="d2aca-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2aca-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="d2aca-111">이 명령은 ContosoWorkspace 이라는 작업 영역에 ContosoDataset 이라는 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="d2aca-112">명령은 파일의 Dataset.js정보를 기준으로 데이터 집합을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="d2aca-113">변수</span><span class="sxs-lookup"><span data-stu-id="d2aca-113">PARAMETERS</span></span>

### <span data-ttu-id="d2aca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2aca-114">-AsJob</span></span>
<span data-ttu-id="d2aca-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d2aca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2aca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2aca-116">-DefaultProfile</span></span>
<span data-ttu-id="d2aca-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2aca-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="d2aca-118">-DefinitionFile</span></span>
<span data-ttu-id="d2aca-119">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-119">The JSON file path.</span></span>

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

### <span data-ttu-id="d2aca-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d2aca-120">-Name</span></span>
<span data-ttu-id="d2aca-121">데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-121">The dataset name.</span></span>

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

### <span data-ttu-id="d2aca-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2aca-122">-WorkspaceName</span></span>
<span data-ttu-id="d2aca-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d2aca-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2aca-124">-WorkspaceObject</span></span>
<span data-ttu-id="d2aca-125">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2aca-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d2aca-126">-Confirm</span></span>
<span data-ttu-id="d2aca-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2aca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2aca-128">-WhatIf</span></span>
<span data-ttu-id="d2aca-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2aca-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2aca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2aca-131">CommonParameters</span></span>
<span data-ttu-id="d2aca-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2aca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2aca-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2aca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2aca-134">입력</span><span class="sxs-lookup"><span data-stu-id="d2aca-134">INPUTS</span></span>

### <span data-ttu-id="d2aca-135">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="d2aca-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d2aca-136">출력</span><span class="sxs-lookup"><span data-stu-id="d2aca-136">OUTPUTS</span></span>

### <span data-ttu-id="d2aca-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="d2aca-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="d2aca-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d2aca-138">NOTES</span></span>

## <span data-ttu-id="d2aca-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2aca-139">RELATED LINKS</span></span>
