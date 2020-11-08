---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataFlow.md
ms.openlocfilehash: dcfcd391d1103b0755a3ffae481e4f1bd5fde2c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226008"
---
# <span data-ttu-id="9f507-101">Remove-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="9f507-101">Remove-AzSynapseDataFlow</span></span>

## <span data-ttu-id="9f507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f507-102">SYNOPSIS</span></span>
<span data-ttu-id="9f507-103">작업 영역에서 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-103">Removes a data flow from workspace.</span></span>

## <span data-ttu-id="9f507-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f507-104">SYNTAX</span></span>

### <span data-ttu-id="9f507-105">RemoveByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f507-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f507-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9f507-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f507-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f507-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataFlow -InputObject <PSDataFlowResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f507-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9f507-108">DESCRIPTION</span></span>
<span data-ttu-id="9f507-109">**AzSynapseDataFlow** cmdlet은 작업 영역의 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-109">The **Remove-AzSynapseDataFlow** cmdlet removes a data flow from workspace.</span></span>

## <span data-ttu-id="9f507-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9f507-110">EXAMPLES</span></span>

### <span data-ttu-id="9f507-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f507-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="9f507-112">이 명령은 ContosoWorkspace 이라는 작업 영역에서 ContosoDataFlow 이라는 데이터 흐름을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-112">This command removes the data flow named ContosoDataFlow from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9f507-113">변수</span><span class="sxs-lookup"><span data-stu-id="9f507-113">PARAMETERS</span></span>

### <span data-ttu-id="9f507-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f507-114">-AsJob</span></span>
<span data-ttu-id="9f507-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9f507-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f507-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f507-116">-DefaultProfile</span></span>
<span data-ttu-id="9f507-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f507-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f507-118">-InputObject</span></span>
<span data-ttu-id="9f507-119">데이터 흐름 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-119">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f507-120">-이름</span><span class="sxs-lookup"><span data-stu-id="9f507-120">-Name</span></span>
<span data-ttu-id="9f507-121">데이터 흐름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f507-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f507-122">-PassThru</span></span>
<span data-ttu-id="9f507-123">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9f507-124">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9f507-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f507-125">-WorkspaceName</span></span>
<span data-ttu-id="9f507-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9f507-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9f507-127">-WorkspaceObject</span></span>
<span data-ttu-id="9f507-128">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9f507-129">-확인</span><span class="sxs-lookup"><span data-stu-id="9f507-129">-Confirm</span></span>
<span data-ttu-id="9f507-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f507-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f507-131">-WhatIf</span></span>
<span data-ttu-id="9f507-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f507-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f507-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f507-134">CommonParameters</span></span>
<span data-ttu-id="9f507-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f507-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f507-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f507-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f507-137">입력</span><span class="sxs-lookup"><span data-stu-id="9f507-137">INPUTS</span></span>

### <span data-ttu-id="9f507-138">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="9f507-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9f507-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="9f507-139">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="9f507-140">출력</span><span class="sxs-lookup"><span data-stu-id="9f507-140">OUTPUTS</span></span>

### <span data-ttu-id="9f507-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9f507-141">System.Boolean</span></span>

## <span data-ttu-id="9f507-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9f507-142">NOTES</span></span>

## <span data-ttu-id="9f507-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f507-143">RELATED LINKS</span></span>
