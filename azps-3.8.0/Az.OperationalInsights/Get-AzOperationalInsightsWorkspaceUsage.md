---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: c1054e8dfb9a9133da740c5162c8e8f60c9df5d1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047275"
---
# <span data-ttu-id="0d506-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="0d506-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="0d506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d506-102">SYNOPSIS</span></span>
<span data-ttu-id="0d506-103">작업 영역에 대 한 사용 현황 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="0d506-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d506-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d506-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d506-105">DESCRIPTION</span></span>
<span data-ttu-id="0d506-106">**AzOperationalInsightsWorkspaceUsage** cmdlet은 작업 영역에 대 한 사용 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="0d506-107">이는 특정 기간 동안 작업 영역에 의해 분석 된 데이터의 양을 노출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="0d506-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0d506-108">EXAMPLES</span></span>

### <span data-ttu-id="0d506-109">예제 1: 작업 영역 이름별 사용량 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d506-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0d506-110">이 명령은 지정 된 리소스 그룹의 MyWorkspace 라는 작업 영역에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="0d506-111">예제 2: 파이프라인을 사용 하 여 사용 현황 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d506-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="0d506-112">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkSpace 라는 작업 영역을 가져온 다음 현재 cmdlet에 작업 영역을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="0d506-113">명령 작업 영역에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="0d506-114">변수</span><span class="sxs-lookup"><span data-stu-id="0d506-114">PARAMETERS</span></span>

### <span data-ttu-id="0d506-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d506-115">-DefaultProfile</span></span>
<span data-ttu-id="0d506-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d506-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d506-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0d506-117">-Name</span></span>
<span data-ttu-id="0d506-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0d506-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d506-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d506-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0d506-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d506-121">CommonParameters</span></span>
<span data-ttu-id="0d506-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d506-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d506-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d506-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d506-124">입력</span><span class="sxs-lookup"><span data-stu-id="0d506-124">INPUTS</span></span>

### <span data-ttu-id="0d506-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d506-125">System.String</span></span>

## <span data-ttu-id="0d506-126">출력</span><span class="sxs-lookup"><span data-stu-id="0d506-126">OUTPUTS</span></span>

### <span data-ttu-id="0d506-127">OperationalInsights. PSUsageMetric/.</span><span class="sxs-lookup"><span data-stu-id="0d506-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="0d506-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0d506-128">NOTES</span></span>

## <span data-ttu-id="0d506-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d506-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d506-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0d506-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="0d506-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0d506-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


