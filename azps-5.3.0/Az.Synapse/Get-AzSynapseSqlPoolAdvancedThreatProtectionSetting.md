---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383867"
---
# <span data-ttu-id="a5a31-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="a5a31-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="a5a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a31-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a31-103">SQL 풀에 대한 고급 위협 방지 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="a5a31-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5a31-104">SYNTAX</span></span>

### <span data-ttu-id="a5a31-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5a31-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a31-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a31-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a31-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a31-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5a31-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a31-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5a31-109">설명</span><span class="sxs-lookup"><span data-stu-id="a5a31-109">DESCRIPTION</span></span>
<span data-ttu-id="a5a31-110">**Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics 풀의 고급 위협 보호 설정을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a5a31-111">예제</span><span class="sxs-lookup"><span data-stu-id="a5a31-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a31-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5a31-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a5a31-113">이 명령은 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 SQL 풀에 대한 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a5a31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a31-114">PARAMETERS</span></span>

### <span data-ttu-id="a5a31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a31-115">-DefaultProfile</span></span>
<span data-ttu-id="a5a31-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a31-117">-InputObject</span></span>
<span data-ttu-id="a5a31-118">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5a31-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a31-119">-Name</span></span>
<span data-ttu-id="a5a31-120">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a5a31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a31-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5a31-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-122">Resource group name.</span></span>

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

### <span data-ttu-id="a5a31-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5a31-123">-ResourceId</span></span>
<span data-ttu-id="a5a31-124">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a5a31-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5a31-125">-WorkspaceName</span></span>
<span data-ttu-id="a5a31-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5a31-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5a31-127">-WorkspaceObject</span></span>
<span data-ttu-id="a5a31-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5a31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a31-129">CommonParameters</span></span>
<span data-ttu-id="a5a31-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5a31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a31-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5a31-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a31-132">입력</span><span class="sxs-lookup"><span data-stu-id="a5a31-132">INPUTS</span></span>

### <span data-ttu-id="a5a31-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5a31-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a5a31-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a5a31-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a5a31-135">출력</span><span class="sxs-lookup"><span data-stu-id="a5a31-135">OUTPUTS</span></span>

### <span data-ttu-id="a5a31-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="a5a31-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="a5a31-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5a31-137">NOTES</span></span>

## <span data-ttu-id="a5a31-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5a31-138">RELATED LINKS</span></span>
