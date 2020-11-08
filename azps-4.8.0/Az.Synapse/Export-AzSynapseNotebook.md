---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204697"
---
# <span data-ttu-id="ed6ed-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="ed6ed-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="ed6ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6ed-103">Notbooks를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-103">Exports notbooks.</span></span>

## <span data-ttu-id="ed6ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed6ed-104">SYNTAX</span></span>

### <span data-ttu-id="ed6ed-105">ExportByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ed6ed-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed6ed-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="ed6ed-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed6ed-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed6ed-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6ed-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ed6ed-108">DESCRIPTION</span></span>
<span data-ttu-id="ed6ed-109">**Export-AzSynapseNotebook** Cmdlet은 Azure Synapse 전자 필기장을 전자 필기장 (. ip b) 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="ed6ed-110">전자 필기장의 이름이 내보낸 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="ed6ed-111">전자 필기장의 이름을 지정 하는 경우 cmdlet은 해당 전자 필기장을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="ed6ed-112">이름을 지정 하지 않으면 cmdlet에서 작업 영역의 모든 전자 필기장을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="ed6ed-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ed6ed-113">EXAMPLES</span></span>

### <span data-ttu-id="ed6ed-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed6ed-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ed6ed-115">작업 영역에 있는 모든 전자 필기장을 "C:\Notebook" 폴더로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="ed6ed-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ed6ed-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ed6ed-117">작업 영역에서 ContosoNotebook 이라는 단일 전자 필기장을 "C:\Notebook" 폴더로 내보냅니다 ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="ed6ed-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="ed6ed-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ed6ed-119">작업 영역에서 ContosoNotebook 이라는 단일 전자 필기장을 "C:\Notebook" 폴더에서 파이프라인을 통해 내보내기 ContosoWorkspace 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="ed6ed-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="ed6ed-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="ed6ed-121">작업 영역에서 ContosoNotebook 이라는 단일 전자 필기장을 "C:\Notebook" 폴더에서 파이프라인을 통해 내보내기 ContosoWorkspace 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="ed6ed-122">변수</span><span class="sxs-lookup"><span data-stu-id="ed6ed-122">PARAMETERS</span></span>

### <span data-ttu-id="ed6ed-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed6ed-123">-AsJob</span></span>
<span data-ttu-id="ed6ed-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ed6ed-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed6ed-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6ed-125">-DefaultProfile</span></span>
<span data-ttu-id="ed6ed-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed6ed-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed6ed-127">-InputObject</span></span>
<span data-ttu-id="ed6ed-128">전자 필기장 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6ed-129">-이름</span><span class="sxs-lookup"><span data-stu-id="ed6ed-129">-Name</span></span>
<span data-ttu-id="ed6ed-130">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6ed-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ed6ed-131">-OutputFolder</span></span>
<span data-ttu-id="ed6ed-132">전자 필기장을 배치할 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-132">The folder where the notebook should be placed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6ed-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed6ed-133">-WorkspaceName</span></span>
<span data-ttu-id="ed6ed-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed6ed-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ed6ed-135">-WorkspaceObject</span></span>
<span data-ttu-id="ed6ed-136">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6ed-137">CommonParameters</span></span>
<span data-ttu-id="ed6ed-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6ed-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6ed-140">입력</span><span class="sxs-lookup"><span data-stu-id="ed6ed-140">INPUTS</span></span>

### <span data-ttu-id="ed6ed-141">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ed6ed-142">Synapse. PSNotebookResource/.</span><span class="sxs-lookup"><span data-stu-id="ed6ed-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="ed6ed-143">출력</span><span class="sxs-lookup"><span data-stu-id="ed6ed-143">OUTPUTS</span></span>

### <span data-ttu-id="ed6ed-144">시스템. o. FileInfo</span><span class="sxs-lookup"><span data-stu-id="ed6ed-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="ed6ed-145">상속자</span><span class="sxs-lookup"><span data-stu-id="ed6ed-145">NOTES</span></span>

## <span data-ttu-id="ed6ed-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed6ed-146">RELATED LINKS</span></span>
