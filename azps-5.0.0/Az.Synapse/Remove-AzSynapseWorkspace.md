---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseWorkspace.md
ms.openlocfilehash: dcc73c78334fba9823ddc1d26463422bcc388bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217132"
---
# <span data-ttu-id="dc932-101">Remove-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc932-101">Remove-AzSynapseWorkspace</span></span>

## <span data-ttu-id="dc932-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc932-102">SYNOPSIS</span></span>
<span data-ttu-id="dc932-103">Synapse Analytics 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-103">Deletes a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dc932-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc932-104">SYNTAX</span></span>

### <span data-ttu-id="dc932-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc932-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseWorkspace [-ResourceGroupName <String>] -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc932-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc932-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc932-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc932-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseWorkspace -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc932-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc932-108">DESCRIPTION</span></span>
<span data-ttu-id="dc932-109">**AzSynapseWorkspace** Cmdlet은 Azure Synapse Analytics 작업 영역을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-109">The **Remove-AzSynapseWorkspace** cmdlet permanently deletes an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="dc932-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dc932-110">EXAMPLES</span></span>

### <span data-ttu-id="dc932-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc932-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="dc932-112">이 명령은 Azure Synapse Analytics 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-112">This command deletes an Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="dc932-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dc932-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseWorkspace
```

<span data-ttu-id="dc932-114">이 명령은 파이프라인을 통해 Azure Synapse Analytics 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-114">This command deletes an Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="dc932-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="dc932-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="dc932-116">이 명령은 지정 된 리소스 ID를 가진 파이프라인을 통해 Azure Synapse Analytics 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-116">This command deletes an Azure Synapse Analytics workspace through pipeline with the specified resource ID.</span></span>

## <span data-ttu-id="dc932-117">변수</span><span class="sxs-lookup"><span data-stu-id="dc932-117">PARAMETERS</span></span>

### <span data-ttu-id="dc932-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc932-118">-AsJob</span></span>
<span data-ttu-id="dc932-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc932-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc932-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc932-120">-DefaultProfile</span></span>
<span data-ttu-id="dc932-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc932-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc932-122">-InputObject</span></span>
<span data-ttu-id="dc932-123">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc932-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dc932-124">-Name</span></span>
<span data-ttu-id="dc932-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc932-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc932-126">-PassThru</span></span>
<span data-ttu-id="dc932-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="dc932-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="dc932-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc932-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc932-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc932-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc932-131">-ResourceId</span></span>
<span data-ttu-id="dc932-132">Synapse workspace의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-132">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc932-133">-확인</span><span class="sxs-lookup"><span data-stu-id="dc932-133">-Confirm</span></span>
<span data-ttu-id="dc932-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc932-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc932-135">-WhatIf</span></span>
<span data-ttu-id="dc932-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc932-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc932-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc932-138">CommonParameters</span></span>
<span data-ttu-id="dc932-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc932-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc932-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc932-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc932-141">입력</span><span class="sxs-lookup"><span data-stu-id="dc932-141">INPUTS</span></span>

### <span data-ttu-id="dc932-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="dc932-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="dc932-143">출력</span><span class="sxs-lookup"><span data-stu-id="dc932-143">OUTPUTS</span></span>

### <span data-ttu-id="dc932-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="dc932-144">System.Boolean</span></span>

## <span data-ttu-id="dc932-145">상속자</span><span class="sxs-lookup"><span data-stu-id="dc932-145">NOTES</span></span>

## <span data-ttu-id="dc932-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc932-146">RELATED LINKS</span></span>
