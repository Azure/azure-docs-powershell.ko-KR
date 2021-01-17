---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353517"
---
# <span data-ttu-id="195d6-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="195d6-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="195d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195d6-102">SYNOPSIS</span></span>
<span data-ttu-id="195d6-103">Application Insights 리소스에 대한 새 Application Insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="195d6-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="195d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="195d6-104">SYNTAX</span></span>

### <span data-ttu-id="195d6-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="195d6-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195d6-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="195d6-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195d6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="195d6-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195d6-108">설명</span><span class="sxs-lookup"><span data-stu-id="195d6-108">DESCRIPTION</span></span>
<span data-ttu-id="195d6-109">Application Insights 리소스에 대한 새 Application Insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="195d6-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="195d6-110">예제</span><span class="sxs-lookup"><span data-stu-id="195d6-110">EXAMPLES</span></span>

### <span data-ttu-id="195d6-111">예제 1 Application Insights 리소스에 대한 새 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="195d6-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="195d6-112">스토리지로 "요청" 및 "추적" 문서 형식을 내보내는 새 Application Insights 연속 내보내기 구성을 만들면 리소스 그룹 "testgroup"의 저장소 계정 "teststorageaccount"에 "testcontainer"가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="195d6-113">SAS 토큰은 유효해야 합니다. 컨테이너에 대한 쓰기 권한이 있어야 합니다. 그렇지 않으면 연속 내보내기 기능이 작동하지 않습니다. SAS 토큰이 만료되면 연속 내보내기 기능의 작동이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="195d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="195d6-114">PARAMETERS</span></span>

### <span data-ttu-id="195d6-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="195d6-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="195d6-116">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="195d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195d6-117">-DefaultProfile</span></span>
<span data-ttu-id="195d6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="195d6-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="195d6-119">-DocumentType</span></span>
<span data-ttu-id="195d6-120">내보내야 하는 문서 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="195d6-121">-Name</span></span>
<span data-ttu-id="195d6-122">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-122">Component Name.</span></span>

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

### <span data-ttu-id="195d6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195d6-123">-ResourceGroupName</span></span>
<span data-ttu-id="195d6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="195d6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="195d6-125">-ResourceId</span></span>
<span data-ttu-id="195d6-126">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="195d6-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="195d6-127">-StorageAccountId</span></span>
<span data-ttu-id="195d6-128">대상 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="195d6-129">-StorageLocation</span></span>
<span data-ttu-id="195d6-130">대상 저장소 위치 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="195d6-131">-StorageSASUri</span></span>
<span data-ttu-id="195d6-132">대상 저장소 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="195d6-133">-Confirm</span></span>
<span data-ttu-id="195d6-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195d6-135">-WhatIf</span></span>
<span data-ttu-id="195d6-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="195d6-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="195d6-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="195d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195d6-138">CommonParameters</span></span>
<span data-ttu-id="195d6-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="195d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195d6-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="195d6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195d6-141">입력</span><span class="sxs-lookup"><span data-stu-id="195d6-141">INPUTS</span></span>

### <span data-ttu-id="195d6-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="195d6-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="195d6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="195d6-143">System.String</span></span>

## <span data-ttu-id="195d6-144">출력</span><span class="sxs-lookup"><span data-stu-id="195d6-144">OUTPUTS</span></span>

### <span data-ttu-id="195d6-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="195d6-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="195d6-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="195d6-146">NOTES</span></span>

## <span data-ttu-id="195d6-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="195d6-147">RELATED LINKS</span></span>
