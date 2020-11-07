---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 9c92156f3fe739cd4f4285d536bd8a4c79cd3ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702826"
---
# <span data-ttu-id="bdd46-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bdd46-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="bdd46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd46-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd46-103">스트림 분석 작업 변환에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdd46-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bdd46-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd46-106">**AzureRmStreamAnalyticsTransformation** Cmdlet은 Stream Analytics 작업에 정의 된 변환에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="bdd46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bdd46-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd46-108">예제 1: Stream Analytics 변환에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="bdd46-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="bdd46-109">이 명령은 StreamingJob 이라는 작업의 StreamingJob 이라는 변형에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="bdd46-110">변수</span><span class="sxs-lookup"><span data-stu-id="bdd46-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd46-111">-DefaultProfile</span></span>
<span data-ttu-id="bdd46-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd46-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="bdd46-113">-JobName</span></span>
<span data-ttu-id="bdd46-114">Azure Stream Analytics 변환이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="bdd46-115">-이름</span><span class="sxs-lookup"><span data-stu-id="bdd46-115">-Name</span></span>
<span data-ttu-id="bdd46-116">검색할 Azure Stream Analytics 변환의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd46-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdd46-118">Azure Stream Analytics 변환이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="bdd46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd46-119">CommonParameters</span></span>
<span data-ttu-id="bdd46-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd46-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd46-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd46-122">입력</span><span class="sxs-lookup"><span data-stu-id="bdd46-122">INPUTS</span></span>

### <span data-ttu-id="bdd46-123">않아야</span><span class="sxs-lookup"><span data-stu-id="bdd46-123">None</span></span>
<span data-ttu-id="bdd46-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdd46-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bdd46-125">출력</span><span class="sxs-lookup"><span data-stu-id="bdd46-125">OUTPUTS</span></span>

### <span data-ttu-id="bdd46-126">System.webserver. List ' 1 [[Microsoft Azure. PSTransformation, Microsoft azure. PSTransformation 분석]] Microsoft Azure. e. e t e. e 1.</span><span class="sxs-lookup"><span data-stu-id="bdd46-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="bdd46-127">상속자</span><span class="sxs-lookup"><span data-stu-id="bdd46-127">NOTES</span></span>

## <span data-ttu-id="bdd46-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdd46-128">RELATED LINKS</span></span>

[<span data-ttu-id="bdd46-129">새로운 AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="bdd46-129">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


