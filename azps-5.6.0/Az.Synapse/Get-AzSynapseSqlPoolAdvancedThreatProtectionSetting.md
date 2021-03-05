---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c706de537f4d95603399540342bd3ad52d2b30fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015675"
---
# <span data-ttu-id="14331-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="14331-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="14331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14331-102">SYNOPSIS</span></span>
<span data-ttu-id="14331-103">풀에 대한 고급 위협 보호 설정을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="14331-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="14331-104">구문</span><span class="sxs-lookup"><span data-stu-id="14331-104">SYNTAX</span></span>

### <span data-ttu-id="14331-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="14331-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14331-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14331-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14331-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14331-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14331-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14331-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14331-109">설명</span><span class="sxs-lookup"><span data-stu-id="14331-109">DESCRIPTION</span></span>
<span data-ttu-id="14331-110">**Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics SQL 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="14331-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="14331-111">예제</span><span class="sxs-lookup"><span data-stu-id="14331-111">EXAMPLES</span></span>

### <span data-ttu-id="14331-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="14331-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="14331-113">이 명령은 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 풀에 대한 고급 위협 보호 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="14331-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="14331-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14331-114">PARAMETERS</span></span>

### <span data-ttu-id="14331-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14331-115">-DefaultProfile</span></span>
<span data-ttu-id="14331-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14331-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14331-117">-InputObject</span></span>
<span data-ttu-id="14331-118">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="14331-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14331-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14331-119">-Name</span></span>
<span data-ttu-id="14331-120">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14331-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14331-121">-ResourceGroupName</span></span>
<span data-ttu-id="14331-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14331-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14331-123">-ResourceId</span></span>
<span data-ttu-id="14331-124">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-124">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14331-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14331-125">-WorkspaceName</span></span>
<span data-ttu-id="14331-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14331-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="14331-127">-WorkspaceObject</span></span>
<span data-ttu-id="14331-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="14331-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14331-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14331-129">CommonParameters</span></span>
<span data-ttu-id="14331-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14331-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14331-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14331-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14331-132">입력</span><span class="sxs-lookup"><span data-stu-id="14331-132">INPUTS</span></span>

### <span data-ttu-id="14331-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="14331-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="14331-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="14331-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="14331-135">출력</span><span class="sxs-lookup"><span data-stu-id="14331-135">OUTPUTS</span></span>

### <span data-ttu-id="14331-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="14331-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="14331-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14331-137">NOTES</span></span>

## <span data-ttu-id="14331-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14331-138">RELATED LINKS</span></span>
