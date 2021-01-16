---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 1f83eaf8ff358c211dbe8b83cfb99d986e56c1ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366444"
---
# <span data-ttu-id="76c20-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="76c20-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="76c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c20-102">SYNOPSIS</span></span>
<span data-ttu-id="76c20-103">Stream Analytics 작업 입력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="76c20-104">구문</span><span class="sxs-lookup"><span data-stu-id="76c20-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c20-105">설명</span><span class="sxs-lookup"><span data-stu-id="76c20-105">DESCRIPTION</span></span>
<span data-ttu-id="76c20-106">**Get-AzStreamAnalyticsInput** cmdlet은 Stream Analytics 작업에서 정의된 모든 입력을 나열하거나 특정 입력에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="76c20-107">예제</span><span class="sxs-lookup"><span data-stu-id="76c20-107">EXAMPLES</span></span>

### <span data-ttu-id="76c20-108">예제 1: 작업에서 정의된 입력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="76c20-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="76c20-109">이 명령은 StreamingJob 작업에서 정의된 모든 입력에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="76c20-110">예제 2: 작업에서 정의된 특정 입력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="76c20-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="76c20-111">이 명령은 StreamingJob 작업에서 정의된 EntryStream이라는 입력에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="76c20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76c20-112">PARAMETERS</span></span>

### <span data-ttu-id="76c20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c20-113">-DefaultProfile</span></span>
<span data-ttu-id="76c20-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c20-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="76c20-115">-JobName</span></span>
<span data-ttu-id="76c20-116">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="76c20-117">-Name</span><span class="sxs-lookup"><span data-stu-id="76c20-117">-Name</span></span>
<span data-ttu-id="76c20-118">검색할 Azure Stream Analytics 입력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76c20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c20-119">-ResourceGroupName</span></span>
<span data-ttu-id="76c20-120">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="76c20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c20-121">CommonParameters</span></span>
<span data-ttu-id="76c20-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76c20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c20-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76c20-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c20-124">입력</span><span class="sxs-lookup"><span data-stu-id="76c20-124">INPUTS</span></span>

### <span data-ttu-id="76c20-125">System.String</span><span class="sxs-lookup"><span data-stu-id="76c20-125">System.String</span></span>

## <span data-ttu-id="76c20-126">출력</span><span class="sxs-lookup"><span data-stu-id="76c20-126">OUTPUTS</span></span>

### <span data-ttu-id="76c20-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="76c20-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="76c20-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76c20-128">NOTES</span></span>

## <span data-ttu-id="76c20-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76c20-129">RELATED LINKS</span></span>

[<span data-ttu-id="76c20-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="76c20-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="76c20-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="76c20-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="76c20-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="76c20-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


