---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 9a17dfd649f35da3fa071eb7c6d2752d3a923398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699880"
---
# <span data-ttu-id="e2971-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e2971-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="e2971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2971-102">SYNOPSIS</span></span>
<span data-ttu-id="e2971-103">알림 허브 네임 스페이스에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="e2971-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2971-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2971-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2971-105">DESCRIPTION</span></span>
<span data-ttu-id="e2971-106">**Set-AzNotificationHubsNamespace** cmdlet은 기존 알림 허브 네임 스페이스의 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="e2971-107">네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="e2971-108">적어도 하나 이상의 알림 허브 네임 스페이스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="e2971-109">또한 모든 알림 허브에는 지정 된 네임 스페이스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="e2971-110">이 cmdlet은 주로 네임 스페이스를 사용 하거나 사용 하지 않도록 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="e2971-111">네임 스페이스를 사용 하지 않도록 설정 하면 사용자가 네임 스페이스의 알림 허브에 연결할 수 없으며 관리자가 해당 허브를 사용 하 여 푸시 알림을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="e2971-112">비활성화 된 네임 스페이스를 다시 사용 하도록 설정 하려면이 cmdlet을 사용 하 여 네임 스페이스의 **State** 속성을 Active로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="e2971-113">이 cmdlet을 사용 하 여 네임 스페이스에 중요 한 태그를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="e2971-114">이렇게 하면 네임 스페이스가 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="e2971-115">중요 한 네임 스페이스를 제거 하려면 먼저 중요 한 태그를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="e2971-116">예제의</span><span class="sxs-lookup"><span data-stu-id="e2971-116">EXAMPLES</span></span>

### <span data-ttu-id="e2971-117">예제 1: 네임 스페이스 비활성화</span><span class="sxs-lookup"><span data-stu-id="e2971-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="e2971-118">이 명령은 ContosoPartners 라는 네임 스페이스를 사용 하지 않도록 설정 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="e2971-119">예제 2: 네임 스페이스 사용</span><span class="sxs-lookup"><span data-stu-id="e2971-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="e2971-120">이 명령은 ContosoPartners 라는 네임 스페이스를 사용 하도록 설정 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="e2971-121">변수</span><span class="sxs-lookup"><span data-stu-id="e2971-121">PARAMETERS</span></span>

### <span data-ttu-id="e2971-122">-중요</span><span class="sxs-lookup"><span data-stu-id="e2971-122">-Critical</span></span>
<span data-ttu-id="e2971-123">네임 스페이스가 중요 한 네임 스페이스 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="e2971-124">중요 한 네임 스페이스는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="e2971-125">중요 한 네임 스페이스를 삭제 하려면 네임 스페이스를 중요 하지 않은 것으로 표시 하기 위해이 속성의 값을 False로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="e2971-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2971-126">-DefaultProfile</span></span>
<span data-ttu-id="e2971-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2971-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2971-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e2971-128">-Force</span></span>
<span data-ttu-id="e2971-129">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e2971-130">-위치</span><span class="sxs-lookup"><span data-stu-id="e2971-130">-Location</span></span>
<span data-ttu-id="e2971-131">네임 스페이스를 호스트 하는 데이터 센터의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="e2971-132">이 매개 변수를 유효한 Azure 위치로 설정할 수 있지만, 최적의 성능을 위해서는 대다수 사용자의 근처에 있는 데이터 센터를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="e2971-133">Azure 위치를 최신 목록으로 가져오려면 다음 명령을 실행 합니다. `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="e2971-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="e2971-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2971-134">-Namespace</span></span>
<span data-ttu-id="e2971-135">이 cmdlet이 수정 하는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="e2971-136">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e2971-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2971-137">-ResourceGroup</span></span>
<span data-ttu-id="e2971-138">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="e2971-139">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e2971-140">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="e2971-140">-SkuTier</span></span>
<span data-ttu-id="e2971-141">네임 스페이스의 Sku 계층</span><span class="sxs-lookup"><span data-stu-id="e2971-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="e2971-142">-상태</span><span class="sxs-lookup"><span data-stu-id="e2971-142">-State</span></span>
<span data-ttu-id="e2971-143">네임 스페이스의 현재 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="e2971-144">이 매개 변수에 허용 되는 값은 Active 및 Disabled입니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="e2971-145">태그</span><span class="sxs-lookup"><span data-stu-id="e2971-145">-Tag</span></span>
<span data-ttu-id="e2971-146">Azure 항목을 분류 하 고 구성 하는 데 사용할 수 있는 이름-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="e2971-147">태그는 키워드와 유사 하 게 작동 하며 배포에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="e2971-148">예를 들어 태그 부서가 있는 모든 항목을 검색 하는 경우 항목 유형, 위치 또는 리소스 그룹과 관계 없이 해당 태그가 있는 모든 Azure 항목이 검색 결과로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="e2971-149">개별 태그는 *이름* 및 *값* (선택적으로)의 두 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="e2971-150">예를 들어 부서에서는 태그 이름이 부서이 고 tag 값은입니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="e2971-151">태그를 추가 하려면 다음과 같은 해시 테이블 구문을 사용 합니다. CalendarYear (2016:-tag @ {Name = "CalendarYear")를 만듭니다. Value = "2016"} 같은 명령에 여러 태그를 추가 하려면 쉼표를 사용 하 여 개별 태그를 구분 합니다.-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="e2971-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="e2971-152">-확인</span><span class="sxs-lookup"><span data-stu-id="e2971-152">-Confirm</span></span>
<span data-ttu-id="e2971-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2971-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2971-154">-WhatIf</span></span>
<span data-ttu-id="e2971-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2971-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2971-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2971-157">CommonParameters</span></span>
<span data-ttu-id="e2971-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2971-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2971-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2971-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2971-160">입력</span><span class="sxs-lookup"><span data-stu-id="e2971-160">INPUTS</span></span>

### <span data-ttu-id="e2971-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2971-161">System.String</span></span>

### <span data-ttu-id="e2971-162">Microsoft. Azure. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="e2971-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="e2971-163">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e2971-163">System.Boolean</span></span>

### <span data-ttu-id="e2971-164">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e2971-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e2971-165">출력</span><span class="sxs-lookup"><span data-stu-id="e2971-165">OUTPUTS</span></span>

### <span data-ttu-id="e2971-166">Microsoft. Azure. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e2971-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e2971-167">상속자</span><span class="sxs-lookup"><span data-stu-id="e2971-167">NOTES</span></span>

## <span data-ttu-id="e2971-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2971-168">RELATED LINKS</span></span>

[<span data-ttu-id="e2971-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e2971-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e2971-170">새로운 AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e2971-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e2971-171">제거-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e2971-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)


