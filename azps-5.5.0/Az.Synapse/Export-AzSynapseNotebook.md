---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209064"
---
# <span data-ttu-id="78443-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="78443-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="78443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78443-102">SYNOPSIS</span></span>
<span data-ttu-id="78443-103">Notbook을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-103">Exports notbooks.</span></span>

## <span data-ttu-id="78443-104">구문</span><span class="sxs-lookup"><span data-stu-id="78443-104">SYNTAX</span></span>

### <span data-ttu-id="78443-105">ExportByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="78443-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78443-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="78443-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78443-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="78443-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78443-108">설명</span><span class="sxs-lookup"><span data-stu-id="78443-108">DESCRIPTION</span></span>
<span data-ttu-id="78443-109">**Export-AzSynapseNotebook** cmdlet은 Azure Synapse Notebook을 Notebook(.ipynb) 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="78443-110">전자 필기장의 이름은 내보낼 파일의 이름이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78443-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="78443-111">Notebook의 이름을 지정하면 cmdlet에서 해당 Notebook을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="78443-112">이름을 지정하지 않으면 cmdlet은 작업 영역의 모든 Notebook을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="78443-113">예제</span><span class="sxs-lookup"><span data-stu-id="78443-113">EXAMPLES</span></span>

### <span data-ttu-id="78443-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="78443-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="78443-115">작업 영역 ContosoWorkspace의 모든 Notebook을 "C:\Notebook" 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="78443-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="78443-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="78443-117">작업 영역 ContosoWorkspace의 ContosoNotebook이라는 단일 Notebook을 "C:\Notebook" 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="78443-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="78443-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="78443-119">작업 영역 ContosoWorkspace의 ContosoNotebook이라는 단일 Notebook을 파이프라인을 통해 "C:\Notebook" 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="78443-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="78443-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="78443-121">작업 영역 ContosoWorkspace의 ContosoNotebook이라는 단일 Notebook을 파이프라인을 통해 "C:\Notebook" 폴더로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78443-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="78443-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78443-122">PARAMETERS</span></span>

### <span data-ttu-id="78443-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78443-123">-AsJob</span></span>
<span data-ttu-id="78443-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="78443-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78443-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78443-125">-DefaultProfile</span></span>
<span data-ttu-id="78443-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78443-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78443-127">-InputObject</span></span>
<span data-ttu-id="78443-128">Notebook 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-128">The notebook object.</span></span>

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

### <span data-ttu-id="78443-129">-Name</span><span class="sxs-lookup"><span data-stu-id="78443-129">-Name</span></span>
<span data-ttu-id="78443-130">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-130">The notebook name.</span></span>

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

### <span data-ttu-id="78443-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="78443-131">-OutputFolder</span></span>
<span data-ttu-id="78443-132">전자 필기장을 배치해야 하는 폴더입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="78443-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78443-133">-WorkspaceName</span></span>
<span data-ttu-id="78443-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="78443-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="78443-135">-WorkspaceObject</span></span>
<span data-ttu-id="78443-136">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="78443-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="78443-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78443-137">CommonParameters</span></span>
<span data-ttu-id="78443-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78443-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78443-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="78443-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78443-140">입력</span><span class="sxs-lookup"><span data-stu-id="78443-140">INPUTS</span></span>

### <span data-ttu-id="78443-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="78443-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="78443-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="78443-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="78443-143">출력</span><span class="sxs-lookup"><span data-stu-id="78443-143">OUTPUTS</span></span>

### <span data-ttu-id="78443-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="78443-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="78443-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78443-145">NOTES</span></span>

## <span data-ttu-id="78443-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78443-146">RELATED LINKS</span></span>
