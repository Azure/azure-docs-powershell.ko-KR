---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 144200f95ca7cff8b4fa541666912d62ba6bd0b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966816"
---
# <span data-ttu-id="4351a-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="4351a-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="4351a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4351a-102">SYNOPSIS</span></span>
<span data-ttu-id="4351a-103">애플리케이션 인사이트 리소스에서 연속 내보내기 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="4351a-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="4351a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4351a-104">SYNTAX</span></span>

### <span data-ttu-id="4351a-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4351a-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4351a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4351a-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4351a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4351a-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4351a-108">설명</span><span class="sxs-lookup"><span data-stu-id="4351a-108">DESCRIPTION</span></span>
<span data-ttu-id="4351a-109">애플리케이션 인사이트 리소스에서 연속 내보내기 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="4351a-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="4351a-110">예제</span><span class="sxs-lookup"><span data-stu-id="4351a-110">EXAMPLES</span></span>

### <span data-ttu-id="4351a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4351a-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="4351a-112">"testgroup"에서 리소스 "test"의 연속 내보내기 구성 "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" 리소스 "testgroup"을 업데이트하여 "testtorageaccount"의 저장소 컨테이너 "testcontainer"로 "Testcontainer"를 내보낼 수 있습니다. SAS 토큰은 유효해야 합니다. 컨테이너에 대한 쓰기 권한이 있어야 합니다. 그렇지 않으면 연속 내보내기 기능이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="4351a-113">SAS 토큰이 만료되면 연속 내보내기 기능이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="4351a-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4351a-114">PARAMETERS</span></span>

### <span data-ttu-id="4351a-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4351a-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="4351a-116">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="4351a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4351a-117">-DefaultProfile</span></span>
<span data-ttu-id="4351a-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4351a-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="4351a-119">-DisableConfiguration</span></span>
<span data-ttu-id="4351a-120">연속 내보내기 또는 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-120">Disable continuous export or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4351a-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="4351a-121">-DocumentType</span></span>
<span data-ttu-id="4351a-122">내보낼 필요가 있는 문서 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="4351a-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="4351a-123">-ExportId</span></span>
<span data-ttu-id="4351a-124">Application Insights 연속 내보내기 ID.</span><span class="sxs-lookup"><span data-stu-id="4351a-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="4351a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4351a-125">-Name</span></span>
<span data-ttu-id="4351a-126">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="4351a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4351a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4351a-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="4351a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4351a-129">-ResourceId</span></span>
<span data-ttu-id="4351a-130">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="4351a-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4351a-131">-StorageAccountId</span></span>
<span data-ttu-id="4351a-132">대상 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="4351a-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="4351a-133">-StorageLocation</span></span>
<span data-ttu-id="4351a-134">대상 저장소 위치 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="4351a-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="4351a-135">-StorageSASUri</span></span>
<span data-ttu-id="4351a-136">대상 저장소 SAS uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="4351a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="4351a-137">-Confirm</span></span>
<span data-ttu-id="4351a-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4351a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4351a-139">-WhatIf</span></span>
<span data-ttu-id="4351a-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4351a-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4351a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4351a-142">CommonParameters</span></span>
<span data-ttu-id="4351a-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4351a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4351a-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4351a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4351a-145">입력</span><span class="sxs-lookup"><span data-stu-id="4351a-145">INPUTS</span></span>

### <span data-ttu-id="4351a-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4351a-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="4351a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="4351a-147">System.String</span></span>

## <span data-ttu-id="4351a-148">출력</span><span class="sxs-lookup"><span data-stu-id="4351a-148">OUTPUTS</span></span>

### <span data-ttu-id="4351a-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="4351a-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="4351a-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4351a-150">NOTES</span></span>

## <span data-ttu-id="4351a-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4351a-151">RELATED LINKS</span></span>
