---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537184"
---
# <span data-ttu-id="1fcf5-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf5-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="1fcf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcf5-103">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-103">Creates a new activity log profile.</span></span> <span data-ttu-id="1fcf5-104">이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="1fcf5-105">**저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="1fcf5-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="1fcf5-106">ARM 또는 클래식 형식이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="1fcf5-107">저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="1fcf5-108">구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="1fcf5-109">**이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="1fcf5-110">활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="1fcf5-111">활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="1fcf5-112">전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="1fcf5-113">활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="1fcf5-114">Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="1fcf5-115">**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="1fcf5-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fcf5-116">구문과</span><span class="sxs-lookup"><span data-stu-id="1fcf5-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fcf5-117">설명은</span><span class="sxs-lookup"><span data-stu-id="1fcf5-117">DESCRIPTION</span></span>
<span data-ttu-id="1fcf5-118">**추가-AzureRmLogProfile** cmdlet은 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="1fcf5-119">예제의</span><span class="sxs-lookup"><span data-stu-id="1fcf5-119">EXAMPLES</span></span>

### <span data-ttu-id="1fcf5-120">예제 1: 새 로그 프로필을 추가 하 여 위치 조건과 일치 하는 활동 로그를 저장소 계정으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="1fcf5-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="1fcf5-121">변수</span><span class="sxs-lookup"><span data-stu-id="1fcf5-121">PARAMETERS</span></span>

### <span data-ttu-id="1fcf5-122">-범주</span><span class="sxs-lookup"><span data-stu-id="1fcf5-122">-Categories</span></span>
<span data-ttu-id="1fcf5-123">범주 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-123">Specifies the list of categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-124">-위치</span><span class="sxs-lookup"><span data-stu-id="1fcf5-124">-Locations</span></span>
<span data-ttu-id="1fcf5-125">로그 프로필의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="1fcf5-126">유효한 값: 최신 위치 목록을 가져오려면 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="1fcf5-127">Get-AzureLocation | DisplayName 선택</span><span class="sxs-lookup"><span data-stu-id="1fcf5-127">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1fcf5-128">-Name</span></span>
<span data-ttu-id="1fcf5-129">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-129">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-130">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="1fcf5-130">-RetentionInDays</span></span>
<span data-ttu-id="1fcf5-131">보존 정책을 일 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="1fcf5-132">지정 된 저장소 계정에서 로그가 보존 되는 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="1fcf5-133">데이터를 계속 유지 하려면이를 **0** 으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="1fcf5-134">지정 하지 않으면 **0** 으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="1fcf5-135">데이터 보존에는 일반 표준 저장소나 이벤트 허브 청구 요금이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="1fcf5-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="1fcf5-137">서비스 버스 규칙의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-137">Specifies the ID of the Service Bus rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1fcf5-138">-StorageAccountId</span></span>
<span data-ttu-id="1fcf5-139">저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="1fcf5-140">ID는 저장소 계정의 정규화 된 리소스 ID입니다 예:</span><span class="sxs-lookup"><span data-stu-id="1fcf5-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="1fcf5-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="1fcf5-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fcf5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf5-142">-DefaultProfile</span></span>
<span data-ttu-id="1fcf5-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fcf5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcf5-144">CommonParameters</span></span>
<span data-ttu-id="1fcf5-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fcf5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcf5-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fcf5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcf5-147">입력</span><span class="sxs-lookup"><span data-stu-id="1fcf5-147">INPUTS</span></span>

## <span data-ttu-id="1fcf5-148">출력</span><span class="sxs-lookup"><span data-stu-id="1fcf5-148">OUTPUTS</span></span>

### <span data-ttu-id="1fcf5-149">Microsoft Azure.. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf5-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="1fcf5-150">상속자</span><span class="sxs-lookup"><span data-stu-id="1fcf5-150">NOTES</span></span>

## <span data-ttu-id="1fcf5-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fcf5-151">RELATED LINKS</span></span>

[<span data-ttu-id="1fcf5-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf5-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="1fcf5-153">제거-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="1fcf5-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


