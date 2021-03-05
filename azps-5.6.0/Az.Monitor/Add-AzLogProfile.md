---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980320"
---
# <span data-ttu-id="f244b-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f244b-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="f244b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f244b-102">SYNOPSIS</span></span>
<span data-ttu-id="f244b-103">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-103">Creates a new activity log profile.</span></span> <span data-ttu-id="f244b-104">이 프로필은 활동 로그를 Azure Storage 계정에 보관하거나 동일한 구독의 Azure 이벤트 허브로 스트리밍하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="f244b-105">구문</span><span class="sxs-lookup"><span data-stu-id="f244b-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f244b-106">설명</span><span class="sxs-lookup"><span data-stu-id="f244b-106">DESCRIPTION</span></span>
<span data-ttu-id="f244b-107">**Add-AzLogProfile** cmdlet은 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="f244b-108">**Storage 계정** - 표준 저장소 계정(프리미엄 저장소 계정이 지원되지 않습니다)만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="f244b-109">형식은 클래식 또는 ARM 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="f244b-110">저장소 계정에 기록된 경우 활동 로그를 저장하는 비용은 일반 표준 저장소 요금으로 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="f244b-111">구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 저장소 계정만 활동 로그를 내보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="f244b-112">**Event Hub** - 구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 이벤트 허브만 활동 로그를 내보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="f244b-113">활동 로그가 이벤트 허브로 스트리밍된 경우 표준 이벤트 허브 가격 책정이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="f244b-114">활동 로그에서 이벤트는 지역에 대한 것일 수 있습니다. 또는 "전역"일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="f244b-115">전역은 기본적으로 이러한 이벤트가 지역 무지정적이며 지역과 독립적입니다. 사실 대부분의 이벤트는 이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="f244b-116">활동 로그 프로필이 포털에서 설정되어 있는 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 암시적으로 "전역"을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="f244b-117">cmdlet을 사용하는 경우 다른 지역과 별도로 "전역"으로 위치를 명시적으로 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="f244b-118">**참고** :- **위치에서 "전역"을** 설정하지 못하면 대부분의 활동 로그가 내보내지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="f244b-119">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f244b-120">예제</span><span class="sxs-lookup"><span data-stu-id="f244b-120">EXAMPLES</span></span>

### <span data-ttu-id="f244b-121">예제 1: 위치 조건과 일치하는 활동 로그를 저장소 계정에 내보낼 새 로그 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="f244b-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="f244b-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="f244b-122">Example 2</span></span>

<span data-ttu-id="f244b-123">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-123">Creates a new activity log profile.</span></span> <span data-ttu-id="f244b-124">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="f244b-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="f244b-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f244b-125">PARAMETERS</span></span>

### <span data-ttu-id="f244b-126">-Category</span><span class="sxs-lookup"><span data-stu-id="f244b-126">-Category</span></span>
<span data-ttu-id="f244b-127">범주 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="f244b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f244b-128">-DefaultProfile</span></span>
<span data-ttu-id="f244b-129">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f244b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f244b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f244b-130">-Location</span></span>
<span data-ttu-id="f244b-131">로그 프로필의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="f244b-132">유효한 값: cmdlet 아래에서 실행하여 위치의 최신 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="f244b-133">Get-AzLocation | DisplayName 선택</span><span class="sxs-lookup"><span data-stu-id="f244b-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="f244b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f244b-134">-Name</span></span>
<span data-ttu-id="f244b-135">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f244b-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f244b-136">-RetentionInDays</span></span>
<span data-ttu-id="f244b-137">보존 정책을 며칠 동안 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="f244b-138">지정된 저장소 계정에 로그가 보존되는 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="f244b-139">데이터를 영원히 유지하면 **을 0으로 설정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f244b-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="f244b-140">지정되지 않은 경우 기본값은 **0입니다.**</span><span class="sxs-lookup"><span data-stu-id="f244b-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="f244b-141">일반 표준 저장소 또는 이벤트 허브 청구 요금은 데이터 보존에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="f244b-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="f244b-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="f244b-143">Service Bus 규칙의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="f244b-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f244b-144">-StorageAccountId</span></span>
<span data-ttu-id="f244b-145">Storage 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="f244b-146">ID는 저장소 계정의 정식 리소스 ID입니다.(예:</span><span class="sxs-lookup"><span data-stu-id="f244b-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="f244b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="f244b-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="f244b-148">-확인</span><span class="sxs-lookup"><span data-stu-id="f244b-148">-Confirm</span></span>
<span data-ttu-id="f244b-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f244b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f244b-150">-WhatIf</span></span>
<span data-ttu-id="f244b-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f244b-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f244b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f244b-153">CommonParameters</span></span>
<span data-ttu-id="f244b-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f244b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f244b-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f244b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f244b-156">입력</span><span class="sxs-lookup"><span data-stu-id="f244b-156">INPUTS</span></span>

### <span data-ttu-id="f244b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f244b-157">System.String</span></span>

### <span data-ttu-id="f244b-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f244b-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f244b-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f244b-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f244b-160">출력</span><span class="sxs-lookup"><span data-stu-id="f244b-160">OUTPUTS</span></span>

### <span data-ttu-id="f244b-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="f244b-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="f244b-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f244b-162">NOTES</span></span>

## <span data-ttu-id="f244b-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f244b-163">RELATED LINKS</span></span>

[<span data-ttu-id="f244b-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f244b-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="f244b-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f244b-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


