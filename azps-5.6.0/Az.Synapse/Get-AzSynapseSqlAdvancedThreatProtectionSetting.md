---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f35e4787779c49b399659f5e01ed8002df2e19ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015707"
---
# <span data-ttu-id="7d439-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="7d439-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="7d439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d439-102">SYNOPSIS</span></span>
<span data-ttu-id="7d439-103">작업 영역의 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="7d439-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d439-104">SYNTAX</span></span>

### <span data-ttu-id="7d439-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d439-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d439-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d439-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d439-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d439-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d439-108">설명</span><span class="sxs-lookup"><span data-stu-id="7d439-108">DESCRIPTION</span></span>
<span data-ttu-id="7d439-109">**Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse Analytics 작업 영역의 고급 위협 보호 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="7d439-110">예제</span><span class="sxs-lookup"><span data-stu-id="7d439-110">EXAMPLES</span></span>

### <span data-ttu-id="7d439-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d439-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7d439-112">이 명령은 ContosoWorkspace라는 작업 영역의 고급 위협 보호 설정을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="7d439-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7d439-113">PARAMETERS</span></span>

### <span data-ttu-id="7d439-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d439-114">-DefaultProfile</span></span>
<span data-ttu-id="7d439-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d439-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d439-116">-InputObject</span></span>
<span data-ttu-id="7d439-117">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7d439-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d439-118">-ResourceGroupName</span></span>
<span data-ttu-id="7d439-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-119">Resource group name.</span></span>

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

### <span data-ttu-id="7d439-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d439-120">-ResourceId</span></span>
<span data-ttu-id="7d439-121">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="7d439-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d439-122">-WorkspaceName</span></span>
<span data-ttu-id="7d439-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7d439-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d439-124">CommonParameters</span></span>
<span data-ttu-id="7d439-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d439-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d439-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d439-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d439-127">입력</span><span class="sxs-lookup"><span data-stu-id="7d439-127">INPUTS</span></span>

### <span data-ttu-id="7d439-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d439-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7d439-129">출력</span><span class="sxs-lookup"><span data-stu-id="7d439-129">OUTPUTS</span></span>

### <span data-ttu-id="7d439-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="7d439-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="7d439-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d439-131">NOTES</span></span>

## <span data-ttu-id="7d439-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d439-132">RELATED LINKS</span></span>
