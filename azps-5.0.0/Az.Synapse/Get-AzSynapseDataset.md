---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216500"
---
# <span data-ttu-id="97651-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="97651-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="97651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97651-102">SYNOPSIS</span></span>
<span data-ttu-id="97651-103">작업 영역의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="97651-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97651-104">SYNTAX</span></span>

### <span data-ttu-id="97651-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="97651-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97651-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="97651-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97651-107">설명은</span><span class="sxs-lookup"><span data-stu-id="97651-107">DESCRIPTION</span></span>
<span data-ttu-id="97651-108">**AzSynapseDataset** cmdlet은 작업 영역의 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="97651-109">데이터 집합의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="97651-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="97651-111">예제의</span><span class="sxs-lookup"><span data-stu-id="97651-111">EXAMPLES</span></span>

### <span data-ttu-id="97651-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="97651-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="97651-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 모든 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="97651-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="97651-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="97651-115">이 명령은 ContosoWorkspace 이라는 작업 영역의 ContosoDataset 이라는 데이터 집합에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="97651-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="97651-116">변수</span><span class="sxs-lookup"><span data-stu-id="97651-116">PARAMETERS</span></span>

### <span data-ttu-id="97651-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97651-117">-DefaultProfile</span></span>
<span data-ttu-id="97651-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97651-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97651-119">-이름</span><span class="sxs-lookup"><span data-stu-id="97651-119">-Name</span></span>
<span data-ttu-id="97651-120">데이터 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97651-120">The dataset name.</span></span>

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

### <span data-ttu-id="97651-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="97651-121">-WorkspaceName</span></span>
<span data-ttu-id="97651-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97651-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="97651-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="97651-123">-WorkspaceObject</span></span>
<span data-ttu-id="97651-124">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="97651-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="97651-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97651-125">CommonParameters</span></span>
<span data-ttu-id="97651-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97651-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97651-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97651-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97651-128">입력</span><span class="sxs-lookup"><span data-stu-id="97651-128">INPUTS</span></span>

### <span data-ttu-id="97651-129">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="97651-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="97651-130">출력</span><span class="sxs-lookup"><span data-stu-id="97651-130">OUTPUTS</span></span>

### <span data-ttu-id="97651-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="97651-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="97651-132">상속자</span><span class="sxs-lookup"><span data-stu-id="97651-132">NOTES</span></span>

## <span data-ttu-id="97651-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97651-133">RELATED LINKS</span></span>
