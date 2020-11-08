---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3BCEADF3-15DC-4033-A94A-4C8B4F5E7340
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotMetric.md
ms.openlocfilehash: 27800007756f8de91f23feab2f3cc1bd5206aa76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041847"
---
# <span data-ttu-id="fb291-101">Get-AzWebAppSlotMetric</span><span class="sxs-lookup"><span data-stu-id="fb291-101">Get-AzWebAppSlotMetric</span></span>

## <span data-ttu-id="fb291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb291-102">SYNOPSIS</span></span>
<span data-ttu-id="fb291-103">Azure Web App 슬롯에 대 한 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb291-103">Gets metrics for an Azure Web App slot.</span></span>

## <span data-ttu-id="fb291-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb291-104">SYNTAX</span></span>

### <span data-ttu-id="fb291-105">S1</span><span class="sxs-lookup"><span data-stu-id="fb291-105">S1</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb291-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="fb291-106">S2</span></span>
```
Get-AzWebAppSlotMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb291-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb291-107">DESCRIPTION</span></span>
<span data-ttu-id="fb291-108">**AzWebAppSlotMetric** 에서 지정 된 슬롯에 대 한 웹 앱 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb291-108">The **Get-AzWebAppSlotMetric** gets Web App metrics for the specified slot.</span></span>

## <span data-ttu-id="fb291-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb291-109">EXAMPLES</span></span>

### <span data-ttu-id="fb291-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb291-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="fb291-111">이 명령은 StartTime 및 EndTime 사이의 분당 지정 된 웹 앱 (PT1M-폴링 시간 1 분) 요청을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb291-111">This command gets Request of the specified Web App per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="fb291-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb291-112">PARAMETERS</span></span>

### <span data-ttu-id="fb291-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb291-113">-DefaultProfile</span></span>
<span data-ttu-id="fb291-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb291-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb291-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fb291-115">-EndTime</span></span>
<span data-ttu-id="fb291-116">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="fb291-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-117">-세분성</span><span class="sxs-lookup"><span data-stu-id="fb291-117">-Granularity</span></span>
<span data-ttu-id="fb291-118">수준을</span><span class="sxs-lookup"><span data-stu-id="fb291-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="fb291-119">-InstanceDetails</span></span>
<span data-ttu-id="fb291-120">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="fb291-120">Instance Details</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-121">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="fb291-121">-Metrics</span></span>
<span data-ttu-id="fb291-122">매트릭스</span><span class="sxs-lookup"><span data-stu-id="fb291-122">Metrics</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fb291-123">-Name</span></span>
<span data-ttu-id="fb291-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fb291-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb291-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb291-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fb291-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-127">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fb291-127">-Slot</span></span>
<span data-ttu-id="fb291-128">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fb291-128">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fb291-129">-StartTime</span></span>
<span data-ttu-id="fb291-130">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="fb291-130">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-131">-Web app</span><span class="sxs-lookup"><span data-stu-id="fb291-131">-WebApp</span></span>
<span data-ttu-id="fb291-132">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="fb291-132">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb291-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb291-133">CommonParameters</span></span>
<span data-ttu-id="fb291-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb291-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb291-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb291-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb291-136">입력</span><span class="sxs-lookup"><span data-stu-id="fb291-136">INPUTS</span></span>

### <span data-ttu-id="fb291-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb291-137">System.String</span></span>

### <span data-ttu-id="fb291-138">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="fb291-138">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fb291-139">출력</span><span class="sxs-lookup"><span data-stu-id="fb291-139">OUTPUTS</span></span>

### <span data-ttu-id="fb291-140">ResourceMetric/. m i.</span><span class="sxs-lookup"><span data-stu-id="fb291-140">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="fb291-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fb291-141">NOTES</span></span>

## <span data-ttu-id="fb291-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb291-142">RELATED LINKS</span></span>

[<span data-ttu-id="fb291-143">Get-AzAppServicePlanMetric</span><span class="sxs-lookup"><span data-stu-id="fb291-143">Get-AzAppServicePlanMetric</span></span>](./Get-AzAppServicePlanMetric.md)

[<span data-ttu-id="fb291-144">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fb291-144">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="fb291-145">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fb291-145">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)
