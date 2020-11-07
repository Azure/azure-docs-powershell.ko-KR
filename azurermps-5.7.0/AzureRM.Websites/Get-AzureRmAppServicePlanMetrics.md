---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlanMetrics.md
ms.openlocfilehash: f3376f40246640b8de52ffa138912c768486a3dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703529"
---
# <span data-ttu-id="dc565-101">Get-AzureRmAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="dc565-101">Get-AzureRmAppServicePlanMetrics</span></span>

## <span data-ttu-id="dc565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc565-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc565-103">구문과</span><span class="sxs-lookup"><span data-stu-id="dc565-103">SYNTAX</span></span>

### <span data-ttu-id="dc565-104">S1</span><span class="sxs-lookup"><span data-stu-id="dc565-104">S1</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc565-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="dc565-105">S2</span></span>
```
Get-AzureRmAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <ServerFarmWithRichSku>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc565-106">설명은</span><span class="sxs-lookup"><span data-stu-id="dc565-106">DESCRIPTION</span></span>
<span data-ttu-id="dc565-107">**Get-AzureRmAppServicePlanMetrics** 는 앱 서비스 계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc565-107">The **Get-AzureRmAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="dc565-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dc565-108">EXAMPLES</span></span>

### <span data-ttu-id="dc565-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="dc565-109">1:</span></span>
```
PS C:\>Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="dc565-110">이 명령은 StartTime 및 EndTime 사이의 분당 앱 서비스 계획의 PT1M-폴링 시간 1 분)의 CPU 백분율을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc565-110">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="dc565-111">변수</span><span class="sxs-lookup"><span data-stu-id="dc565-111">PARAMETERS</span></span>

### <span data-ttu-id="dc565-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dc565-112">-AppServicePlan</span></span>
<span data-ttu-id="dc565-113">App Service 계획 개체</span><span class="sxs-lookup"><span data-stu-id="dc565-113">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc565-114">-DefaultProfile</span></span>
<span data-ttu-id="dc565-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc565-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc565-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dc565-116">-EndTime</span></span>
<span data-ttu-id="dc565-117">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="dc565-117">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-118">-세분성</span><span class="sxs-lookup"><span data-stu-id="dc565-118">-Granularity</span></span>
<span data-ttu-id="dc565-119">수준을</span><span class="sxs-lookup"><span data-stu-id="dc565-119">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-120">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="dc565-120">-InstanceDetails</span></span>
<span data-ttu-id="dc565-121">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="dc565-121">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-122">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="dc565-122">-Metrics</span></span>
<span data-ttu-id="dc565-123">매트릭스</span><span class="sxs-lookup"><span data-stu-id="dc565-123">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dc565-124">-Name</span></span>
<span data-ttu-id="dc565-125">App Service 계획 이름</span><span class="sxs-lookup"><span data-stu-id="dc565-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc565-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc565-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="dc565-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dc565-128">-StartTime</span></span>
<span data-ttu-id="dc565-129">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="dc565-129">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc565-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc565-130">CommonParameters</span></span>
<span data-ttu-id="dc565-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc565-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc565-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc565-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc565-133">입력</span><span class="sxs-lookup"><span data-stu-id="dc565-133">INPUTS</span></span>

### <span data-ttu-id="dc565-134">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="dc565-134">ServerFarmWithRichSku</span></span>
<span data-ttu-id="dc565-135">' AppServicePlan ' 매개 변수는 파이프라인에서 ' ServerFarmWithRichSku ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc565-135">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="dc565-136">출력</span><span class="sxs-lookup"><span data-stu-id="dc565-136">OUTPUTS</span></span>

## <span data-ttu-id="dc565-137">상속자</span><span class="sxs-lookup"><span data-stu-id="dc565-137">NOTES</span></span>

## <span data-ttu-id="dc565-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc565-138">RELATED LINKS</span></span>

