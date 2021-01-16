---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384098"
---
# <span data-ttu-id="100a1-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="100a1-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="100a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="100a1-102">SYNOPSIS</span></span>
<span data-ttu-id="100a1-103">작업 영역의 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="100a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="100a1-104">SYNTAX</span></span>

### <span data-ttu-id="100a1-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="100a1-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="100a1-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="100a1-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="100a1-107">설명</span><span class="sxs-lookup"><span data-stu-id="100a1-107">DESCRIPTION</span></span>
<span data-ttu-id="100a1-108">**Get-AzSynapseDataFlow** cmdlet은 작업 영역의 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="100a1-109">데이터 흐름의 이름을 지정하는 경우 이 cmdlet은 해당 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="100a1-110">이름을 지정하지 않으면 이 cmdlet은 작업 영역의 모든 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="100a1-111">예제</span><span class="sxs-lookup"><span data-stu-id="100a1-111">EXAMPLES</span></span>

### <span data-ttu-id="100a1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="100a1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="100a1-113">이 명령은 ContosoWorkspace라는 작업 영역의 모든 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="100a1-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="100a1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="100a1-115">이 명령은 ContosoWorkspace라는 작업 영역의 ContosoDataFlow라는 데이터 흐름에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="100a1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="100a1-116">PARAMETERS</span></span>

### <span data-ttu-id="100a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100a1-117">-DefaultProfile</span></span>
<span data-ttu-id="100a1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="100a1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="100a1-119">-Name</span></span>
<span data-ttu-id="100a1-120">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="100a1-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="100a1-121">-WorkspaceName</span></span>
<span data-ttu-id="100a1-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="100a1-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="100a1-123">-WorkspaceObject</span></span>
<span data-ttu-id="100a1-124">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="100a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100a1-125">CommonParameters</span></span>
<span data-ttu-id="100a1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="100a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100a1-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="100a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100a1-128">입력</span><span class="sxs-lookup"><span data-stu-id="100a1-128">INPUTS</span></span>

### <span data-ttu-id="100a1-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="100a1-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="100a1-130">출력</span><span class="sxs-lookup"><span data-stu-id="100a1-130">OUTPUTS</span></span>

### <span data-ttu-id="100a1-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="100a1-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="100a1-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="100a1-132">NOTES</span></span>

## <span data-ttu-id="100a1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="100a1-133">RELATED LINKS</span></span>
