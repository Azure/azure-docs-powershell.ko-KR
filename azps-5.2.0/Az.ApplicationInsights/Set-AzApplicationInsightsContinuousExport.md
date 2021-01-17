---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: fef34358855666d0f407c72831b2973ce95cc7e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353445"
---
# <span data-ttu-id="cd021-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="cd021-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="cd021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd021-102">SYNOPSIS</span></span>
<span data-ttu-id="cd021-103">Application Insights 리소스에서 연속 내보내기 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cd021-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="cd021-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd021-104">SYNTAX</span></span>

### <span data-ttu-id="cd021-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd021-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd021-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd021-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd021-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd021-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd021-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd021-108">DESCRIPTION</span></span>
<span data-ttu-id="cd021-109">Application Insights 리소스에서 연속 내보내기 구성 업데이트</span><span class="sxs-lookup"><span data-stu-id="cd021-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="cd021-110">예제</span><span class="sxs-lookup"><span data-stu-id="cd021-110">EXAMPLES</span></span>

### <span data-ttu-id="cd021-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd021-111">Example 1</span></span>
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

<span data-ttu-id="cd021-112">리소스 그룹 "testgroup"에서 리소스 "test"의 연속 내보내기 구성 "jlTFEiBg1rkDXOCIeJQ2mB2TxZg="를 업데이트하여 "testtorageaccount"의 저장소 컨테이너 "testcontainer"로 "Request" 및 "Trace" 문서를 내보낼 수 있습니다. SAS 토큰은 유효해야 합니다. 컨테이너에 대한 쓰기 권한이 있어야 합니다. 그렇지 않으면 연속 내보내기 기능이 작동하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="cd021-113">SAS 토큰이 만료되면 연속 내보내기 기능의 작동이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="cd021-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd021-114">PARAMETERS</span></span>

### <span data-ttu-id="cd021-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cd021-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="cd021-116">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="cd021-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd021-117">-DefaultProfile</span></span>
<span data-ttu-id="cd021-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd021-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd021-119">-DisableConfiguration</span></span>
<span data-ttu-id="cd021-120">연속 내보내기 사용 안 하게 설정</span><span class="sxs-lookup"><span data-stu-id="cd021-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="cd021-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="cd021-121">-DocumentType</span></span>
<span data-ttu-id="cd021-122">내보내야 하는 문서 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="cd021-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="cd021-123">-ExportId</span></span>
<span data-ttu-id="cd021-124">Application Insights 연속 내보내기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="cd021-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cd021-125">-Name</span></span>
<span data-ttu-id="cd021-126">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="cd021-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd021-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd021-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd021-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd021-129">-ResourceId</span></span>
<span data-ttu-id="cd021-130">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="cd021-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cd021-131">-StorageAccountId</span></span>
<span data-ttu-id="cd021-132">대상 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="cd021-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="cd021-133">-StorageLocation</span></span>
<span data-ttu-id="cd021-134">대상 저장소 위치 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="cd021-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="cd021-135">-StorageSASUri</span></span>
<span data-ttu-id="cd021-136">대상 저장소 SAS uri입니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="cd021-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd021-137">-Confirm</span></span>
<span data-ttu-id="cd021-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd021-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd021-139">-WhatIf</span></span>
<span data-ttu-id="cd021-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cd021-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd021-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd021-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd021-142">CommonParameters</span></span>
<span data-ttu-id="cd021-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd021-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd021-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd021-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd021-145">입력</span><span class="sxs-lookup"><span data-stu-id="cd021-145">INPUTS</span></span>

### <span data-ttu-id="cd021-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="cd021-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="cd021-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cd021-147">System.String</span></span>

## <span data-ttu-id="cd021-148">출력</span><span class="sxs-lookup"><span data-stu-id="cd021-148">OUTPUTS</span></span>

### <span data-ttu-id="cd021-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd021-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="cd021-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd021-150">NOTES</span></span>

## <span data-ttu-id="cd021-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd021-151">RELATED LINKS</span></span>
