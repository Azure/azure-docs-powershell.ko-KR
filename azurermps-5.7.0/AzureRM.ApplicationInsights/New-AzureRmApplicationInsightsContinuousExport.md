---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 1e4dd5f65789751f9a28deb9e10c37221f45b97b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703591"
---
# <span data-ttu-id="e4fb9-101">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="e4fb9-101">New-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="e4fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fb9-103">Application insights 리소스에 대 한 새 application insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="e4fb9-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4fb9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4fb9-104">SYNTAX</span></span>

### <span data-ttu-id="e4fb9-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4fb9-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4fb9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4fb9-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4fb9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4fb9-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4fb9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e4fb9-108">DESCRIPTION</span></span>
<span data-ttu-id="e4fb9-109">Application insights 리소스에 대 한 새 application insights 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="e4fb9-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="e4fb9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e4fb9-110">EXAMPLES</span></span>

### <span data-ttu-id="e4fb9-111">예제 1 application insights 리소스에 대 한 새 연속 내보내기 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="e4fb9-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
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

<span data-ttu-id="e4fb9-112">"요청" 및 "추적" 문서 유형을 저장소로 내보내기 위한 새 application insights 연속 내보내기 구성을 만듭니다. "teststorageaccount" 리소스 그룹의 "testcontainer" 저장소 계정에 "에서"를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="e4fb9-113">SAS 토큰은 유효 해야 하 고 컨테이너에 대 한 쓰기 권한이 있어야 하며, 그렇지 않은 경우에는 연속 내보내기 기능이 작동 하지 않습니다. SAS 토큰이 만료 되 면 연속 내보내기 기능이 작동을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="e4fb9-114">변수</span><span class="sxs-lookup"><span data-stu-id="e4fb9-114">PARAMETERS</span></span>

### <span data-ttu-id="e4fb9-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e4fb9-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="e4fb9-116">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="e4fb9-117">-확인</span><span class="sxs-lookup"><span data-stu-id="e4fb9-117">-Confirm</span></span>
<span data-ttu-id="e4fb9-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4fb9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fb9-119">-DefaultProfile</span></span>
<span data-ttu-id="e4fb9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4fb9-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="e4fb9-121">-DocumentType</span></span>
<span data-ttu-id="e4fb9-122">내보내야 할 문서 형식</span><span class="sxs-lookup"><span data-stu-id="e4fb9-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="e4fb9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="e4fb9-123">-Name</span></span>
<span data-ttu-id="e4fb9-124">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-124">Component Name.</span></span>

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

### <span data-ttu-id="e4fb9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4fb9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e4fb9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4fb9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4fb9-127">-ResourceId</span></span>
<span data-ttu-id="e4fb9-128">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-128">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="e4fb9-129">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e4fb9-129">-StorageAccountId</span></span>
<span data-ttu-id="e4fb9-130">대상 저장소 계정 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-130">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="e4fb9-131">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="e4fb9-131">-StorageLocation</span></span>
<span data-ttu-id="e4fb9-132">대상 저장소 위치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-132">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="e4fb9-133">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="e4fb9-133">-StorageSASUri</span></span>
<span data-ttu-id="e4fb9-134">대상 저장소 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-134">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="e4fb9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4fb9-135">-WhatIf</span></span>
<span data-ttu-id="e4fb9-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4fb9-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4fb9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fb9-138">CommonParameters</span></span>
<span data-ttu-id="e4fb9-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fb9-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4fb9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fb9-141">입력</span><span class="sxs-lookup"><span data-stu-id="e4fb9-141">INPUTS</span></span>

### <span data-ttu-id="e4fb9-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4fb9-142">System.String</span></span>
<span data-ttu-id="e4fb9-143">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e4fb9-143">System.String[]</span></span>

## <span data-ttu-id="e4fb9-144">출력</span><span class="sxs-lookup"><span data-stu-id="e4fb9-144">OUTPUTS</span></span>

### <span data-ttu-id="e4fb9-145">PSExportConfiguration-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e4fb9-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="e4fb9-146">상속자</span><span class="sxs-lookup"><span data-stu-id="e4fb9-146">NOTES</span></span>

## <span data-ttu-id="e4fb9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4fb9-147">RELATED LINKS</span></span>

