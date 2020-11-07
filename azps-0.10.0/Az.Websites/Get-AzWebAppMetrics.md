---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 513BE097-EB4A-4C49-9F7F-42A2BED09022
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppMetrics.md
ms.openlocfilehash: 9a3aeabc3eb38127b37ca4ab6a12975c51daea5b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876155"
---
# <span data-ttu-id="b13a2-101">Get-AzWebAppMetrics</span><span class="sxs-lookup"><span data-stu-id="b13a2-101">Get-AzWebAppMetrics</span></span>

## <span data-ttu-id="b13a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13a2-102">SYNOPSIS</span></span>
<span data-ttu-id="b13a2-103">Azure Web App 메트릭스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-103">Gets Azure Web App metrics.</span></span>

## <span data-ttu-id="b13a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b13a2-104">SYNTAX</span></span>

### <span data-ttu-id="b13a2-105">S1</span><span class="sxs-lookup"><span data-stu-id="b13a2-105">S1</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b13a2-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="b13a2-106">S2</span></span>
```
Get-AzWebAppMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b13a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b13a2-107">DESCRIPTION</span></span>
<span data-ttu-id="b13a2-108">**Get-AzWebAppMetrics** 는 웹 앱 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-108">The **Get-AzWebAppMetrics** gets Web App metrics.</span></span>

## <span data-ttu-id="b13a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b13a2-109">EXAMPLES</span></span>

### <span data-ttu-id="b13a2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b13a2-110">Example 1</span></span>
```
PS C:\> Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["Requests"]
```

<span data-ttu-id="b13a2-111">이 명령은 StartTime 및 EndTime 사이의 분 당 웹 앱 ContosoWebApp (PT1M-폴링 시간 1 분) 요청을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-111">This command gets Requests of the Web App ContosoWebApp per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="b13a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="b13a2-112">PARAMETERS</span></span>

### <span data-ttu-id="b13a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13a2-113">-DefaultProfile</span></span>
<span data-ttu-id="b13a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13a2-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b13a2-115">-EndTime</span></span>
<span data-ttu-id="b13a2-116">UTC의 종료 시간</span><span class="sxs-lookup"><span data-stu-id="b13a2-116">End Time in UTC</span></span>

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

### <span data-ttu-id="b13a2-117">-세분성</span><span class="sxs-lookup"><span data-stu-id="b13a2-117">-Granularity</span></span>
<span data-ttu-id="b13a2-118">수준을</span><span class="sxs-lookup"><span data-stu-id="b13a2-118">Granularity</span></span>

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

### <span data-ttu-id="b13a2-119">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="b13a2-119">-InstanceDetails</span></span>
<span data-ttu-id="b13a2-120">인스턴스 세부 정보</span><span class="sxs-lookup"><span data-stu-id="b13a2-120">Instance Details</span></span>

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

### <span data-ttu-id="b13a2-121">-메트릭스</span><span class="sxs-lookup"><span data-stu-id="b13a2-121">-Metrics</span></span>
<span data-ttu-id="b13a2-122">메트릭을 문자열 배열로</span><span class="sxs-lookup"><span data-stu-id="b13a2-122">Metrics as a string array</span></span>

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

### <span data-ttu-id="b13a2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b13a2-123">-Name</span></span>
<span data-ttu-id="b13a2-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="b13a2-124">WebApp Name</span></span>

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

### <span data-ttu-id="b13a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="b13a2-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b13a2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b13a2-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b13a2-127">-StartTime</span></span>
<span data-ttu-id="b13a2-128">UTC의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="b13a2-128">Start Time in UTC</span></span>

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

### <span data-ttu-id="b13a2-129">-Web app</span><span class="sxs-lookup"><span data-stu-id="b13a2-129">-WebApp</span></span>
<span data-ttu-id="b13a2-130">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="b13a2-130">WebApp object</span></span>

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

### <span data-ttu-id="b13a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13a2-131">CommonParameters</span></span>
<span data-ttu-id="b13a2-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13a2-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13a2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13a2-134">입력</span><span class="sxs-lookup"><span data-stu-id="b13a2-134">INPUTS</span></span>

### <span data-ttu-id="b13a2-135">Site</span><span class="sxs-lookup"><span data-stu-id="b13a2-135">Site</span></span>
<span data-ttu-id="b13a2-136">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13a2-136">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b13a2-137">출력</span><span class="sxs-lookup"><span data-stu-id="b13a2-137">OUTPUTS</span></span>

## <span data-ttu-id="b13a2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b13a2-138">NOTES</span></span>

## <span data-ttu-id="b13a2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b13a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="b13a2-140">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="b13a2-140">Get-AzWebAppCertificate</span></span>](./Get-AzWebAppCertificate.md)

