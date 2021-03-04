---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 6203143eb2d386b627d0208730987709b1dd68c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983947"
---
# <span data-ttu-id="17b9a-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="17b9a-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="17b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="17b9a-103">작업 영역에서 전자 필기장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="17b9a-104">구문</span><span class="sxs-lookup"><span data-stu-id="17b9a-104">SYNTAX</span></span>

### <span data-ttu-id="17b9a-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="17b9a-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="17b9a-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17b9a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="17b9a-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17b9a-108">설명</span><span class="sxs-lookup"><span data-stu-id="17b9a-108">DESCRIPTION</span></span>
<span data-ttu-id="17b9a-109">**Remove-AzSynapseNotebook** cmdlet은 작업 영역에서 전자 필기장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="17b9a-110">예제</span><span class="sxs-lookup"><span data-stu-id="17b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="17b9a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="17b9a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="17b9a-112">작업 영역 ContosoWorkspace에서 ContosoNotebook이라는 전자 필기장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="17b9a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="17b9a-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="17b9a-114">작업 영역 ContosoWorkspace에서 파이프라인을 통해 ContosoNotebook이라는 전자 필기장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="17b9a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="17b9a-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="17b9a-116">작업 영역 ContosoWorkspace에서 파이프라인을 통해 ContosoNotebook이라는 전자 필기장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="17b9a-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="17b9a-117">PARAMETERS</span></span>

### <span data-ttu-id="17b9a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17b9a-118">-AsJob</span></span>
<span data-ttu-id="17b9a-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="17b9a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17b9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b9a-120">-DefaultProfile</span></span>
<span data-ttu-id="17b9a-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17b9a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="17b9a-122">-Force</span></span>
<span data-ttu-id="17b9a-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="17b9a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17b9a-124">-InputObject</span></span>
<span data-ttu-id="17b9a-125">전자 필기장 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-125">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b9a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="17b9a-126">-Name</span></span>
<span data-ttu-id="17b9a-127">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-127">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: NotebookName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b9a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17b9a-128">-PassThru</span></span>
<span data-ttu-id="17b9a-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="17b9a-130">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="17b9a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17b9a-131">-WorkspaceName</span></span>
<span data-ttu-id="17b9a-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b9a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="17b9a-133">-WorkspaceObject</span></span>
<span data-ttu-id="17b9a-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17b9a-135">-확인</span><span class="sxs-lookup"><span data-stu-id="17b9a-135">-Confirm</span></span>
<span data-ttu-id="17b9a-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b9a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b9a-137">-WhatIf</span></span>
<span data-ttu-id="17b9a-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17b9a-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b9a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b9a-140">CommonParameters</span></span>
<span data-ttu-id="17b9a-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17b9a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b9a-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17b9a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b9a-143">입력</span><span class="sxs-lookup"><span data-stu-id="17b9a-143">INPUTS</span></span>

### <span data-ttu-id="17b9a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="17b9a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="17b9a-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="17b9a-145">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="17b9a-146">출력</span><span class="sxs-lookup"><span data-stu-id="17b9a-146">OUTPUTS</span></span>

### <span data-ttu-id="17b9a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17b9a-147">System.Boolean</span></span>

## <span data-ttu-id="17b9a-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17b9a-148">NOTES</span></span>

## <span data-ttu-id="17b9a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17b9a-149">RELATED LINKS</span></span>
