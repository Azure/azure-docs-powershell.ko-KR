---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359388"
---
# <span data-ttu-id="15c94-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="15c94-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="15c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c94-102">SYNOPSIS</span></span>
<span data-ttu-id="15c94-103">Azure Synapse Analytics 풀의 감사 설정을 SQL.</span><span class="sxs-lookup"><span data-stu-id="15c94-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="15c94-104">구문</span><span class="sxs-lookup"><span data-stu-id="15c94-104">SYNTAX</span></span>

### <span data-ttu-id="15c94-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="15c94-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c94-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c94-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c94-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c94-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15c94-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c94-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15c94-109">설명</span><span class="sxs-lookup"><span data-stu-id="15c94-109">DESCRIPTION</span></span>
<span data-ttu-id="15c94-110">**Get-AzSynapseSqlPoolAuditSetting** cmdlet은 Azure Synapse Analytics 풀의 감사 설정을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="15c94-111">예제</span><span class="sxs-lookup"><span data-stu-id="15c94-111">EXAMPLES</span></span>

### <span data-ttu-id="15c94-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="15c94-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="15c94-113">이 명령은 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="15c94-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="15c94-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="15c94-115">이 명령은 파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoSqlPool이라는 SQL 풀의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="15c94-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15c94-116">PARAMETERS</span></span>

### <span data-ttu-id="15c94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c94-117">-DefaultProfile</span></span>
<span data-ttu-id="15c94-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c94-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15c94-119">-InputObject</span></span>
<span data-ttu-id="15c94-120">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="15c94-121">-Name</span><span class="sxs-lookup"><span data-stu-id="15c94-121">-Name</span></span>
<span data-ttu-id="15c94-122">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="15c94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c94-123">-ResourceGroupName</span></span>
<span data-ttu-id="15c94-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-124">Resource group name.</span></span>

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

### <span data-ttu-id="15c94-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15c94-125">-ResourceId</span></span>
<span data-ttu-id="15c94-126">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="15c94-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15c94-127">-WorkspaceName</span></span>
<span data-ttu-id="15c94-128">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="15c94-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="15c94-129">-WorkspaceObject</span></span>
<span data-ttu-id="15c94-130">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="15c94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c94-131">CommonParameters</span></span>
<span data-ttu-id="15c94-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15c94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c94-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15c94-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c94-134">입력</span><span class="sxs-lookup"><span data-stu-id="15c94-134">INPUTS</span></span>

### <span data-ttu-id="15c94-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="15c94-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="15c94-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="15c94-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="15c94-137">출력</span><span class="sxs-lookup"><span data-stu-id="15c94-137">OUTPUTS</span></span>

### <span data-ttu-id="15c94-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="15c94-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="15c94-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15c94-139">NOTES</span></span>

## <span data-ttu-id="15c94-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15c94-140">RELATED LINKS</span></span>
