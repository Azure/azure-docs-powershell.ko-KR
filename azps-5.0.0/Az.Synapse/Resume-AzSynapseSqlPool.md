---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309390"
---
# <span data-ttu-id="110d0-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="110d0-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="110d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="110d0-102">SYNOPSIS</span></span>
<span data-ttu-id="110d0-103">Synapse Analytics SQL 풀을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="110d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="110d0-104">SYNTAX</span></span>

### <span data-ttu-id="110d0-105">ResumeByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="110d0-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110d0-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="110d0-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110d0-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="110d0-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="110d0-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="110d0-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="110d0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="110d0-109">DESCRIPTION</span></span>
<span data-ttu-id="110d0-110">**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="110d0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="110d0-111">EXAMPLES</span></span>

### <span data-ttu-id="110d0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="110d0-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="110d0-113">이 명령은 일시 중단 된 Azure Synapse Analytics SQL 풀을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="110d0-114">변수</span><span class="sxs-lookup"><span data-stu-id="110d0-114">PARAMETERS</span></span>

### <span data-ttu-id="110d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="110d0-115">-AsJob</span></span>
<span data-ttu-id="110d0-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="110d0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="110d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="110d0-117">-DefaultProfile</span></span>
<span data-ttu-id="110d0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="110d0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="110d0-119">-InputObject</span></span>
<span data-ttu-id="110d0-120">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="110d0-121">-Name</span></span>
<span data-ttu-id="110d0-122">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="110d0-123">-PassThru</span></span>
<span data-ttu-id="110d0-124">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="110d0-125">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="110d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="110d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="110d0-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="110d0-128">-ResourceId</span></span>
<span data-ttu-id="110d0-129">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="110d0-130">-WorkspaceName</span></span>
<span data-ttu-id="110d0-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="110d0-132">-WorkspaceObject</span></span>
<span data-ttu-id="110d0-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="110d0-134">-확인</span><span class="sxs-lookup"><span data-stu-id="110d0-134">-Confirm</span></span>
<span data-ttu-id="110d0-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="110d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="110d0-136">-WhatIf</span></span>
<span data-ttu-id="110d0-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="110d0-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="110d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="110d0-139">CommonParameters</span></span>
<span data-ttu-id="110d0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="110d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="110d0-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="110d0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="110d0-142">입력</span><span class="sxs-lookup"><span data-stu-id="110d0-142">INPUTS</span></span>

### <span data-ttu-id="110d0-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="110d0-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="110d0-144">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="110d0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="110d0-145">출력</span><span class="sxs-lookup"><span data-stu-id="110d0-145">OUTPUTS</span></span>

### <span data-ttu-id="110d0-146">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="110d0-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="110d0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="110d0-147">NOTES</span></span>

## <span data-ttu-id="110d0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="110d0-148">RELATED LINKS</span></span>
