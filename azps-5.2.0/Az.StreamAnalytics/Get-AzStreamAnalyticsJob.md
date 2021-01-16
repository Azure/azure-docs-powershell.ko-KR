---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366430"
---
# <span data-ttu-id="bb2f1-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="bb2f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2f1-103">Stream Analytics 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="bb2f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb2f1-104">SYNTAX</span></span>

### <span data-ttu-id="bb2f1-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb2f1-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2f1-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bb2f1-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb2f1-107">설명</span><span class="sxs-lookup"><span data-stu-id="bb2f1-107">DESCRIPTION</span></span>
<span data-ttu-id="bb2f1-108">**Get-AzStreamAnalyticsJob** cmdlet은 Azure 구독 또는 지정된 리소스 그룹에 정의된 모든 Stream Analytics 작업을 나열하거나 리소스 그룹 내의 특정 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="bb2f1-109">예제</span><span class="sxs-lookup"><span data-stu-id="bb2f1-109">EXAMPLES</span></span>

### <span data-ttu-id="bb2f1-110">예제 1: 구독의 모든 작업 관련 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bb2f1-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="bb2f1-111">이 명령은 Azure 구독의 모든 Stream Analytics 작업 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="bb2f1-112">예제 2: 리소스 그룹의 모든 작업 관련 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bb2f1-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="bb2f1-113">이 명령은 리소스 그룹 StreamAnalytics-Default-West-US의 모든 Stream Analytics 작업 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="bb2f1-114">예제 3: 리소스 그룹의 특정 작업 관련 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bb2f1-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="bb2f1-115">이 명령은 리소스 그룹 StreamAnalytics-Default-West-US의 Stream Analytics 작업 StreamingJob에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="bb2f1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb2f1-116">PARAMETERS</span></span>

### <span data-ttu-id="bb2f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2f1-117">-DefaultProfile</span></span>
<span data-ttu-id="bb2f1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb2f1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bb2f1-119">-Name</span></span>
<span data-ttu-id="bb2f1-120">검색할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2f1-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="bb2f1-121">-NoExpand</span></span>
<span data-ttu-id="bb2f1-122">cmdlet이 Azure Stream Analytics 작업을 검색하지만 입력, 출력 및 변환에 대한 정보를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2f1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2f1-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb2f1-124">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2f1-125">CommonParameters</span></span>
<span data-ttu-id="bb2f1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2f1-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bb2f1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2f1-128">입력</span><span class="sxs-lookup"><span data-stu-id="bb2f1-128">INPUTS</span></span>

### <span data-ttu-id="bb2f1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bb2f1-129">System.String</span></span>

### <span data-ttu-id="bb2f1-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb2f1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb2f1-131">출력</span><span class="sxs-lookup"><span data-stu-id="bb2f1-131">OUTPUTS</span></span>

### <span data-ttu-id="bb2f1-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="bb2f1-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb2f1-133">NOTES</span></span>

## <span data-ttu-id="bb2f1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb2f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb2f1-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb2f1-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb2f1-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="bb2f1-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bb2f1-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


