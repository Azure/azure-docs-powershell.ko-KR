---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 091f9b57d7e40c20b52f82ec9d6c17e6d90dad3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527999"
---
# <span data-ttu-id="f9fab-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="f9fab-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="f9fab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9fab-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fab-103">작업 영역에 대 한 사용 현황 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9fab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9fab-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9fab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f9fab-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fab-106">**AzureRmOperationalInsightsWorkspaceUsage** cmdlet은 작업 영역에 대 한 사용 데이터를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="f9fab-107">이는 특정 기간 동안 작업 영역에 의해 분석 된 데이터의 양을 노출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="f9fab-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f9fab-108">EXAMPLES</span></span>

### <span data-ttu-id="f9fab-109">예제 1: 작업 영역 이름별 사용량 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="f9fab-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="f9fab-110">이 명령은 지정 된 리소스 그룹의 MyWorkspace 라는 작업 영역에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="f9fab-111">예제 2: 파이프라인을 사용 하 여 사용 현황 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="f9fab-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="f9fab-112">이 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkSpace 라는 작업 영역을 가져온 다음 현재 cmdlet에 작업 영역을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="f9fab-113">명령 작업 영역에 대 한 사용 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="f9fab-114">변수</span><span class="sxs-lookup"><span data-stu-id="f9fab-114">PARAMETERS</span></span>

### <span data-ttu-id="f9fab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fab-115">-DefaultProfile</span></span>
<span data-ttu-id="f9fab-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f9fab-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9fab-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f9fab-117">-Name</span></span>
<span data-ttu-id="f9fab-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fab-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9fab-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fab-121">CommonParameters</span></span>
<span data-ttu-id="f9fab-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fab-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fab-124">입력</span><span class="sxs-lookup"><span data-stu-id="f9fab-124">INPUTS</span></span>

### <span data-ttu-id="f9fab-125">않아야</span><span class="sxs-lookup"><span data-stu-id="f9fab-125">None</span></span>
<span data-ttu-id="f9fab-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9fab-127">출력</span><span class="sxs-lookup"><span data-stu-id="f9fab-127">OUTPUTS</span></span>

### <span data-ttu-id="f9fab-128">OperationalInsights의 ' 1 [Microsoft Azure. PSUsageMetric] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f9fab-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="f9fab-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f9fab-129">NOTES</span></span>

## <span data-ttu-id="f9fab-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9fab-130">RELATED LINKS</span></span>

[<span data-ttu-id="f9fab-131">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9fab-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="f9fab-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9fab-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


