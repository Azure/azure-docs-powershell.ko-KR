---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491092"
---
# <span data-ttu-id="c8910-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="c8910-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="c8910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8910-102">SYNOPSIS</span></span>
<span data-ttu-id="c8910-103">작업 영역의 전자 필기장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="c8910-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8910-104">SYNTAX</span></span>

### <span data-ttu-id="c8910-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c8910-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8910-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="c8910-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8910-107">설명</span><span class="sxs-lookup"><span data-stu-id="c8910-107">DESCRIPTION</span></span>
<span data-ttu-id="c8910-108">**Get-AzSynapseNotebook** cmdlet은 작업 영역의 Notebook에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="c8910-109">전자 필기장의 이름을 지정하면 cmdlet에서 해당 전자 필기장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="c8910-110">이름을 지정하지 않으면 cmdlet은 작업 영역의 모든 Notebook에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="c8910-111">예제</span><span class="sxs-lookup"><span data-stu-id="c8910-111">EXAMPLES</span></span>

### <span data-ttu-id="c8910-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c8910-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="c8910-113">작업 영역 ContosoWorkspace의 모든 Notebook 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c8910-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c8910-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="c8910-115">작업 영역 ContosoWorkspace에서 ContosoNotebook이라는 단일 Notebook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c8910-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c8910-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="c8910-117">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoNotebook이라는 단일 Notebook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c8910-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8910-118">PARAMETERS</span></span>

### <span data-ttu-id="c8910-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8910-119">-DefaultProfile</span></span>
<span data-ttu-id="c8910-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8910-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c8910-121">-Name</span></span>
<span data-ttu-id="c8910-122">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8910-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c8910-123">-WorkspaceName</span></span>
<span data-ttu-id="c8910-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c8910-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c8910-125">-WorkspaceObject</span></span>
<span data-ttu-id="c8910-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8910-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8910-127">CommonParameters</span></span>
<span data-ttu-id="c8910-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8910-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8910-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8910-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8910-130">입력</span><span class="sxs-lookup"><span data-stu-id="c8910-130">INPUTS</span></span>

### <span data-ttu-id="c8910-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8910-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c8910-132">출력</span><span class="sxs-lookup"><span data-stu-id="c8910-132">OUTPUTS</span></span>

### <span data-ttu-id="c8910-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="c8910-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="c8910-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8910-134">NOTES</span></span>

## <span data-ttu-id="c8910-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8910-135">RELATED LINKS</span></span>
