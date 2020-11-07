---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappmetrics
schema: 2.0.0
ms.openlocfilehash: 1382ec0f4a2eaa61493e05a762616d9fac54a7f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880842"
---
# <span data-ttu-id="79838-101">Get-AzureRmWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="79838-101">Get-AzureRmWebAppMetrics</span></span>

## <span data-ttu-id="79838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79838-102">SYNOPSIS</span></span>
<span data-ttu-id="79838-103">Azure Web App 메트릭스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79838-103">Gets Azure Web App metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79838-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79838-104">SYNTAX</span></span>

### <span data-ttu-id="79838-105">S1</span><span class="sxs-lookup"><span data-stu-id="79838-105">S1</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79838-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="79838-106">S2</span></span>
```
Get-AzureRmWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79838-107">설명은</span><span class="sxs-lookup"><span data-stu-id="79838-107">DESCRIPTION</span></span>
<span data-ttu-id="79838-108">**Get-AzureRmWebAppMetrics** 는 웹 앱 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79838-108">The **Get-AzureRmWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="79838-109">예제의</span><span class="sxs-lookup"><span data-stu-id="79838-109">EXAMPLES</span></span>

### <span data-ttu-id="79838-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="79838-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="79838-111">이 명령은 StartTime 및 EndTime 사이의 분 당 웹 앱 ContosoWebApp (PT1M-폴링 시간 1 분) 요청을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79838-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="79838-112">변수</span><span class="sxs-lookup"><span data-stu-id="79838-112">PARAMETERS</span></span>

### <span data-ttu-id="79838-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79838-113">-DefaultProfile</span></span>
<span data-ttu-id="79838-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79838-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79838-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="79838-115">-EndTime</span></span>
<span data-ttu-id="79838-116">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="79838-116">End Time in UTC</span></span>

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

### <span data-ttu-id="79838-117">-세분성</span><span class="sxs-lookup"><span data-stu-id="79838-117">-Granularity</span></span>
<span data-ttu-id="79838-118">수준을</span><span class="sxs-lookup"><span data-stu-id="79838-118">Granularity</span></span>

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

### <span data-ttu-id="79838-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="79838-119">-InstanceDetails</span></span>
<span data-ttu-id="79838-120">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="79838-120">Instance Details</span></span>

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

### <span data-ttu-id="79838-121">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="79838-121">-Metrics</span></span>
<span data-ttu-id="79838-122">메트릭을 문자열 배열로</span><span class="sxs-lookup"><span data-stu-id="79838-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="79838-123">-이름</span><span class="sxs-lookup"><span data-stu-id="79838-123">-Name</span></span>
<span data-ttu-id="79838-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="79838-124">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79838-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79838-125">-ResourceGroupName</span></span>
<span data-ttu-id="79838-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="79838-126">Resource Group Name</span></span>

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

### <span data-ttu-id="79838-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="79838-127">-StartTime</span></span>
<span data-ttu-id="79838-128">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="79838-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="79838-129">-Web app</span><span class="sxs-lookup"><span data-stu-id="79838-129">-WebApp</span></span>
<span data-ttu-id="79838-130">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="79838-130">WebApp object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79838-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79838-131">CommonParameters</span></span>
<span data-ttu-id="79838-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79838-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79838-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79838-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79838-134">입력</span><span class="sxs-lookup"><span data-stu-id="79838-134">INPUTS</span></span>

### <span data-ttu-id="79838-135">Site</span><span class="sxs-lookup"><span data-stu-id="79838-135">Site</span></span>
<span data-ttu-id="79838-136">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79838-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="79838-137">출력</span><span class="sxs-lookup"><span data-stu-id="79838-137">OUTPUTS</span></span>

## <span data-ttu-id="79838-138">상속자</span><span class="sxs-lookup"><span data-stu-id="79838-138">NOTES</span></span>

## <span data-ttu-id="79838-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79838-139">RELATED LINKS</span></span>

[<span data-ttu-id="79838-140">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="79838-140">Get-AzureRmWebAppCertificate</span></span>](./Get-AzureRmWebAppCertificate.md)

