---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: c4ed6fc65a3f785f78a86c7f495486e95404f3d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689338"
---
# <span data-ttu-id="54989-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="54989-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="54989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54989-102">SYNOPSIS</span></span>
<span data-ttu-id="54989-103">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54989-103">Creates a new activity log profile.</span></span> <span data-ttu-id="54989-104">이 프로필을 사용 하 여 활동 로그를 Azure storage 계정에 보관 하거나 같은 구독의 Azure 이벤트 허브에 스트리밍할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="54989-105">구문과</span><span class="sxs-lookup"><span data-stu-id="54989-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54989-106">설명은</span><span class="sxs-lookup"><span data-stu-id="54989-106">DESCRIPTION</span></span>
<span data-ttu-id="54989-107">**추가-AzLogProfile** cmdlet은 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54989-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="54989-108">**저장소 계정** -표준 저장소 계정 (premium 저장소 계정 (지원 되지 않음)이 지원 되지 않음).</span><span class="sxs-lookup"><span data-stu-id="54989-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="54989-109">ARM 또는 클래식 형식이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="54989-110">저장소 계정에 기록 된 경우 활동 로그를 저장 하는 비용은 표준 저장소 요금으로 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54989-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="54989-111">구독 당 하나의 로그 프로필만 있을 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 저장소 계정만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="54989-112">**이벤트 허브** -구독 당 하나의 로그 프로필만 사용할 수 있습니다 consequentially 활동 로그 내보내기에는 구독 당 하나의 이벤트 허브가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="54989-113">활동 로그가 이벤트 허브로 스트리밍되는 경우 표준 이벤트 허브 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54989-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="54989-114">활동 로그에서 이벤트는 지역과 관련이 있거나 "전역" 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="54989-115">전역 본질적으로 이러한 이벤트는 영역 agnostics 지역에 관계 없이 대부분의 이벤트가이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="54989-116">활동 로그 프로필이 포털에서 설정 된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "Global"이 암시적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54989-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="54989-117">Cmdlet을 사용 하는 경우에는 "전역"으로 위치를 명시적으로 다른 지역과 별도로 언급 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="54989-118">**참고** : **위치에 "Global"을 설정 하지 않으면 대부분의 활동 로그가 내보내지지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="54989-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="54989-119">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="54989-120">예제의</span><span class="sxs-lookup"><span data-stu-id="54989-120">EXAMPLES</span></span>

### <span data-ttu-id="54989-121">예제 1: 새 로그 프로필을 추가 하 여 위치 조건과 일치 하는 활동 로그를 저장소 계정으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="54989-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="54989-122">변수</span><span class="sxs-lookup"><span data-stu-id="54989-122">PARAMETERS</span></span>

### <span data-ttu-id="54989-123">-범주</span><span class="sxs-lookup"><span data-stu-id="54989-123">-Category</span></span>
<span data-ttu-id="54989-124">범주 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-124">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="54989-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54989-125">-DefaultProfile</span></span>
<span data-ttu-id="54989-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54989-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54989-127">-위치</span><span class="sxs-lookup"><span data-stu-id="54989-127">-Location</span></span>
<span data-ttu-id="54989-128">로그 프로필의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="54989-129">유효한 값: 최신 위치 목록을 가져오려면 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="54989-130">Get-AzLocation | DisplayName 선택</span><span class="sxs-lookup"><span data-stu-id="54989-130">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="54989-131">-이름</span><span class="sxs-lookup"><span data-stu-id="54989-131">-Name</span></span>
<span data-ttu-id="54989-132">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="54989-133">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="54989-133">-RetentionInDays</span></span>
<span data-ttu-id="54989-134">보존 정책을 일 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="54989-135">지정 된 저장소 계정에서 로그가 보존 되는 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="54989-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="54989-136">데이터를 계속 유지 하려면이를 **0** 으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="54989-137">지정 하지 않으면 **0** 으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54989-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="54989-138">데이터 보존에는 일반 표준 저장소나 이벤트 허브 청구 요금이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54989-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="54989-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="54989-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="54989-140">서비스 버스 규칙의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="54989-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="54989-141">-StorageAccountId</span></span>
<span data-ttu-id="54989-142">저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="54989-143">ID는 저장소 계정의 정규화 된 리소스 ID입니다 예:</span><span class="sxs-lookup"><span data-stu-id="54989-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="54989-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="54989-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="54989-145">-확인</span><span class="sxs-lookup"><span data-stu-id="54989-145">-Confirm</span></span>
<span data-ttu-id="54989-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54989-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54989-147">-WhatIf</span></span>
<span data-ttu-id="54989-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54989-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54989-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54989-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54989-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54989-150">CommonParameters</span></span>
<span data-ttu-id="54989-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54989-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54989-152">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54989-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54989-153">입력</span><span class="sxs-lookup"><span data-stu-id="54989-153">INPUTS</span></span>

### <span data-ttu-id="54989-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54989-154">System.String</span></span>

### <span data-ttu-id="54989-155">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="54989-155">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54989-156">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54989-156">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="54989-157">출력</span><span class="sxs-lookup"><span data-stu-id="54989-157">OUTPUTS</span></span>

### <span data-ttu-id="54989-158">Microsoft Azure.. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="54989-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="54989-159">상속자</span><span class="sxs-lookup"><span data-stu-id="54989-159">NOTES</span></span>

## <span data-ttu-id="54989-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54989-160">RELATED LINKS</span></span>

[<span data-ttu-id="54989-161">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="54989-161">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="54989-162">제거-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="54989-162">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


