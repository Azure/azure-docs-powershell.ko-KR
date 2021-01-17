---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTrigger.md
ms.openlocfilehash: 9e39d6458ca330909e500a45532d0a9d66f404af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359339"
---
# <span data-ttu-id="7aebf-101">Get-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="7aebf-101">Get-AzSynapseTrigger</span></span>

## <span data-ttu-id="7aebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aebf-102">SYNOPSIS</span></span>
<span data-ttu-id="7aebf-103">작업 영역의 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-103">Gets information about triggers in a workspace.</span></span>

## <span data-ttu-id="7aebf-104">구문</span><span class="sxs-lookup"><span data-stu-id="7aebf-104">SYNTAX</span></span>

### <span data-ttu-id="7aebf-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7aebf-105">GetByName (Default)</span></span>
```
Get-AzSynapseTrigger -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aebf-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="7aebf-106">GetByObject</span></span>
```
Get-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aebf-107">설명</span><span class="sxs-lookup"><span data-stu-id="7aebf-107">DESCRIPTION</span></span>
<span data-ttu-id="7aebf-108">**Get-AzSynapseTrigger** cmdlet은 작업 영역의 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-108">The **Get-AzSynapseTrigger** cmdlet gets information about triggers in a workspace.</span></span> <span data-ttu-id="7aebf-109">트리거의 이름을 지정하는 경우 cmdlet은 해당 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-109">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="7aebf-110">이름을 지정하지 않으면 cmdlet은 작업 영역의 모든 트리거에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-110">If you do not specify a name, the cmdlet gets information about all triggers in the workspace.</span></span>

## <span data-ttu-id="7aebf-111">예제</span><span class="sxs-lookup"><span data-stu-id="7aebf-111">EXAMPLES</span></span>

### <span data-ttu-id="7aebf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7aebf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7aebf-113">작업 영역 ContosoWorkspace에서 만든 모든 트리거 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-113">Gets a list of all triggers that have been created in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7aebf-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="7aebf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="7aebf-115">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 단일 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-115">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="7aebf-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="7aebf-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="7aebf-117">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 단일 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-117">Gets a single trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7aebf-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aebf-118">PARAMETERS</span></span>

### <span data-ttu-id="7aebf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aebf-119">-DefaultProfile</span></span>
<span data-ttu-id="7aebf-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aebf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7aebf-121">-Name</span></span>
<span data-ttu-id="7aebf-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-122">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aebf-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7aebf-123">-WorkspaceName</span></span>
<span data-ttu-id="7aebf-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7aebf-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7aebf-125">-WorkspaceObject</span></span>
<span data-ttu-id="7aebf-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7aebf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aebf-127">CommonParameters</span></span>
<span data-ttu-id="7aebf-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7aebf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aebf-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7aebf-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aebf-130">입력</span><span class="sxs-lookup"><span data-stu-id="7aebf-130">INPUTS</span></span>

### <span data-ttu-id="7aebf-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7aebf-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7aebf-132">출력</span><span class="sxs-lookup"><span data-stu-id="7aebf-132">OUTPUTS</span></span>

### <span data-ttu-id="7aebf-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="7aebf-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="7aebf-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7aebf-134">NOTES</span></span>

## <span data-ttu-id="7aebf-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7aebf-135">RELATED LINKS</span></span>
