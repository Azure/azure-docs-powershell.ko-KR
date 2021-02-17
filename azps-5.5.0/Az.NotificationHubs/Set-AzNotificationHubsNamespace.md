---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191489"
---
# <span data-ttu-id="46187-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="46187-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="46187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46187-102">SYNOPSIS</span></span>
<span data-ttu-id="46187-103">알림 허브 네임스페이스에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="46187-104">구문</span><span class="sxs-lookup"><span data-stu-id="46187-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46187-105">설명</span><span class="sxs-lookup"><span data-stu-id="46187-105">DESCRIPTION</span></span>
<span data-ttu-id="46187-106">**Set-AzNotificationHubsNamespace** cmdlet은 기존 알림 허브 네임스페이스의 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="46187-107">네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="46187-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="46187-108">알림 허브 네임스페이스가 하나 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="46187-109">또한 모든 알림 허브에는 할당된 네임스페이스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="46187-110">이 cmdlet은 주로 네임스페이스를 설정하고 사용하지 않도록 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="46187-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="46187-111">네임스페이스를 사용하지 않도록 설정하면 사용자는 네임스페이스의 알림 허브에 연결할 수 없으며 관리자가 해당 허브를 사용하여 푸시 알림을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="46187-112">비활성화된 네임스페이스를 다시 사용하도록 설정하려면 이 cmdlet을 사용하여 네임스페이스의 **상태** 속성을 활성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="46187-113">또한 이 cmdlet을 사용하여 네임스페이스를 중요로 태그를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="46187-114">이렇게 하면 네임스페이스가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="46187-115">중요한 네임스페이스를 제거하려면 먼저 중요 태그를 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="46187-116">예제</span><span class="sxs-lookup"><span data-stu-id="46187-116">EXAMPLES</span></span>

### <span data-ttu-id="46187-117">예제 1: 네임스페이스 사용 안</span><span class="sxs-lookup"><span data-stu-id="46187-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="46187-118">이 명령은 미국 서부 데이터 센터에 있는 ContosoPartners라는 네임스페이스를 사용하지 않도록 설정하고 ContosoNotificationsGroup 리소스 그룹에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="46187-119">예제 2: 네임스페이스 사용</span><span class="sxs-lookup"><span data-stu-id="46187-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="46187-120">이 명령은 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당된 ContosoPartners라는 네임스페이스를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="46187-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46187-121">PARAMETERS</span></span>

### <span data-ttu-id="46187-122">-Critical</span><span class="sxs-lookup"><span data-stu-id="46187-122">-Critical</span></span>
<span data-ttu-id="46187-123">네임스페이스가 중요한 네임스페이스인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46187-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="46187-124">중요한 네임스페이스는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="46187-125">중요한 네임스페이스를 삭제하려면 네임스페이스를 중요하지 않은 것으로 표시하려면 이 속성의 값을 False로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46187-126">-DefaultProfile</span></span>
<span data-ttu-id="46187-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46187-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46187-128">-Force</span><span class="sxs-lookup"><span data-stu-id="46187-128">-Force</span></span>
<span data-ttu-id="46187-129">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="46187-130">-Location</span><span class="sxs-lookup"><span data-stu-id="46187-130">-Location</span></span>
<span data-ttu-id="46187-131">네임스페이스를 호스트하는 데이터 센터의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="46187-132">이 매개 변수를 유효한 모든 Azure 위치로 설정할 수 있습니다. 최적의 성능을 위해 대부분의 사용자 근처에 있는 데이터 센터를 사용하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="46187-133">Azure 위치의 최신 목록을 얻습니다. 다음 명령을 실행합니다. `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="46187-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="46187-134">-Namespace</span></span>
<span data-ttu-id="46187-135">이 cmdlet이 수정하는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="46187-136">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46187-137">-ResourceGroup</span></span>
<span data-ttu-id="46187-138">네임스페이스가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="46187-139">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="46187-140">-SkuTier</span></span>
<span data-ttu-id="46187-141">네임스페이스의 SKU 계층</span><span class="sxs-lookup"><span data-stu-id="46187-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-142">-State</span><span class="sxs-lookup"><span data-stu-id="46187-142">-State</span></span>
<span data-ttu-id="46187-143">네임스페이스의 현재 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="46187-144">이 매개 변수에 허용되는 값은 Active 및 Disabled입니다.</span><span class="sxs-lookup"><span data-stu-id="46187-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="46187-145">-Tag</span></span>
<span data-ttu-id="46187-146">Azure 항목을 분류하고 구성하는 데 사용할 수 있는 이름-값 쌍을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="46187-147">태그는 키워드와 유사하게 작동하며 배포 전반에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="46187-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="46187-148">예를 들어 Department:IT 태그를 사용하여 모든 항목을 검색하는 경우 검색은 항목 유형, 위치 또는 리소스 그룹과 같은 항목에 관계없이 해당 태그가 있는 모든 Azure 항목을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="46187-149">개별 태그는 이름과 값(선택 사항)의 두 부분으로 *구성됩니다.* </span><span class="sxs-lookup"><span data-stu-id="46187-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="46187-150">예를 들어 Department:IT에서 태그 이름은 Department, 태그 값은 IT입니다.</span><span class="sxs-lookup"><span data-stu-id="46187-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="46187-151">태그를 추가하기 위해 이와 유사한 해시 테이블 구문을 사용하여 CalendarYear:2016: -Tags @{Name="CalendarYear"라는 태그를 만듭니다. Value="2016"} 동일한 명령에 여러 태그를 추가하기 위해 콤마를 사용하여 개별 태그를 구분합니다. -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="46187-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46187-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46187-152">-Confirm</span></span>
<span data-ttu-id="46187-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46187-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46187-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46187-154">-WhatIf</span></span>
<span data-ttu-id="46187-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46187-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46187-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46187-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46187-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46187-157">CommonParameters</span></span>
<span data-ttu-id="46187-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46187-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46187-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46187-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46187-160">입력</span><span class="sxs-lookup"><span data-stu-id="46187-160">INPUTS</span></span>

### <span data-ttu-id="46187-161">System.String</span><span class="sxs-lookup"><span data-stu-id="46187-161">System.String</span></span>

### <span data-ttu-id="46187-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="46187-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="46187-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46187-163">System.Boolean</span></span>

### <span data-ttu-id="46187-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46187-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46187-165">출력</span><span class="sxs-lookup"><span data-stu-id="46187-165">OUTPUTS</span></span>

### <span data-ttu-id="46187-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="46187-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="46187-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46187-167">NOTES</span></span>

## <span data-ttu-id="46187-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46187-168">RELATED LINKS</span></span>

[<span data-ttu-id="46187-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="46187-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="46187-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="46187-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="46187-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="46187-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


