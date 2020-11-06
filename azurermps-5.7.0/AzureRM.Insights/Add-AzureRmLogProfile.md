---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 0ef53015b3e07eeb69cdcfd0ab70c67317ab92cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536788"
---
# <span data-ttu-id="114e0-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="114e0-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="114e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="114e0-102">SYNOPSIS</span></span>
<span data-ttu-id="114e0-103">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-103">Creates a new activity log profile.</span></span> <span data-ttu-id="114e0-104">이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="114e0-105">구문과</span><span class="sxs-lookup"><span data-stu-id="114e0-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="114e0-106">설명은</span><span class="sxs-lookup"><span data-stu-id="114e0-106">DESCRIPTION</span></span>
<span data-ttu-id="114e0-107">**추가-AzureRmLogProfile** cmdlet은 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

- <span data-ttu-id="114e0-108">**저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="114e0-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="114e0-109">ARM 또는 클래식 형식이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="114e0-110">저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="114e0-111">구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="114e0-112">**이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="114e0-113">활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="114e0-114">활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="114e0-115">전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="114e0-116">활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="114e0-117">Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="114e0-118">**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="114e0-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

<span data-ttu-id="114e0-119">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="114e0-120">예제의</span><span class="sxs-lookup"><span data-stu-id="114e0-120">EXAMPLES</span></span>

### <span data-ttu-id="114e0-121">예제 1: 새 로그 프로필을 추가 하 여 위치 조건과 일치 하는 활동 로그를 저장소 계정으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="114e0-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="114e0-122">변수</span><span class="sxs-lookup"><span data-stu-id="114e0-122">PARAMETERS</span></span>

### <span data-ttu-id="114e0-123">-범주</span><span class="sxs-lookup"><span data-stu-id="114e0-123">-Category</span></span>
<span data-ttu-id="114e0-124">범주 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-124">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Categories

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114e0-125">-DefaultProfile</span></span>
<span data-ttu-id="114e0-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="114e0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="114e0-127">-위치</span><span class="sxs-lookup"><span data-stu-id="114e0-127">-Location</span></span>
<span data-ttu-id="114e0-128">로그 프로필의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="114e0-129">유효한 값: 최신 위치 목록을 가져오려면 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="114e0-130">Get-AzureLocation | DisplayName 선택</span><span class="sxs-lookup"><span data-stu-id="114e0-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: Locations

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-131">-이름</span><span class="sxs-lookup"><span data-stu-id="114e0-131">-Name</span></span>
<span data-ttu-id="114e0-132">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-132">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-133">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="114e0-133">-RetentionInDays</span></span>
<span data-ttu-id="114e0-134">보존 정책을 일 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="114e0-135">지정 된 저장소 계정에서 로그가 보존 되는 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="114e0-136">데이터를 계속 유지 하려면이를 **0** 으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="114e0-137">지정 하지 않으면 **0** 으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="114e0-138">데이터 보존에는 일반 표준 저장소나 이벤트 허브 청구 요금이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="114e0-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="114e0-140">서비스 버스 규칙의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-140">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="114e0-141">-StorageAccountId</span></span>
<span data-ttu-id="114e0-142">저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="114e0-143">ID는 저장소 계정의 정규화 된 리소스 ID입니다 예:</span><span class="sxs-lookup"><span data-stu-id="114e0-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="114e0-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="114e0-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114e0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114e0-145">CommonParameters</span></span>
<span data-ttu-id="114e0-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114e0-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114e0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114e0-148">입력</span><span class="sxs-lookup"><span data-stu-id="114e0-148">INPUTS</span></span>

### <span data-ttu-id="114e0-149">않아야</span><span class="sxs-lookup"><span data-stu-id="114e0-149">None</span></span>
<span data-ttu-id="114e0-150">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="114e0-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="114e0-151">출력</span><span class="sxs-lookup"><span data-stu-id="114e0-151">OUTPUTS</span></span>

### <span data-ttu-id="114e0-152">Microsoft Azure.. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="114e0-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="114e0-153">상속자</span><span class="sxs-lookup"><span data-stu-id="114e0-153">NOTES</span></span>

## <span data-ttu-id="114e0-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="114e0-154">RELATED LINKS</span></span>

[<span data-ttu-id="114e0-155">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="114e0-155">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="114e0-156">제거-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="114e0-156">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


