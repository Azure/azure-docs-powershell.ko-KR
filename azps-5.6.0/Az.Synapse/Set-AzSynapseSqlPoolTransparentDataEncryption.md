---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cdc72a2bb0e21873bd0fa2d82123afe8ed011378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992091"
---
# <span data-ttu-id="63a01-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="63a01-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="63a01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a01-102">SYNOPSIS</span></span>
<span data-ttu-id="63a01-103">풀에 대한 TDE SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="63a01-104">구문</span><span class="sxs-lookup"><span data-stu-id="63a01-104">SYNTAX</span></span>

### <span data-ttu-id="63a01-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="63a01-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a01-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a01-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a01-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a01-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63a01-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63a01-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a01-109">설명</span><span class="sxs-lookup"><span data-stu-id="63a01-109">DESCRIPTION</span></span>
<span data-ttu-id="63a01-110">**Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet은 Azure Synapse Analytics SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="63a01-111">예제</span><span class="sxs-lookup"><span data-stu-id="63a01-111">EXAMPLES</span></span>

### <span data-ttu-id="63a01-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="63a01-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="63a01-113">이 명령을 사용하면 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 SQL 풀에 대해 TDE를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="63a01-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="63a01-114">PARAMETERS</span></span>

### <span data-ttu-id="63a01-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63a01-115">-AsJob</span></span>
<span data-ttu-id="63a01-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="63a01-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63a01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a01-117">-DefaultProfile</span></span>
<span data-ttu-id="63a01-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a01-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63a01-119">-InputObject</span></span>
<span data-ttu-id="63a01-120">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-121">-Name</span><span class="sxs-lookup"><span data-stu-id="63a01-121">-Name</span></span>
<span data-ttu-id="63a01-122">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a01-123">-ResourceGroupName</span></span>
<span data-ttu-id="63a01-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63a01-125">-ResourceId</span></span>
<span data-ttu-id="63a01-126">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-127">-State</span><span class="sxs-lookup"><span data-stu-id="63a01-127">-State</span></span>
<span data-ttu-id="63a01-128">Azure Synapse Analytics Sql Pool 투명한 데이터 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="63a01-129">-WorkspaceName</span></span>
<span data-ttu-id="63a01-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="63a01-131">-WorkspaceObject</span></span>
<span data-ttu-id="63a01-132">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a01-133">-확인</span><span class="sxs-lookup"><span data-stu-id="63a01-133">-Confirm</span></span>
<span data-ttu-id="63a01-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a01-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a01-135">-WhatIf</span></span>
<span data-ttu-id="63a01-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a01-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a01-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a01-138">CommonParameters</span></span>
<span data-ttu-id="63a01-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63a01-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a01-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63a01-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a01-141">입력</span><span class="sxs-lookup"><span data-stu-id="63a01-141">INPUTS</span></span>

### <span data-ttu-id="63a01-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="63a01-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="63a01-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="63a01-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="63a01-144">출력</span><span class="sxs-lookup"><span data-stu-id="63a01-144">OUTPUTS</span></span>

### <span data-ttu-id="63a01-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="63a01-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="63a01-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63a01-146">NOTES</span></span>

## <span data-ttu-id="63a01-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63a01-147">RELATED LINKS</span></span>
