---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015648"
---
# <span data-ttu-id="24b06-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="24b06-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="24b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b06-102">SYNOPSIS</span></span>
<span data-ttu-id="24b06-103">Azure Synapse Analytics의 감사 설정을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24b06-104">구문</span><span class="sxs-lookup"><span data-stu-id="24b06-104">SYNTAX</span></span>

### <span data-ttu-id="24b06-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="24b06-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24b06-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24b06-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24b06-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24b06-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24b06-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24b06-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24b06-109">설명</span><span class="sxs-lookup"><span data-stu-id="24b06-109">DESCRIPTION</span></span>
<span data-ttu-id="24b06-110">**Get-AzSynapseSqlPoolAuditSetting** cmdlet은 Azure Synapse Analytics SQL 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="24b06-111">예제</span><span class="sxs-lookup"><span data-stu-id="24b06-111">EXAMPLES</span></span>

### <span data-ttu-id="24b06-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="24b06-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="24b06-113">이 명령은 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="24b06-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="24b06-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="24b06-115">이 명령은 파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="24b06-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="24b06-116">PARAMETERS</span></span>

### <span data-ttu-id="24b06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b06-117">-DefaultProfile</span></span>
<span data-ttu-id="24b06-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b06-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b06-119">-InputObject</span></span>
<span data-ttu-id="24b06-120">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24b06-121">-Name</span><span class="sxs-lookup"><span data-stu-id="24b06-121">-Name</span></span>
<span data-ttu-id="24b06-122">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="24b06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b06-123">-ResourceGroupName</span></span>
<span data-ttu-id="24b06-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-124">Resource group name.</span></span>

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

### <span data-ttu-id="24b06-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b06-125">-ResourceId</span></span>
<span data-ttu-id="24b06-126">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="24b06-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24b06-127">-WorkspaceName</span></span>
<span data-ttu-id="24b06-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="24b06-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24b06-129">-WorkspaceObject</span></span>
<span data-ttu-id="24b06-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="24b06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b06-131">CommonParameters</span></span>
<span data-ttu-id="24b06-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24b06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b06-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24b06-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b06-134">입력</span><span class="sxs-lookup"><span data-stu-id="24b06-134">INPUTS</span></span>

### <span data-ttu-id="24b06-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24b06-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="24b06-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="24b06-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="24b06-137">출력</span><span class="sxs-lookup"><span data-stu-id="24b06-137">OUTPUTS</span></span>

### <span data-ttu-id="24b06-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="24b06-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="24b06-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24b06-139">NOTES</span></span>

## <span data-ttu-id="24b06-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24b06-140">RELATED LINKS</span></span>
