---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 802dabc8373e1f3a97c66b9a9a7a121383b68287
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195300"
---
# <span data-ttu-id="1230e-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="1230e-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="1230e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1230e-102">SYNOPSIS</span></span>
<span data-ttu-id="1230e-103">Application Insights 리소스에 대한 Application Insights API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="1230e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1230e-104">SYNTAX</span></span>

### <span data-ttu-id="1230e-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1230e-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1230e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1230e-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1230e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1230e-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1230e-108">설명</span><span class="sxs-lookup"><span data-stu-id="1230e-108">DESCRIPTION</span></span>
<span data-ttu-id="1230e-109">Application Insights 리소스에 대한 Application Insights API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="1230e-110">예제</span><span class="sxs-lookup"><span data-stu-id="1230e-110">EXAMPLES</span></span>

### <span data-ttu-id="1230e-111">예제 1 Application Insights 리소스에 대한 API 키 얻기</span><span class="sxs-lookup"><span data-stu-id="1230e-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="1230e-112">리소스 그룹 "testGroup"에서 리소스 "테스트"에 대한 Application Insights API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="1230e-113">예제 2 Application Insights 리소스에 대한 특정 API 키 얻기</span><span class="sxs-lookup"><span data-stu-id="1230e-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="1230e-114">리소스 그룹 "testGroup"의 리소스 "테스트"에 대해 ID가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867"인 특정 Application Insights API 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="1230e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1230e-115">PARAMETERS</span></span>

### <span data-ttu-id="1230e-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="1230e-116">-ApiKeyId</span></span>
<span data-ttu-id="1230e-117">Application Insights Api 키 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="1230e-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1230e-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="1230e-119">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="1230e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1230e-120">-DefaultProfile</span></span>
<span data-ttu-id="1230e-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1230e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1230e-122">-Name</span></span>
<span data-ttu-id="1230e-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="1230e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1230e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1230e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1230e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1230e-126">-ResourceId</span></span>
<span data-ttu-id="1230e-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="1230e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1230e-128">CommonParameters</span></span>
<span data-ttu-id="1230e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1230e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1230e-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1230e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1230e-131">입력</span><span class="sxs-lookup"><span data-stu-id="1230e-131">INPUTS</span></span>

### <span data-ttu-id="1230e-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1230e-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="1230e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1230e-133">System.String</span></span>

## <span data-ttu-id="1230e-134">출력</span><span class="sxs-lookup"><span data-stu-id="1230e-134">OUTPUTS</span></span>

### <span data-ttu-id="1230e-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="1230e-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="1230e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1230e-136">NOTES</span></span>

## <span data-ttu-id="1230e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1230e-137">RELATED LINKS</span></span>
