---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: cf32bea3942c89b408592778657e5ecffae2acd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015696"
---
# <span data-ttu-id="037ce-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="037ce-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="037ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="037ce-102">SYNOPSIS</span></span>
<span data-ttu-id="037ce-103">Azure Synapse Analytics 작업 영역의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="037ce-104">구문</span><span class="sxs-lookup"><span data-stu-id="037ce-104">SYNTAX</span></span>

### <span data-ttu-id="037ce-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="037ce-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="037ce-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="037ce-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="037ce-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="037ce-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="037ce-108">설명</span><span class="sxs-lookup"><span data-stu-id="037ce-108">DESCRIPTION</span></span>
<span data-ttu-id="037ce-109">**Get-AzSynapseSqlAuditSetting** cmdlet은 Azure Synapse Analytics 작업 영역의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="037ce-110">예제</span><span class="sxs-lookup"><span data-stu-id="037ce-110">EXAMPLES</span></span>

### <span data-ttu-id="037ce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="037ce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="037ce-112">ContosoWorkspace라는 작업 영역의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="037ce-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="037ce-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="037ce-114">파이프라인을 통해 ContosoWorkspace라는 작업 영역의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="037ce-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="037ce-115">PARAMETERS</span></span>

### <span data-ttu-id="037ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037ce-116">-DefaultProfile</span></span>
<span data-ttu-id="037ce-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="037ce-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="037ce-118">-InputObject</span></span>
<span data-ttu-id="037ce-119">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="037ce-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="037ce-120">-ResourceGroupName</span></span>
<span data-ttu-id="037ce-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-121">Resource group name.</span></span>

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

### <span data-ttu-id="037ce-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="037ce-122">-ResourceId</span></span>
<span data-ttu-id="037ce-123">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="037ce-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="037ce-124">-WorkspaceName</span></span>
<span data-ttu-id="037ce-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="037ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037ce-126">CommonParameters</span></span>
<span data-ttu-id="037ce-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="037ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037ce-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="037ce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037ce-129">입력</span><span class="sxs-lookup"><span data-stu-id="037ce-129">INPUTS</span></span>

### <span data-ttu-id="037ce-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="037ce-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="037ce-131">출력</span><span class="sxs-lookup"><span data-stu-id="037ce-131">OUTPUTS</span></span>

### <span data-ttu-id="037ce-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="037ce-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="037ce-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="037ce-133">NOTES</span></span>

## <span data-ttu-id="037ce-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="037ce-134">RELATED LINKS</span></span>
