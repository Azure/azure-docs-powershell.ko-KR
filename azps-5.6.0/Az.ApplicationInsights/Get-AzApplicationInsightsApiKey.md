---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 96887bebdfddec0a5393ca41bc3b552119cffe81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965259"
---
# <span data-ttu-id="c8cf4-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c8cf4-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c8cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8cf4-103">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 사용</span><span class="sxs-lookup"><span data-stu-id="c8cf4-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c8cf4-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8cf4-104">SYNTAX</span></span>

### <span data-ttu-id="c8cf4-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c8cf4-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8cf4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cf4-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8cf4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8cf4-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8cf4-108">설명</span><span class="sxs-lookup"><span data-stu-id="c8cf4-108">DESCRIPTION</span></span>
<span data-ttu-id="c8cf4-109">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 사용</span><span class="sxs-lookup"><span data-stu-id="c8cf4-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c8cf4-110">예제</span><span class="sxs-lookup"><span data-stu-id="c8cf4-110">EXAMPLES</span></span>

### <span data-ttu-id="c8cf4-111">예제 1 애플리케이션 인사이트 리소스에 대한 Api 키 Get</span><span class="sxs-lookup"><span data-stu-id="c8cf4-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="c8cf4-112">리소스 그룹 "testGroup"에서 리소스 "테스트"에 대한 application insights api 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="c8cf4-113">예제 2 애플리케이션 인사이트 리소스에 대한 특정 API 키 사용</span><span class="sxs-lookup"><span data-stu-id="c8cf4-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="c8cf4-114">"testGroup"의 리소스 "테스트"에 대한 ID가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867"인 특정 애플리케이션 인사이트 api 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c8cf4-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8cf4-115">PARAMETERS</span></span>

### <span data-ttu-id="c8cf4-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="c8cf4-116">-ApiKeyId</span></span>
<span data-ttu-id="c8cf4-117">Application Insights Api 키 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="c8cf4-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c8cf4-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c8cf4-119">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c8cf4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8cf4-120">-DefaultProfile</span></span>
<span data-ttu-id="c8cf4-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8cf4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c8cf4-122">-Name</span></span>
<span data-ttu-id="c8cf4-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c8cf4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8cf4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8cf4-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8cf4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8cf4-126">-ResourceId</span></span>
<span data-ttu-id="c8cf4-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c8cf4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8cf4-128">CommonParameters</span></span>
<span data-ttu-id="c8cf4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8cf4-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c8cf4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8cf4-131">입력</span><span class="sxs-lookup"><span data-stu-id="c8cf4-131">INPUTS</span></span>

### <span data-ttu-id="c8cf4-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c8cf4-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c8cf4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c8cf4-133">System.String</span></span>

## <span data-ttu-id="c8cf4-134">출력</span><span class="sxs-lookup"><span data-stu-id="c8cf4-134">OUTPUTS</span></span>

### <span data-ttu-id="c8cf4-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c8cf4-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c8cf4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8cf4-136">NOTES</span></span>

## <span data-ttu-id="c8cf4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8cf4-137">RELATED LINKS</span></span>
