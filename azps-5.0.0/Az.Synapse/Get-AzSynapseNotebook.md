---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309838"
---
# <span data-ttu-id="a7472-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="a7472-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="a7472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7472-102">SYNOPSIS</span></span>
<span data-ttu-id="a7472-103">작업 영역의 전자 필기장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="a7472-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7472-104">SYNTAX</span></span>

### <span data-ttu-id="a7472-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a7472-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7472-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a7472-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7472-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a7472-107">DESCRIPTION</span></span>
<span data-ttu-id="a7472-108">**AzSynapseNotebook** cmdlet은 작업 영역의 전자 필기장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="a7472-109">전자 필기장의 이름을 지정 하는 경우 cmdlet은 해당 전자 필기장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="a7472-110">이름을 지정 하지 않으면 cmdlet은 작업 영역의 모든 전자 필기장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="a7472-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a7472-111">EXAMPLES</span></span>

### <span data-ttu-id="a7472-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7472-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="a7472-113">작업 영역 ContosoWorkspace의 모든 전자 필기장 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a7472-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a7472-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="a7472-115">작업 영역 ContosoWorkspace에서 ContosoNotebook 이라는 단일 전자 필기장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a7472-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="a7472-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="a7472-117">Workspace ContosoWorkspace to 파이프라인에서 ContosoNotebook 이라는 단일 전자 필기장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a7472-118">변수</span><span class="sxs-lookup"><span data-stu-id="a7472-118">PARAMETERS</span></span>

### <span data-ttu-id="a7472-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7472-119">-DefaultProfile</span></span>
<span data-ttu-id="a7472-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7472-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a7472-121">-Name</span></span>
<span data-ttu-id="a7472-122">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-122">The notebook name.</span></span>

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

### <span data-ttu-id="a7472-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a7472-123">-WorkspaceName</span></span>
<span data-ttu-id="a7472-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a7472-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a7472-125">-WorkspaceObject</span></span>
<span data-ttu-id="a7472-126">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a7472-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7472-127">CommonParameters</span></span>
<span data-ttu-id="a7472-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7472-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7472-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7472-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7472-130">입력</span><span class="sxs-lookup"><span data-stu-id="a7472-130">INPUTS</span></span>

### <span data-ttu-id="a7472-131">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="a7472-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a7472-132">출력</span><span class="sxs-lookup"><span data-stu-id="a7472-132">OUTPUTS</span></span>

### <span data-ttu-id="a7472-133">Synapse. PSNotebookResource/.</span><span class="sxs-lookup"><span data-stu-id="a7472-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="a7472-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a7472-134">NOTES</span></span>

## <span data-ttu-id="a7472-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7472-135">RELATED LINKS</span></span>
