---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 996dc0ee168b11ecf3610b0d977854e32dd769bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702327"
---
# <span data-ttu-id="23d8a-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="23d8a-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="23d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="23d8a-103">Applciation insights 리소스에서 연속 내보내기 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23d8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23d8a-104">SYNTAX</span></span>

### <span data-ttu-id="23d8a-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="23d8a-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23d8a-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d8a-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23d8a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23d8a-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d8a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23d8a-108">DESCRIPTION</span></span>
<span data-ttu-id="23d8a-109">Applciation insights 리소스에서 연속 내보내기 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="23d8a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23d8a-110">EXAMPLES</span></span>

### <span data-ttu-id="23d8a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="23d8a-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="23d8a-112">"요청" 및 "추적" 문서를 "teststorageaccount"의 저장소 컨테이너로 내보내려면 "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" 리소스 그룹에서 "test" 리소스의 연속 내보내기 구성을 업데이트 하세요. "testgroup". SAS 토큰은 유효 해야 하 고 컨테이너에 대 한 쓰기 권한이 있어야 하며, 그렇지 않은 경우에는 연속 내보내기 기능이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="23d8a-113">SAS 토큰이 만료 되 면 연속 내보내기 기능이 작동을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="23d8a-114">변수</span><span class="sxs-lookup"><span data-stu-id="23d8a-114">PARAMETERS</span></span>

### <span data-ttu-id="23d8a-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="23d8a-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="23d8a-116">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="23d8a-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="23d8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d8a-117">-DefaultProfile</span></span>
<span data-ttu-id="23d8a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d8a-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="23d8a-119">-DisableConfiguration</span></span>
<span data-ttu-id="23d8a-120">연속 내보내기를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="23d8a-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="23d8a-121">-DocumentType</span></span>
<span data-ttu-id="23d8a-122">내보내야 할 문서 형식</span><span class="sxs-lookup"><span data-stu-id="23d8a-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="23d8a-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="23d8a-123">-ExportId</span></span>
<span data-ttu-id="23d8a-124">Application Insights 연속 내보내기 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="23d8a-125">-이름</span><span class="sxs-lookup"><span data-stu-id="23d8a-125">-Name</span></span>
<span data-ttu-id="23d8a-126">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="23d8a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d8a-127">-ResourceGroupName</span></span>
<span data-ttu-id="23d8a-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="23d8a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23d8a-129">-ResourceId</span></span>
<span data-ttu-id="23d8a-130">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="23d8a-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="23d8a-131">-StorageAccountId</span></span>
<span data-ttu-id="23d8a-132">대상 저장소 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="23d8a-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="23d8a-133">-StorageLocation</span></span>
<span data-ttu-id="23d8a-134">대상 저장소 위치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="23d8a-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="23d8a-135">-StorageSASUri</span></span>
<span data-ttu-id="23d8a-136">대상 저장소 SAS uri입니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="23d8a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="23d8a-137">-Confirm</span></span>
<span data-ttu-id="23d8a-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d8a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d8a-139">-WhatIf</span></span>
<span data-ttu-id="23d8a-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23d8a-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d8a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d8a-142">CommonParameters</span></span>
<span data-ttu-id="23d8a-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23d8a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d8a-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23d8a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d8a-145">입력</span><span class="sxs-lookup"><span data-stu-id="23d8a-145">INPUTS</span></span>

### <span data-ttu-id="23d8a-146">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="23d8a-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="23d8a-147">매개 변수: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="23d8a-147">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="23d8a-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23d8a-148">System.String</span></span>

## <span data-ttu-id="23d8a-149">출력</span><span class="sxs-lookup"><span data-stu-id="23d8a-149">OUTPUTS</span></span>

### <span data-ttu-id="23d8a-150">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="23d8a-150">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="23d8a-151">상속자</span><span class="sxs-lookup"><span data-stu-id="23d8a-151">NOTES</span></span>

## <span data-ttu-id="23d8a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23d8a-152">RELATED LINKS</span></span>
