---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 7d586af76115ddf7cada5a443dd10d51463fe576
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981840"
---
# <span data-ttu-id="db0a9-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="db0a9-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="db0a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="db0a9-103">작업 영역의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="db0a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="db0a9-104">SYNTAX</span></span>

### <span data-ttu-id="db0a9-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="db0a9-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db0a9-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="db0a9-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db0a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="db0a9-107">DESCRIPTION</span></span>
<span data-ttu-id="db0a9-108">**Get-AzSynapseDataset** cmdlet은 작업 영역의 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="db0a9-109">데이터 세트의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="db0a9-110">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="db0a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="db0a9-111">EXAMPLES</span></span>

### <span data-ttu-id="db0a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="db0a9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="db0a9-113">이 명령은 ContosoWorkspace라는 작업 영역의 모든 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="db0a9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="db0a9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="db0a9-115">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoDataset이라는 데이터 세트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="db0a9-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="db0a9-116">PARAMETERS</span></span>

### <span data-ttu-id="db0a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0a9-117">-DefaultProfile</span></span>
<span data-ttu-id="db0a9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db0a9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="db0a9-119">-Name</span></span>
<span data-ttu-id="db0a9-120">데이터 세트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0a9-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db0a9-121">-WorkspaceName</span></span>
<span data-ttu-id="db0a9-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db0a9-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db0a9-123">-WorkspaceObject</span></span>
<span data-ttu-id="db0a9-124">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db0a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0a9-125">CommonParameters</span></span>
<span data-ttu-id="db0a9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db0a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0a9-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db0a9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0a9-128">입력</span><span class="sxs-lookup"><span data-stu-id="db0a9-128">INPUTS</span></span>

### <span data-ttu-id="db0a9-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db0a9-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="db0a9-130">출력</span><span class="sxs-lookup"><span data-stu-id="db0a9-130">OUTPUTS</span></span>

### <span data-ttu-id="db0a9-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="db0a9-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="db0a9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db0a9-132">NOTES</span></span>

## <span data-ttu-id="db0a9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db0a9-133">RELATED LINKS</span></span>
