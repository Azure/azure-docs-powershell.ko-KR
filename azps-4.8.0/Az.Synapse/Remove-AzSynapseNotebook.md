---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseNotebook.md
ms.openlocfilehash: 22570fa8d236675a8ad2acd712e1ff66c1bc5049
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056628"
---
# <span data-ttu-id="52c11-101">Remove-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="52c11-101">Remove-AzSynapseNotebook</span></span>

## <span data-ttu-id="52c11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c11-102">SYNOPSIS</span></span>
<span data-ttu-id="52c11-103">작업 영역에서 전자 필기장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-103">Removes a notebook from a workspace.</span></span>

## <span data-ttu-id="52c11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52c11-104">SYNTAX</span></span>

### <span data-ttu-id="52c11-105">RemoveByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="52c11-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseNotebook -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c11-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="52c11-106">RemoveByObject</span></span>
```
Remove-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c11-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="52c11-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseNotebook -InputObject <PSNotebookResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c11-108">설명은</span><span class="sxs-lookup"><span data-stu-id="52c11-108">DESCRIPTION</span></span>
<span data-ttu-id="52c11-109">**AzSynapseNotebook** cmdlet은 작업 영역의 전자 필기장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-109">The **Remove-AzSynapseNotebook** cmdlet removes a notebook from a workspace.</span></span>

## <span data-ttu-id="52c11-110">예제의</span><span class="sxs-lookup"><span data-stu-id="52c11-110">EXAMPLES</span></span>

### <span data-ttu-id="52c11-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="52c11-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="52c11-112">작업 영역 ContosoWorkspace에서 ContosoNotebook 이라는 전자 필기장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-112">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="52c11-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="52c11-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="52c11-114">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoNotebook 이라는 전자 필기장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-114">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="52c11-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="52c11-115">Example 3</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Remove-AzSynapseNotebook
```

<span data-ttu-id="52c11-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoNotebook 이라는 전자 필기장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-116">Remove a notebook called ContosoNotebook from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="52c11-117">변수</span><span class="sxs-lookup"><span data-stu-id="52c11-117">PARAMETERS</span></span>

### <span data-ttu-id="52c11-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52c11-118">-AsJob</span></span>
<span data-ttu-id="52c11-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="52c11-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52c11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c11-120">-DefaultProfile</span></span>
<span data-ttu-id="52c11-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c11-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52c11-122">-InputObject</span></span>
<span data-ttu-id="52c11-123">전자 필기장 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-123">The notebook object.</span></span>

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

### <span data-ttu-id="52c11-124">-이름</span><span class="sxs-lookup"><span data-stu-id="52c11-124">-Name</span></span>
<span data-ttu-id="52c11-125">전자 필기장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-125">The notebook name.</span></span>

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

### <span data-ttu-id="52c11-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52c11-126">-PassThru</span></span>
<span data-ttu-id="52c11-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="52c11-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="52c11-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52c11-129">-WorkspaceName</span></span>
<span data-ttu-id="52c11-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="52c11-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="52c11-131">-WorkspaceObject</span></span>
<span data-ttu-id="52c11-132">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="52c11-133">-확인</span><span class="sxs-lookup"><span data-stu-id="52c11-133">-Confirm</span></span>
<span data-ttu-id="52c11-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c11-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c11-135">-WhatIf</span></span>
<span data-ttu-id="52c11-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52c11-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c11-138">CommonParameters</span></span>
<span data-ttu-id="52c11-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52c11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c11-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52c11-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c11-141">입력</span><span class="sxs-lookup"><span data-stu-id="52c11-141">INPUTS</span></span>

### <span data-ttu-id="52c11-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="52c11-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="52c11-143">Synapse. PSNotebookResource/.</span><span class="sxs-lookup"><span data-stu-id="52c11-143">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="52c11-144">출력</span><span class="sxs-lookup"><span data-stu-id="52c11-144">OUTPUTS</span></span>

### <span data-ttu-id="52c11-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="52c11-145">System.Boolean</span></span>

## <span data-ttu-id="52c11-146">상속자</span><span class="sxs-lookup"><span data-stu-id="52c11-146">NOTES</span></span>

## <span data-ttu-id="52c11-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52c11-147">RELATED LINKS</span></span>
