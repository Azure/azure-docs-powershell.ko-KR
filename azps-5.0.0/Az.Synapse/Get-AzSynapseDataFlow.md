---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216501"
---
# <span data-ttu-id="7ed2c-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="7ed2c-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="7ed2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed2c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed2c-103">작업 영역의 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="7ed2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ed2c-104">SYNTAX</span></span>

### <span data-ttu-id="7ed2c-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ed2c-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ed2c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="7ed2c-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed2c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ed2c-107">DESCRIPTION</span></span>
<span data-ttu-id="7ed2c-108">**AzSynapseDataFlow** cmdlet은 작업 영역의 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="7ed2c-109">데이터 흐름의 이름을 지정 하는 경우이 cmdlet은 해당 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="7ed2c-110">이름을 지정 하지 않으면이 cmdlet은 작업 영역의 모든 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="7ed2c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7ed2c-111">EXAMPLES</span></span>

### <span data-ttu-id="7ed2c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7ed2c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7ed2c-113">이 명령은 ContosoWorkspace 이라는 작업 영역의 모든 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7ed2c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="7ed2c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="7ed2c-115">이 명령은 ContosoWorkspace 이라는 작업 영역의 ContosoDataFlow 이라는 데이터 흐름에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7ed2c-116">변수</span><span class="sxs-lookup"><span data-stu-id="7ed2c-116">PARAMETERS</span></span>

### <span data-ttu-id="7ed2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed2c-117">-DefaultProfile</span></span>
<span data-ttu-id="7ed2c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed2c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7ed2c-119">-Name</span></span>
<span data-ttu-id="7ed2c-120">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-120">The data flow name.</span></span>

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

### <span data-ttu-id="7ed2c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7ed2c-121">-WorkspaceName</span></span>
<span data-ttu-id="7ed2c-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7ed2c-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7ed2c-123">-WorkspaceObject</span></span>
<span data-ttu-id="7ed2c-124">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7ed2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed2c-125">CommonParameters</span></span>
<span data-ttu-id="7ed2c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed2c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed2c-128">입력</span><span class="sxs-lookup"><span data-stu-id="7ed2c-128">INPUTS</span></span>

### <span data-ttu-id="7ed2c-129">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7ed2c-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7ed2c-130">출력</span><span class="sxs-lookup"><span data-stu-id="7ed2c-130">OUTPUTS</span></span>

### <span data-ttu-id="7ed2c-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="7ed2c-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="7ed2c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7ed2c-132">NOTES</span></span>

## <span data-ttu-id="7ed2c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ed2c-133">RELATED LINKS</span></span>
