---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppMetric.md
ms.openlocfilehash: 834470fa5ab1c35fb3235329d6eb57b2b5e8ba34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698357"
---
# <span data-ttu-id="2202e-101">Get-AzWebAppMetric</span><span class="sxs-lookup"><span data-stu-id="2202e-101">Get-AzWebAppMetric</span></span>

## <span data-ttu-id="2202e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2202e-102">SYNOPSIS</span></span>
<span data-ttu-id="2202e-103">Azure Web App 메트릭스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2202e-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="2202e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2202e-104">SYNTAX</span></span>

### <span data-ttu-id="2202e-105">S1</span><span class="sxs-lookup"><span data-stu-id="2202e-105">S1</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2202e-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="2202e-106">S2</span></span>
```
Get-AzWebAppMetric [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2202e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2202e-107">DESCRIPTION</span></span>
<span data-ttu-id="2202e-108">**Get-AzWebAppMetric** 는 웹 앱 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2202e-108">The **Get-AzWebAppMetric** gets Web App metrics.</span></span>

## <span data-ttu-id="2202e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2202e-109">EXAMPLES</span></span>

### <span data-ttu-id="2202e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2202e-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetric -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics "Requests"
```

<span data-ttu-id="2202e-111">이 명령은 StartTime 및 EndTime 사이의 분 당 웹 앱 ContosoWebApp (PT1M-폴링 시간 1 분) 요청을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2202e-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="2202e-112">변수</span><span class="sxs-lookup"><span data-stu-id="2202e-112">PARAMETERS</span></span>

### <span data-ttu-id="2202e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2202e-113">-DefaultProfile</span></span>
<span data-ttu-id="2202e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2202e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2202e-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2202e-115">-EndTime</span></span>
<span data-ttu-id="2202e-116">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="2202e-116">End Time in UTC</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2202e-117">-세분성</span><span class="sxs-lookup"><span data-stu-id="2202e-117">-Granularity</span></span>
<span data-ttu-id="2202e-118">수준을</span><span class="sxs-lookup"><span data-stu-id="2202e-118">Granularity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2202e-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="2202e-119">-InstanceDetails</span></span>
<span data-ttu-id="2202e-120">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="2202e-120">Instance Details</span></span>

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

### <span data-ttu-id="2202e-121">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="2202e-121">-Metrics</span></span>
<span data-ttu-id="2202e-122">메트릭을 문자열 배열로</span><span class="sxs-lookup"><span data-stu-id="2202e-122">Metrics as a string array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2202e-123">-이름</span><span class="sxs-lookup"><span data-stu-id="2202e-123">-Name</span></span>
<span data-ttu-id="2202e-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2202e-124">WebApp Name</span></span>

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

### <span data-ttu-id="2202e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2202e-125">-ResourceGroupName</span></span>
<span data-ttu-id="2202e-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2202e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2202e-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2202e-127">-StartTime</span></span>
<span data-ttu-id="2202e-128">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="2202e-128">Start Time in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2202e-129">-Web app</span><span class="sxs-lookup"><span data-stu-id="2202e-129">-WebApp</span></span>
<span data-ttu-id="2202e-130">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="2202e-130">WebApp object</span></span>

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

### <span data-ttu-id="2202e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2202e-131">CommonParameters</span></span>
<span data-ttu-id="2202e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2202e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2202e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2202e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2202e-134">입력</span><span class="sxs-lookup"><span data-stu-id="2202e-134">INPUTS</span></span>

### <span data-ttu-id="2202e-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2202e-135">System.String</span></span>

### <span data-ttu-id="2202e-136">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="2202e-136">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2202e-137">출력</span><span class="sxs-lookup"><span data-stu-id="2202e-137">OUTPUTS</span></span>

### <span data-ttu-id="2202e-138">ResourceMetric/. m i.</span><span class="sxs-lookup"><span data-stu-id="2202e-138">Microsoft.Azure.Management.WebSites.Models.ResourceMetric</span></span>

## <span data-ttu-id="2202e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2202e-139">NOTES</span></span>

## <span data-ttu-id="2202e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2202e-140">RELATED LINKS</span></span>

[<span data-ttu-id="2202e-141">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="2202e-141">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

