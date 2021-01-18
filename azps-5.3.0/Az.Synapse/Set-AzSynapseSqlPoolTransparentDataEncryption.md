---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493256"
---
# <span data-ttu-id="00abc-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="00abc-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="00abc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00abc-102">SYNOPSIS</span></span>
<span data-ttu-id="00abc-103">SQL 풀에 대한 TDE 속성을 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="00abc-104">구문</span><span class="sxs-lookup"><span data-stu-id="00abc-104">SYNTAX</span></span>

### <span data-ttu-id="00abc-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="00abc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00abc-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00abc-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00abc-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00abc-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00abc-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00abc-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00abc-109">설명</span><span class="sxs-lookup"><span data-stu-id="00abc-109">DESCRIPTION</span></span>
<span data-ttu-id="00abc-110">**Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet은 Azure Synapse Analytics 풀의 TDE(투명한 데이터 암호화) 속성을 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="00abc-111">예제</span><span class="sxs-lookup"><span data-stu-id="00abc-111">EXAMPLES</span></span>

### <span data-ttu-id="00abc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="00abc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="00abc-113">이 명령은 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 이름의 풀에 대해 TDE를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="00abc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00abc-114">PARAMETERS</span></span>

### <span data-ttu-id="00abc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00abc-115">-AsJob</span></span>
<span data-ttu-id="00abc-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="00abc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00abc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00abc-117">-DefaultProfile</span></span>
<span data-ttu-id="00abc-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00abc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00abc-119">-InputObject</span></span>
<span data-ttu-id="00abc-120">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00abc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="00abc-121">-Name</span></span>
<span data-ttu-id="00abc-122">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="00abc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00abc-123">-ResourceGroupName</span></span>
<span data-ttu-id="00abc-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-124">Resource group name.</span></span>

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

### <span data-ttu-id="00abc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00abc-125">-ResourceId</span></span>
<span data-ttu-id="00abc-126">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="00abc-127">-State</span><span class="sxs-lookup"><span data-stu-id="00abc-127">-State</span></span>
<span data-ttu-id="00abc-128">Azure Synapse 분석 Sql 풀 투명한 데이터 암호화 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="00abc-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00abc-129">-WorkspaceName</span></span>
<span data-ttu-id="00abc-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="00abc-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="00abc-131">-WorkspaceObject</span></span>
<span data-ttu-id="00abc-132">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="00abc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00abc-133">-Confirm</span></span>
<span data-ttu-id="00abc-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00abc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00abc-135">-WhatIf</span></span>
<span data-ttu-id="00abc-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00abc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00abc-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00abc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00abc-138">CommonParameters</span></span>
<span data-ttu-id="00abc-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00abc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00abc-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00abc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00abc-141">입력</span><span class="sxs-lookup"><span data-stu-id="00abc-141">INPUTS</span></span>

### <span data-ttu-id="00abc-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="00abc-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="00abc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="00abc-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="00abc-144">출력</span><span class="sxs-lookup"><span data-stu-id="00abc-144">OUTPUTS</span></span>

### <span data-ttu-id="00abc-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="00abc-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="00abc-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00abc-146">NOTES</span></span>

## <span data-ttu-id="00abc-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00abc-147">RELATED LINKS</span></span>
