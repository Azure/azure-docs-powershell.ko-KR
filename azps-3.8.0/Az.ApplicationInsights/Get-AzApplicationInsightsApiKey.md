---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 802dabc8373e1f3a97c66b9a9a7a121383b68287
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044155"
---
# <span data-ttu-id="3207d-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="3207d-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="3207d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3207d-102">SYNOPSIS</span></span>
<span data-ttu-id="3207d-103">Application insights 리소스에 대 한 application insights api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3207d-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="3207d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3207d-104">SYNTAX</span></span>

### <span data-ttu-id="3207d-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3207d-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3207d-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3207d-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3207d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3207d-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3207d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3207d-108">DESCRIPTION</span></span>
<span data-ttu-id="3207d-109">Application insights 리소스에 대 한 application insights api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3207d-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="3207d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3207d-110">EXAMPLES</span></span>

### <span data-ttu-id="3207d-111">예제 1 application insights 리소스에 대 한 Api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3207d-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="3207d-112">리소스 그룹 "testGroup"의 리소스 "테스트"에 대 한 application insights api 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="3207d-113">예제 2 application insights 리소스에 대 한 특정 API 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3207d-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="3207d-114">Id가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" 리소스 그룹 "testGroup"의 리소스 "테스트"에 해당 하는 특정 application insights api 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="3207d-115">변수</span><span class="sxs-lookup"><span data-stu-id="3207d-115">PARAMETERS</span></span>

### <span data-ttu-id="3207d-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="3207d-116">-ApiKeyId</span></span>
<span data-ttu-id="3207d-117">Application Insights Api 키 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3207d-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3207d-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3207d-119">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="3207d-119">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3207d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3207d-120">-DefaultProfile</span></span>
<span data-ttu-id="3207d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3207d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3207d-122">-Name</span></span>
<span data-ttu-id="3207d-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3207d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3207d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3207d-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3207d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3207d-126">-ResourceId</span></span>
<span data-ttu-id="3207d-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3207d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3207d-128">CommonParameters</span></span>
<span data-ttu-id="3207d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3207d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3207d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3207d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3207d-131">입력</span><span class="sxs-lookup"><span data-stu-id="3207d-131">INPUTS</span></span>

### <span data-ttu-id="3207d-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="3207d-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="3207d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3207d-133">System.String</span></span>

## <span data-ttu-id="3207d-134">출력</span><span class="sxs-lookup"><span data-stu-id="3207d-134">OUTPUTS</span></span>

### <span data-ttu-id="3207d-135">Microsoft. Azure. m Apikey</span><span class="sxs-lookup"><span data-stu-id="3207d-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="3207d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3207d-136">NOTES</span></span>

## <span data-ttu-id="3207d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3207d-137">RELATED LINKS</span></span>
