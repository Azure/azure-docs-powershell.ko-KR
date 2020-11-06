---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534872"
---
# <span data-ttu-id="db9dc-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="db9dc-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="db9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="db9dc-103">Applciation insights 리소스에서 연속 내보내기 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db9dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db9dc-104">SYNTAX</span></span>

### <span data-ttu-id="db9dc-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="db9dc-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db9dc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9dc-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db9dc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9dc-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9dc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="db9dc-108">DESCRIPTION</span></span>
<span data-ttu-id="db9dc-109">Applciation insights 리소스에서 연속 내보내기 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="db9dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db9dc-110">EXAMPLES</span></span>

### <span data-ttu-id="db9dc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="db9dc-111">Example 1</span></span>
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

<span data-ttu-id="db9dc-112">"요청" 및 "추적" 문서를 "teststorageaccount"의 저장소 컨테이너로 내보내려면 "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" 리소스 그룹에서 "test" 리소스의 연속 내보내기 구성을 업데이트 하세요. "testgroup". SAS 토큰은 유효 해야 하 고 컨테이너에 대 한 쓰기 권한이 있어야 하며, 그렇지 않은 경우에는 연속 내보내기 기능이 작동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="db9dc-113">SAS 토큰이 만료 되 면 연속 내보내기 기능이 작동을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="db9dc-114">변수</span><span class="sxs-lookup"><span data-stu-id="db9dc-114">PARAMETERS</span></span>

### <span data-ttu-id="db9dc-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="db9dc-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="db9dc-116">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="db9dc-116">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-117">-확인</span><span class="sxs-lookup"><span data-stu-id="db9dc-117">-Confirm</span></span>
<span data-ttu-id="db9dc-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9dc-119">-DefaultProfile</span></span>
<span data-ttu-id="db9dc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="db9dc-121">-DisableConfiguration</span></span>
<span data-ttu-id="db9dc-122">연속 내보내기를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-122">Disable continuous export or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="db9dc-123">-DocumentType</span></span>
<span data-ttu-id="db9dc-124">내보내야 할 문서 형식</span><span class="sxs-lookup"><span data-stu-id="db9dc-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-125">-ExportId</span><span class="sxs-lookup"><span data-stu-id="db9dc-125">-ExportId</span></span>
<span data-ttu-id="db9dc-126">Application Insights 연속 내보내기 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-127">-이름</span><span class="sxs-lookup"><span data-stu-id="db9dc-127">-Name</span></span>
<span data-ttu-id="db9dc-128">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-128">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db9dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="db9dc-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db9dc-131">-ResourceId</span></span>
<span data-ttu-id="db9dc-132">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-132">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="db9dc-133">-StorageAccountId</span></span>
<span data-ttu-id="db9dc-134">대상 저장소 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="db9dc-135">-StorageLocation</span></span>
<span data-ttu-id="db9dc-136">대상 저장소 위치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="db9dc-137">-StorageSASUri</span></span>
<span data-ttu-id="db9dc-138">대상 저장소 SAS uri입니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9dc-139">-WhatIf</span></span>
<span data-ttu-id="db9dc-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db9dc-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9dc-142">CommonParameters</span></span>
<span data-ttu-id="db9dc-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db9dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9dc-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9dc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9dc-145">입력</span><span class="sxs-lookup"><span data-stu-id="db9dc-145">INPUTS</span></span>

### <span data-ttu-id="db9dc-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db9dc-146">System.String</span></span>
<span data-ttu-id="db9dc-147">System.webserver [] System. 부울</span><span class="sxs-lookup"><span data-stu-id="db9dc-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="db9dc-148">출력</span><span class="sxs-lookup"><span data-stu-id="db9dc-148">OUTPUTS</span></span>

### <span data-ttu-id="db9dc-149">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="db9dc-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="db9dc-150">상속자</span><span class="sxs-lookup"><span data-stu-id="db9dc-150">NOTES</span></span>

## <span data-ttu-id="db9dc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db9dc-151">RELATED LINKS</span></span>

