---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206357"
---
# <span data-ttu-id="0f5cb-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="0f5cb-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="0f5cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5cb-103">작업 영역의 사용 현황 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="0f5cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f5cb-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5cb-105">설명</span><span class="sxs-lookup"><span data-stu-id="0f5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5cb-106">**Get-AzOperationalInsightsWorkspaceUsage** cmdlet은 작업 영역의 사용 현황 데이터를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="0f5cb-107">그러면 특정 기간 동안 작업 영역이 분석한 데이터의 수가 노출됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="0f5cb-108">예제</span><span class="sxs-lookup"><span data-stu-id="0f5cb-108">EXAMPLES</span></span>

### <span data-ttu-id="0f5cb-109">예제 1: 작업 영역 이름으로 사용 현황 데이터 얻기</span><span class="sxs-lookup"><span data-stu-id="0f5cb-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0f5cb-110">이 명령은 지정된 리소스 그룹의 MyWorkspace라는 작업 영역의 사용 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="0f5cb-111">예제 2: 파이프라인을 사용하여 사용 현황 데이터 얻기</span><span class="sxs-lookup"><span data-stu-id="0f5cb-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="0f5cb-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용하여 MyWorkSpace라는 작업 Get-AzOperationalInsightsWorkspace 작업 영역이 현재 cmdlet에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="0f5cb-113">이 명령은 작업 영역의 사용 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="0f5cb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5cb-114">PARAMETERS</span></span>

### <span data-ttu-id="0f5cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5cb-115">-DefaultProfile</span></span>
<span data-ttu-id="0f5cb-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0f5cb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f5cb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0f5cb-117">-Name</span></span>
<span data-ttu-id="0f5cb-118">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f5cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="0f5cb-120">Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5cb-121">CommonParameters</span></span>
<span data-ttu-id="0f5cb-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5cb-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f5cb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5cb-124">입력</span><span class="sxs-lookup"><span data-stu-id="0f5cb-124">INPUTS</span></span>

### <span data-ttu-id="0f5cb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0f5cb-125">System.String</span></span>

## <span data-ttu-id="0f5cb-126">출력</span><span class="sxs-lookup"><span data-stu-id="0f5cb-126">OUTPUTS</span></span>

### <span data-ttu-id="0f5cb-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="0f5cb-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="0f5cb-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f5cb-128">NOTES</span></span>

## <span data-ttu-id="0f5cb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f5cb-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f5cb-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0f5cb-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0f5cb-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f5cb-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


