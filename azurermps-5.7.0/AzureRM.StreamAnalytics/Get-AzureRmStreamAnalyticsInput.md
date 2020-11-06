---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526508"
---
# <span data-ttu-id="3413c-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3413c-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="3413c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3413c-102">SYNOPSIS</span></span>
<span data-ttu-id="3413c-103">스트림 분석 작업 입력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3413c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3413c-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3413c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3413c-105">DESCRIPTION</span></span>
<span data-ttu-id="3413c-106">**AzureRmStreamAnalyticsInput** Cmdlet은 Stream Analytics 작업에 정의 된 모든 입력을 나열 하거나 특정 입력에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="3413c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3413c-107">EXAMPLES</span></span>

### <span data-ttu-id="3413c-108">예제 1: 작업에 정의 된 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="3413c-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="3413c-109">이 명령은 job StreamingJob에 정의 된 모든 입력에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="3413c-110">예제 2: 작업에 정의 된 특정 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="3413c-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="3413c-111">이 명령은 job StreamingJob에 정의 된 입력 명명 된 EntryStream에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="3413c-112">변수</span><span class="sxs-lookup"><span data-stu-id="3413c-112">PARAMETERS</span></span>

### <span data-ttu-id="3413c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3413c-113">-DefaultProfile</span></span>
<span data-ttu-id="3413c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3413c-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="3413c-115">-JobName</span></span>
<span data-ttu-id="3413c-116">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3413c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3413c-117">-Name</span></span>
<span data-ttu-id="3413c-118">검색할 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3413c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3413c-119">-ResourceGroupName</span></span>
<span data-ttu-id="3413c-120">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="3413c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3413c-121">CommonParameters</span></span>
<span data-ttu-id="3413c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3413c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3413c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3413c-124">입력</span><span class="sxs-lookup"><span data-stu-id="3413c-124">INPUTS</span></span>

### <span data-ttu-id="3413c-125">않아야</span><span class="sxs-lookup"><span data-stu-id="3413c-125">None</span></span>
<span data-ttu-id="3413c-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3413c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3413c-127">출력</span><span class="sxs-lookup"><span data-stu-id="3413c-127">OUTPUTS</span></span>

### <span data-ttu-id="3413c-128">System.webserver. List ' 1 [[Microsoft Azure.]. PSInput, Microsoft Azure. commands 분석]] Microsoft Azure. e. e. e t e-PSInput. a n i 입력</span><span class="sxs-lookup"><span data-stu-id="3413c-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="3413c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3413c-129">NOTES</span></span>

## <span data-ttu-id="3413c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3413c-130">RELATED LINKS</span></span>

[<span data-ttu-id="3413c-131">새로운 AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3413c-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="3413c-132">제거-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3413c-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="3413c-133">테스트-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3413c-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


