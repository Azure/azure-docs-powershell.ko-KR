---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493126"
---
# <span data-ttu-id="08f06-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="08f06-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="08f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f06-102">SYNOPSIS</span></span>
<span data-ttu-id="08f06-103">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-103">Creates a new activity log profile.</span></span> <span data-ttu-id="08f06-104">이 프로필은 활동 로그를 Azure Storage 계정에 보관하거나 동일한 구독의 Azure 이벤트 허브로 스트림하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="08f06-105">구문</span><span class="sxs-lookup"><span data-stu-id="08f06-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f06-106">설명</span><span class="sxs-lookup"><span data-stu-id="08f06-106">DESCRIPTION</span></span>
<span data-ttu-id="08f06-107">**Add-AzLogProfile** cmdlet은 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="08f06-108">**Storage 계정** - 표준 스토리지 계정(Premium Storage 계정은 지원되지 않습니다)만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="08f06-109">클래식 또는 클래식 형식일 ARM 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="08f06-110">저장소 계정에 기록된 경우 활동 로그를 저장하는 비용은 일반 표준 저장소 요금으로 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="08f06-111">구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 저장소 계정만 활동 로그를 내보내는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="08f06-112">**이벤트 허브** - 구독당 하나의 로그 프로필만 있을 수 있습니다. 따라서 구독당 하나의 이벤트 허브만 활동 로그를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="08f06-113">활동 로그가 이벤트 허브로 스트리밍된 경우 표준 이벤트 허브 가격 책정이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="08f06-114">활동 로그에서 이벤트는 지역에 대한 것이거나 "전역"일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="08f06-115">전역은 기본적으로 이러한 이벤트는 지역 독립적이며 지역과 독립적입니다. 실제로 대부분의 이벤트는 이 범주에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="08f06-116">활동 로그 프로필이 포털에서 설정된 경우 사용자 인터페이스에서 선택한 다른 지역과 함께 "전역"을 암시적으로 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="08f06-117">cmdlet을 사용하는 경우 다른 지역과 별도로 "전역"으로 위치를 명시적으로 언급해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="08f06-118">**참고** :- **위치에서 "전역"을** 설정하지 못하면 대부분의 활동 로그가 내보내지지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="08f06-119">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="08f06-120">예제</span><span class="sxs-lookup"><span data-stu-id="08f06-120">EXAMPLES</span></span>

### <span data-ttu-id="08f06-121">예제 1: 위치 조건과 일치하는 활동 로그를 저장소 계정으로 내보내는 새 로그 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="08f06-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="08f06-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="08f06-122">Example 2</span></span>

<span data-ttu-id="08f06-123">새 활동 로그 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-123">Creates a new activity log profile.</span></span> <span data-ttu-id="08f06-124">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="08f06-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="08f06-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08f06-125">PARAMETERS</span></span>

### <span data-ttu-id="08f06-126">-Category</span><span class="sxs-lookup"><span data-stu-id="08f06-126">-Category</span></span>
<span data-ttu-id="08f06-127">범주 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="08f06-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f06-128">-DefaultProfile</span></span>
<span data-ttu-id="08f06-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="08f06-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08f06-130">-Location</span><span class="sxs-lookup"><span data-stu-id="08f06-130">-Location</span></span>
<span data-ttu-id="08f06-131">로그 프로필의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="08f06-132">유효한 값: 아래 cmdlet을 실행하여 최신 위치 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="08f06-133">Get-AzLocation | DisplayName 선택</span><span class="sxs-lookup"><span data-stu-id="08f06-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="08f06-134">-Name</span><span class="sxs-lookup"><span data-stu-id="08f06-134">-Name</span></span>
<span data-ttu-id="08f06-135">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="08f06-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="08f06-136">-RetentionInDays</span></span>
<span data-ttu-id="08f06-137">보존 정책(일)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="08f06-138">지정된 저장소 계정에서 로그가 보존되는 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="08f06-139">데이터를 보존하기 위해 이 데이터를 **0으로 설정합니다.**</span><span class="sxs-lookup"><span data-stu-id="08f06-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="08f06-140">지정하지 않으면 기본값은 **0입니다.**</span><span class="sxs-lookup"><span data-stu-id="08f06-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="08f06-141">일반 표준 저장소 또는 이벤트 허브 청구 요금은 데이터 보존에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="08f06-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="08f06-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="08f06-143">Service Bus 규칙의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="08f06-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="08f06-144">-StorageAccountId</span></span>
<span data-ttu-id="08f06-145">Storage 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="08f06-146">ID는 저장소 계정의 정식 리소스 ID입니다. 예를 들면 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="08f06-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="08f06-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="08f06-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08f06-148">-Confirm</span></span>
<span data-ttu-id="08f06-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f06-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f06-150">-WhatIf</span></span>
<span data-ttu-id="08f06-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="08f06-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08f06-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f06-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f06-153">CommonParameters</span></span>
<span data-ttu-id="08f06-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="08f06-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f06-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08f06-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f06-156">입력</span><span class="sxs-lookup"><span data-stu-id="08f06-156">INPUTS</span></span>

### <span data-ttu-id="08f06-157">System.String</span><span class="sxs-lookup"><span data-stu-id="08f06-157">System.String</span></span>

### <span data-ttu-id="08f06-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08f06-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08f06-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08f06-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="08f06-160">출력</span><span class="sxs-lookup"><span data-stu-id="08f06-160">OUTPUTS</span></span>

### <span data-ttu-id="08f06-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="08f06-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="08f06-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="08f06-162">NOTES</span></span>

## <span data-ttu-id="08f06-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08f06-163">RELATED LINKS</span></span>

[<span data-ttu-id="08f06-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="08f06-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="08f06-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="08f06-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


