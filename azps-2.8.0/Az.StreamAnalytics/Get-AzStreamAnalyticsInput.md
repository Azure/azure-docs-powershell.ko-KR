---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: cd6e7e4bf9ba9a99b9b3a9a5f58acb9578236037
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874070"
---
# <span data-ttu-id="eefa5-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eefa5-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="eefa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefa5-102">SYNOPSIS</span></span>
<span data-ttu-id="eefa5-103">스트림 분석 작업 입력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="eefa5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eefa5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eefa5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eefa5-105">DESCRIPTION</span></span>
<span data-ttu-id="eefa5-106">**AzStreamAnalyticsInput** Cmdlet은 Stream Analytics 작업에 정의 된 모든 입력을 나열 하거나 특정 입력에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="eefa5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eefa5-107">EXAMPLES</span></span>

### <span data-ttu-id="eefa5-108">예제 1: 작업에 정의 된 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="eefa5-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="eefa5-109">이 명령은 job StreamingJob에 정의 된 모든 입력에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="eefa5-110">예제 2: 작업에 정의 된 특정 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="eefa5-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="eefa5-111">이 명령은 job StreamingJob에 정의 된 입력 명명 된 EntryStream에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="eefa5-112">변수</span><span class="sxs-lookup"><span data-stu-id="eefa5-112">PARAMETERS</span></span>

### <span data-ttu-id="eefa5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefa5-113">-DefaultProfile</span></span>
<span data-ttu-id="eefa5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eefa5-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="eefa5-115">-JobName</span></span>
<span data-ttu-id="eefa5-116">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="eefa5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="eefa5-117">-Name</span></span>
<span data-ttu-id="eefa5-118">검색할 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="eefa5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefa5-119">-ResourceGroupName</span></span>
<span data-ttu-id="eefa5-120">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="eefa5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefa5-121">CommonParameters</span></span>
<span data-ttu-id="eefa5-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eefa5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefa5-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eefa5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefa5-124">입력</span><span class="sxs-lookup"><span data-stu-id="eefa5-124">INPUTS</span></span>

### <span data-ttu-id="eefa5-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eefa5-125">System.String</span></span>

## <span data-ttu-id="eefa5-126">출력</span><span class="sxs-lookup"><span data-stu-id="eefa5-126">OUTPUTS</span></span>

### <span data-ttu-id="eefa5-127">Microsoft. StreamAnalytics. PSInput</span><span class="sxs-lookup"><span data-stu-id="eefa5-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="eefa5-128">상속자</span><span class="sxs-lookup"><span data-stu-id="eefa5-128">NOTES</span></span>

## <span data-ttu-id="eefa5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eefa5-129">RELATED LINKS</span></span>

[<span data-ttu-id="eefa5-130">새로운 AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eefa5-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="eefa5-131">제거-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eefa5-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="eefa5-132">테스트-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="eefa5-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


