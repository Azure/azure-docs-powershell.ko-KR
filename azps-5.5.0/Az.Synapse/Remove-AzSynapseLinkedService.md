---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: c70cc0f8659a04e8a10a4fbd2b776d22fca6a616
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195588"
---
# <span data-ttu-id="7488c-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="7488c-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="7488c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7488c-102">SYNOPSIS</span></span>
<span data-ttu-id="7488c-103">작업 영역에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="7488c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7488c-104">SYNTAX</span></span>

### <span data-ttu-id="7488c-105">RemoveByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7488c-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7488c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7488c-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7488c-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="7488c-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7488c-108">설명</span><span class="sxs-lookup"><span data-stu-id="7488c-108">DESCRIPTION</span></span>
<span data-ttu-id="7488c-109">**Remove-AzSynapseLinkedService** cmdlet은 작업 영역에서 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="7488c-110">예제</span><span class="sxs-lookup"><span data-stu-id="7488c-110">EXAMPLES</span></span>

### <span data-ttu-id="7488c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7488c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="7488c-112">이 명령은 ContosoWorkspace라는 작업 영역에서 ContosoLinkedService라는 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7488c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7488c-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="7488c-114">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역에서 ContosoLinkedService라는 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="7488c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7488c-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="7488c-116">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역에서 ContosoLinkedService라는 연결된 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7488c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7488c-117">PARAMETERS</span></span>

### <span data-ttu-id="7488c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7488c-118">-AsJob</span></span>
<span data-ttu-id="7488c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7488c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7488c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7488c-120">-DefaultProfile</span></span>
<span data-ttu-id="7488c-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7488c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7488c-122">-Force</span></span>
<span data-ttu-id="7488c-123">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7488c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7488c-124">-InputObject</span></span>
<span data-ttu-id="7488c-125">연결된 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-125">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7488c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7488c-126">-Name</span></span>
<span data-ttu-id="7488c-127">연결된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-127">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7488c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7488c-128">-PassThru</span></span>
<span data-ttu-id="7488c-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7488c-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7488c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7488c-131">-WorkspaceName</span></span>
<span data-ttu-id="7488c-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7488c-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7488c-133">-WorkspaceObject</span></span>
<span data-ttu-id="7488c-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7488c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7488c-135">-Confirm</span></span>
<span data-ttu-id="7488c-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7488c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7488c-137">-WhatIf</span></span>
<span data-ttu-id="7488c-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7488c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7488c-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7488c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7488c-140">CommonParameters</span></span>
<span data-ttu-id="7488c-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7488c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7488c-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7488c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7488c-143">입력</span><span class="sxs-lookup"><span data-stu-id="7488c-143">INPUTS</span></span>

### <span data-ttu-id="7488c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7488c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7488c-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="7488c-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="7488c-146">출력</span><span class="sxs-lookup"><span data-stu-id="7488c-146">OUTPUTS</span></span>

### <span data-ttu-id="7488c-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="7488c-147">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="7488c-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7488c-148">NOTES</span></span>

## <span data-ttu-id="7488c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7488c-149">RELATED LINKS</span></span>
