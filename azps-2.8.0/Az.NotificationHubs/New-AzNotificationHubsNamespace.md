---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: a9675f2473488d1415a83ae0454a3841cd10d589
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872538"
---
# <span data-ttu-id="f2e1b-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e1b-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="f2e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2e1b-103">알림 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="f2e1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2e1b-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2e1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2e1b-106">**새 AzNotificationHubsNamespace** cmdlet은 알림 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="f2e1b-107">네임 스페이스는 알림 허브를 구성 하 고 관리 하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="f2e1b-108">적어도 하나 이상의 알림 허브 네임 스페이스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="f2e1b-109">단일 네임 스페이스는 여러 허브를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="f2e1b-110">여러 네임 스페이스를 사용 하 여 허브를 구성 하거나 특정 개인에 게 허브의 선택 된 하위 집합을 관리 하기 위한 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="f2e1b-111">네임 스페이스를 만들려면 네임 스페이스에 대 한 고유한 이름을 지정 해야 합니다. 네임 스페이스의 위치를 지정할 데이터 센터를 지정 합니다. 네임 스페이스에 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="f2e1b-112">네임 스페이스를 만든 후에는 New-AzNotificationHubsNamespaceAuthorizationRules cmdlet을 사용 하 여 해당 네임 스페이스에 권한 부여 규칙을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="f2e1b-113">권한 부여 규칙은 네임 스페이스에 대 한 사용 권한을 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="f2e1b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f2e1b-114">EXAMPLES</span></span>

### <span data-ttu-id="f2e1b-115">예제 1: 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="f2e1b-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="f2e1b-116">이 명령은 ContosoPartners 이라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="f2e1b-117">네임 스페이스는 서쪽 US 데이터 센터에 위치 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="f2e1b-118">예제 2: 태그를 사용 하 여 알림 허브 만들기</span><span class="sxs-lookup"><span data-stu-id="f2e1b-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="f2e1b-119">이 명령은 ContosoPartners 이라는 알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="f2e1b-120">네임 스페이스는 서쪽 US 데이터 센터에 위치 하 고 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="f2e1b-121">또한이 명령은 이름 대상과 값이 지정 된 조직으로 태그를 만들고 네임 스페이스에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="f2e1b-122">이렇게 하면 대상 그룹 태그가 있는 항목에 대해 필터링 할 때마다 네임 스페이스를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="f2e1b-123">변수</span><span class="sxs-lookup"><span data-stu-id="f2e1b-123">PARAMETERS</span></span>

### <span data-ttu-id="f2e1b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2e1b-124">-DefaultProfile</span></span>
<span data-ttu-id="f2e1b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2e1b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2e1b-126">-위치</span><span class="sxs-lookup"><span data-stu-id="f2e1b-126">-Location</span></span>
<span data-ttu-id="f2e1b-127">네임 스페이스를 호스팅할 데이터 센터의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="f2e1b-128">이 매개 변수를 올바른 위치로 설정할 수 있지만 최적의 성능을 위해 대부분의 사용자에 게 있는 데이터 센터를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="f2e1b-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f2e1b-129">-Namespace</span></span>
<span data-ttu-id="f2e1b-130">새 네임 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="f2e1b-131">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f2e1b-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2e1b-132">-ResourceGroup</span></span>
<span data-ttu-id="f2e1b-133">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="f2e1b-134">리소스 그룹은 간단 하 게 관리 및 관리를 위한 방법으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="f2e1b-135">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="f2e1b-135">-SkuTier</span></span>
<span data-ttu-id="f2e1b-136">네임 스페이스의 Sku 계층</span><span class="sxs-lookup"><span data-stu-id="f2e1b-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="f2e1b-137">태그</span><span class="sxs-lookup"><span data-stu-id="f2e1b-137">-Tag</span></span>
<span data-ttu-id="f2e1b-138">Azure 항목을 분류 하 고 구성 하는 데 사용할 수 있는 이름-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="f2e1b-139">태그는 키워드와 유사 하 게 작동 하며 배포에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="f2e1b-140">예를 들어 태그 부서가 있는 모든 항목을 검색 하는 경우 항목 유형, 위치 또는 리소스 그룹과 관계 없이 해당 태그가 있는 모든 Azure 항목이 검색 결과로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="f2e1b-141">개별 태그는 *이름* , 선택적으로 *값* 등의 두 부분으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="f2e1b-142">예를 들어 부서에서는 태그 이름이 부서이 고 tag 값은입니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="f2e1b-143">태그를 추가 하려면 다음과 같이 태그를 만드는 해시 테이블 구문을 사용 합니다. CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="f2e1b-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

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

### <span data-ttu-id="f2e1b-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f2e1b-144">-Confirm</span></span>
<span data-ttu-id="f2e1b-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2e1b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2e1b-146">-WhatIf</span></span>
<span data-ttu-id="f2e1b-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2e1b-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2e1b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2e1b-149">CommonParameters</span></span>
<span data-ttu-id="f2e1b-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2e1b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2e1b-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2e1b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2e1b-152">입력</span><span class="sxs-lookup"><span data-stu-id="f2e1b-152">INPUTS</span></span>

### <span data-ttu-id="f2e1b-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2e1b-153">System.String</span></span>

### <span data-ttu-id="f2e1b-154">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f2e1b-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f2e1b-155">출력</span><span class="sxs-lookup"><span data-stu-id="f2e1b-155">OUTPUTS</span></span>

### <span data-ttu-id="f2e1b-156">Microsoft. Azure. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f2e1b-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="f2e1b-157">상속자</span><span class="sxs-lookup"><span data-stu-id="f2e1b-157">NOTES</span></span>

## <span data-ttu-id="f2e1b-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2e1b-158">RELATED LINKS</span></span>

[<span data-ttu-id="f2e1b-159">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e1b-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f2e1b-160">제거-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e1b-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="f2e1b-161">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f2e1b-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


