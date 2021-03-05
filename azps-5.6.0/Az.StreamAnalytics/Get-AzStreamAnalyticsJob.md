---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 26808bd3db72f8618505045b2b20f6d0b56806da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973867"
---
# <span data-ttu-id="d44fa-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="d44fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d44fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d44fa-103">Stream Analytics 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="d44fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="d44fa-104">SYNTAX</span></span>

### <span data-ttu-id="d44fa-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d44fa-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d44fa-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="d44fa-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d44fa-107">설명</span><span class="sxs-lookup"><span data-stu-id="d44fa-107">DESCRIPTION</span></span>
<span data-ttu-id="d44fa-108">**Get-AzStreamAnalyticsJob** cmdlet은 Azure 구독 또는 지정된 리소스 그룹에 정의된 모든 Stream Analytics 작업을 나열하거나 리소스 그룹 내의 특정 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="d44fa-109">예제</span><span class="sxs-lookup"><span data-stu-id="d44fa-109">EXAMPLES</span></span>

### <span data-ttu-id="d44fa-110">예제 1: 구독의 모든 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="d44fa-111">이 명령은 Azure 구독의 모든 Stream Analytics 작업 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="d44fa-112">예제 2: 리소스 그룹의 모든 작업 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="d44fa-113">이 명령은 리소스 그룹 StreamAnalytics-Default-West-US의 모든 Stream Analytics 작업 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="d44fa-114">예제 3: 리소스 그룹의 특정 작업 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="d44fa-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d44fa-115">이 명령은 리소스 그룹 StreamAnalytics-Default-West-US의 Stream Analytics 작업 StreamingJob에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="d44fa-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d44fa-116">PARAMETERS</span></span>

### <span data-ttu-id="d44fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44fa-117">-DefaultProfile</span></span>
<span data-ttu-id="d44fa-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d44fa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d44fa-119">-Name</span></span>
<span data-ttu-id="d44fa-120">검색할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="d44fa-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="d44fa-121">-NoExpand</span></span>
<span data-ttu-id="d44fa-122">cmdlet이 Azure Stream Analytics 작업을 검색하지만 입력, 출력 및 변환에 대한 정보를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="d44fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d44fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="d44fa-124">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="d44fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44fa-125">CommonParameters</span></span>
<span data-ttu-id="d44fa-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d44fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44fa-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d44fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44fa-128">입력</span><span class="sxs-lookup"><span data-stu-id="d44fa-128">INPUTS</span></span>

### <span data-ttu-id="d44fa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d44fa-129">System.String</span></span>

### <span data-ttu-id="d44fa-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d44fa-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d44fa-131">출력</span><span class="sxs-lookup"><span data-stu-id="d44fa-131">OUTPUTS</span></span>

### <span data-ttu-id="d44fa-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d44fa-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d44fa-133">NOTES</span></span>

## <span data-ttu-id="d44fa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d44fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="d44fa-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d44fa-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d44fa-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d44fa-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d44fa-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


