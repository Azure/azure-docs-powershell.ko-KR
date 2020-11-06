---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 86ed0a3fc6dfef3dcfc111ff6d3a75dc78335924
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531497"
---
# <span data-ttu-id="3ff19-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="3ff19-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="3ff19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff19-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff19-103">Application insights 리소스에 대 한 application insights api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ff19-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ff19-104">SYNTAX</span></span>

### <span data-ttu-id="3ff19-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ff19-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff19-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff19-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff19-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff19-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff19-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3ff19-108">DESCRIPTION</span></span>
<span data-ttu-id="3ff19-109">Application insights 리소스에 대 한 application insights api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ff19-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="3ff19-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3ff19-110">EXAMPLES</span></span>

### <span data-ttu-id="3ff19-111">예제 1 application insights 리소스에 대 한 Api 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ff19-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="3ff19-112">리소스 그룹 "testGroup"의 리소스 "테스트"에 대 한 application insights api 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="3ff19-113">예제 2 application insights 리소스에 대 한 특정 API 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3ff19-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="3ff19-114">Id가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" 리소스 그룹 "testGroup"의 리소스 "테스트"에 해당 하는 특정 application insights api 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="3ff19-115">변수</span><span class="sxs-lookup"><span data-stu-id="3ff19-115">PARAMETERS</span></span>

### <span data-ttu-id="3ff19-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="3ff19-116">-ApiKeyId</span></span>
<span data-ttu-id="3ff19-117">Application Insights Api 키 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-117">Application Insights Api Key Id.</span></span>

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

### <span data-ttu-id="3ff19-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3ff19-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3ff19-119">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="3ff19-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="3ff19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff19-120">-DefaultProfile</span></span>
<span data-ttu-id="3ff19-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ff19-122">-이름</span><span class="sxs-lookup"><span data-stu-id="3ff19-122">-Name</span></span>
<span data-ttu-id="3ff19-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="3ff19-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff19-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ff19-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="3ff19-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ff19-126">-ResourceId</span></span>
<span data-ttu-id="3ff19-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="3ff19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff19-128">CommonParameters</span></span>
<span data-ttu-id="3ff19-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff19-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff19-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff19-131">입력</span><span class="sxs-lookup"><span data-stu-id="3ff19-131">INPUTS</span></span>

### <span data-ttu-id="3ff19-132">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="3ff19-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="3ff19-133">매개 변수: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ff19-133">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="3ff19-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ff19-134">System.String</span></span>

## <span data-ttu-id="3ff19-135">출력</span><span class="sxs-lookup"><span data-stu-id="3ff19-135">OUTPUTS</span></span>

### <span data-ttu-id="3ff19-136">Microsoft. Azure. m Apikey</span><span class="sxs-lookup"><span data-stu-id="3ff19-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="3ff19-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3ff19-137">NOTES</span></span>

## <span data-ttu-id="3ff19-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ff19-138">RELATED LINKS</span></span>
