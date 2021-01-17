---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491750"
---
# <span data-ttu-id="5b50d-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5b50d-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="5b50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b50d-102">SYNOPSIS</span></span>
<span data-ttu-id="5b50d-103">알림 허브 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="5b50d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b50d-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b50d-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b50d-105">DESCRIPTION</span></span>
<span data-ttu-id="5b50d-106">**New-AzNotificationHubsNamespace** cmdlet은 알림 허브 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="5b50d-107">네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5b50d-108">알림 허브 네임스페이스가 하나 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="5b50d-109">단일 네임스페이스는 여러 허브를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="5b50d-110">여러 네임스페이스를 사용하여 허브를 구성하거나 특정 개인에게 허브의 선택한 하위 집합을 관리할 수 있는 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="5b50d-111">네임스페이스를 만들 경우 네임스페이스에 대한 고유한 이름을 지정해야 합니다. 네임스페이스가 있는 데이터 센터를 지정합니다. 네임스페이스를 할당할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="5b50d-112">네임스페이스를 만든 후 New-AzNotificationHubsNamespaceAuthorizationRules cmdlet을 사용하여 해당 네임스페이스에 권한 부여 규칙을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="5b50d-113">권한 부여 규칙은 네임스페이스에 대한 사용 권한을 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="5b50d-114">예제</span><span class="sxs-lookup"><span data-stu-id="5b50d-114">EXAMPLES</span></span>

### <span data-ttu-id="5b50d-115">예제 1: 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="5b50d-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="5b50d-116">이 명령은 ContosoPartners라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="5b50d-117">네임스페이스는 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="5b50d-118">예제 2: 태그가 있는 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="5b50d-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="5b50d-119">이 명령은 ContosoPartners라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="5b50d-120">네임스페이스는 미국 서부 데이터 센터에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="5b50d-121">또한 이 명령은 Audience 이름과 PartnerOrganizations 값으로 태그를 만들고 네임스페이스에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="5b50d-122">이렇게 하면 대상 태그가 PartnerOrganizations로 설정된 항목에 대해 필터링할 때 네임스페이스가 표시될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="5b50d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b50d-123">PARAMETERS</span></span>

### <span data-ttu-id="5b50d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b50d-124">-DefaultProfile</span></span>
<span data-ttu-id="5b50d-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5b50d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b50d-126">-Location</span><span class="sxs-lookup"><span data-stu-id="5b50d-126">-Location</span></span>
<span data-ttu-id="5b50d-127">네임스페이스를 호스트할 데이터 센터의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="5b50d-128">이 매개 변수를 유효한 위치로 설정할 수 있습니다. 최적의 성능을 위해 대부분의 사용자 근처에 있는 데이터 센터를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="5b50d-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5b50d-129">-Namespace</span></span>
<span data-ttu-id="5b50d-130">새 네임스페이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="5b50d-131">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5b50d-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b50d-132">-ResourceGroup</span></span>
<span data-ttu-id="5b50d-133">네임스페이스를 할당할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="5b50d-134">리소스 그룹은 인벤토리 관리 및 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="5b50d-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5b50d-135">-SkuTier</span></span>
<span data-ttu-id="5b50d-136">네임스페이스의 SKU 계층</span><span class="sxs-lookup"><span data-stu-id="5b50d-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="5b50d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b50d-137">-Tag</span></span>
<span data-ttu-id="5b50d-138">Azure 항목을 분류하고 구성하는 데 사용할 수 있는 이름-값 쌍을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="5b50d-139">태그는 키워드와 유사하게 작동하며 배포 전반에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="5b50d-140">예를 들어 Department:IT 태그를 사용하여 모든 항목을 검색하는 경우 검색은 항목 유형, 위치 또는 리소스 그룹과 같은 항목에 관계없이 해당 태그가 있는 모든 Azure 항목을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="5b50d-141">개별 태그는 이름 및 선택적으로 *값의* 두 부분으로 *구성됩니다.*</span><span class="sxs-lookup"><span data-stu-id="5b50d-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="5b50d-142">예를 들어 Department:IT에서 태그 이름은 Department, 태그 값은 IT입니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="5b50d-143">태그를 추가하기 위해 이와 유사한 해시 테이블 구문을 사용하여 CalendarYear:2016 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b50d-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b50d-144">-Confirm</span></span>
<span data-ttu-id="5b50d-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b50d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b50d-146">-WhatIf</span></span>
<span data-ttu-id="5b50d-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b50d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b50d-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b50d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b50d-149">CommonParameters</span></span>
<span data-ttu-id="5b50d-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b50d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b50d-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b50d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b50d-152">입력</span><span class="sxs-lookup"><span data-stu-id="5b50d-152">INPUTS</span></span>

### <span data-ttu-id="5b50d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5b50d-153">System.String</span></span>

### <span data-ttu-id="5b50d-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5b50d-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5b50d-155">출력</span><span class="sxs-lookup"><span data-stu-id="5b50d-155">OUTPUTS</span></span>

### <span data-ttu-id="5b50d-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5b50d-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="5b50d-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b50d-157">NOTES</span></span>

## <span data-ttu-id="5b50d-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b50d-158">RELATED LINKS</span></span>

[<span data-ttu-id="5b50d-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5b50d-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5b50d-160">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5b50d-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5b50d-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5b50d-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


