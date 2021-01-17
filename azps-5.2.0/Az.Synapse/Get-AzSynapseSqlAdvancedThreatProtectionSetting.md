---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359437"
---
# <span data-ttu-id="fae41-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="fae41-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="fae41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae41-102">SYNOPSIS</span></span>
<span data-ttu-id="fae41-103">작업 영역의 고급 위협 방지 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="fae41-104">구문</span><span class="sxs-lookup"><span data-stu-id="fae41-104">SYNTAX</span></span>

### <span data-ttu-id="fae41-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fae41-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae41-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae41-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fae41-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fae41-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fae41-108">설명</span><span class="sxs-lookup"><span data-stu-id="fae41-108">DESCRIPTION</span></span>
<span data-ttu-id="fae41-109">**Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet은 Azure Synapse 분석 작업 영역의 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="fae41-110">예제</span><span class="sxs-lookup"><span data-stu-id="fae41-110">EXAMPLES</span></span>

### <span data-ttu-id="fae41-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fae41-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="fae41-112">이 명령은 ContosoWorkspace라는 작업 영역의 고급 위협 보호 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="fae41-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae41-113">PARAMETERS</span></span>

### <span data-ttu-id="fae41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae41-114">-DefaultProfile</span></span>
<span data-ttu-id="fae41-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae41-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fae41-116">-InputObject</span></span>
<span data-ttu-id="fae41-117">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fae41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae41-118">-ResourceGroupName</span></span>
<span data-ttu-id="fae41-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-119">Resource group name.</span></span>

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

### <span data-ttu-id="fae41-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fae41-120">-ResourceId</span></span>
<span data-ttu-id="fae41-121">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="fae41-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fae41-122">-WorkspaceName</span></span>
<span data-ttu-id="fae41-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fae41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae41-124">CommonParameters</span></span>
<span data-ttu-id="fae41-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fae41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae41-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fae41-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae41-127">입력</span><span class="sxs-lookup"><span data-stu-id="fae41-127">INPUTS</span></span>

### <span data-ttu-id="fae41-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fae41-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fae41-129">출력</span><span class="sxs-lookup"><span data-stu-id="fae41-129">OUTPUTS</span></span>

### <span data-ttu-id="fae41-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="fae41-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="fae41-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fae41-131">NOTES</span></span>

## <span data-ttu-id="fae41-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fae41-132">RELATED LINKS</span></span>
