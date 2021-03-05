---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 63c31e07313f7e6ad3e1eea25977e85f3e4c6b53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965243"
---
# <span data-ttu-id="30711-101">Get-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="30711-101">Get-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="30711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30711-102">SYNOPSIS</span></span>
<span data-ttu-id="30711-103">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 연속 내보내기 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30711-103">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="30711-104">구문</span><span class="sxs-lookup"><span data-stu-id="30711-104">SYNTAX</span></span>

### <span data-ttu-id="30711-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="30711-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30711-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30711-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ExportId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30711-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30711-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsContinuousExport [-ResourceId] <String> [[-ExportId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30711-108">설명</span><span class="sxs-lookup"><span data-stu-id="30711-108">DESCRIPTION</span></span>
<span data-ttu-id="30711-109">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 연속 내보내기 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30711-109">Get application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="30711-110">예제</span><span class="sxs-lookup"><span data-stu-id="30711-110">EXAMPLES</span></span>

### <span data-ttu-id="30711-111">예제 1 애플리케이션 인사이트 리소스에 대한 연속 내보내기</span><span class="sxs-lookup"><span data-stu-id="30711-111">Example 1 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"

ExportId                     DocumentTypes                ExportStatus DestinationStorageAccountId
--------                     -------------                ------------ ---------------------------
ZJrfffySPdtG3ESn3iRxVIEFuNY= Request, Performance Counter Preparing    /subscriptions/{subid}...
```

<span data-ttu-id="30711-112">리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 애플리케이션 인사이트 연속 내보내기 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30711-112">Get application insights continuous export configurations for resource named "test" in resource group "testgroup"</span></span>

### <span data-ttu-id="30711-113">예제 2 애플리케이션 인사이트 리소스에 대한 연속 내보내기</span><span class="sxs-lookup"><span data-stu-id="30711-113">Example 2 Get continuous export for an application insights resource</span></span>
```
PS C:\> Get-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "ZJrfffySPdtG3ESn3iRxVIEFuNY="

ExportId                         : ZJrfffySPdtG3ESn3iRxVIEFuNY=
StorageName                      : targetaccount
ContainerName                    : continuousexport
DocumentTypes                    : Request, Performance Counter
DestinationStorageSubscriptionId : {subid}
DestinationStorageLocationId     : eastus
DestinationStorageAccountId      : /subscriptions/{subid}/resourceGroups/targetstorage/providers/Microsoft.Storage/storageAccounts/targetaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="30711-114">리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 내보내기 ID "ZJrfffySPdtG3ESn3iRxVIEFuNY="를 통해 애플리케이션 인사이트 연속 내보내기 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30711-114">Get application insights continuous export configuration with export id "ZJrfffySPdtG3ESn3iRxVIEFuNY=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="30711-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="30711-115">PARAMETERS</span></span>

### <span data-ttu-id="30711-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30711-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="30711-117">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="30711-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="30711-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30711-118">-DefaultProfile</span></span>
<span data-ttu-id="30711-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30711-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30711-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="30711-120">-ExportId</span></span>
<span data-ttu-id="30711-121">Application Insights 연속 내보내기 ID.</span><span class="sxs-lookup"><span data-stu-id="30711-121">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="30711-122">-Name</span><span class="sxs-lookup"><span data-stu-id="30711-122">-Name</span></span>
<span data-ttu-id="30711-123">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30711-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="30711-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30711-124">-ResourceGroupName</span></span>
<span data-ttu-id="30711-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30711-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="30711-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30711-126">-ResourceId</span></span>
<span data-ttu-id="30711-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30711-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="30711-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30711-128">CommonParameters</span></span>
<span data-ttu-id="30711-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30711-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30711-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="30711-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30711-131">입력</span><span class="sxs-lookup"><span data-stu-id="30711-131">INPUTS</span></span>

### <span data-ttu-id="30711-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="30711-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="30711-133">System.String</span><span class="sxs-lookup"><span data-stu-id="30711-133">System.String</span></span>

## <span data-ttu-id="30711-134">출력</span><span class="sxs-lookup"><span data-stu-id="30711-134">OUTPUTS</span></span>

### <span data-ttu-id="30711-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="30711-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="30711-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30711-136">NOTES</span></span>

## <span data-ttu-id="30711-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30711-137">RELATED LINKS</span></span>
