---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214048"
---
# <span data-ttu-id="0e85b-101">Az 허브 모듈</span><span class="sxs-lookup"><span data-stu-id="0e85b-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="0e85b-102">설명은</span><span class="sxs-lookup"><span data-stu-id="0e85b-102">Description</span></span>
<span data-ttu-id="0e85b-103">이 항목에서는 Azure 알림 허브 cmdlet에 대 한 도움말 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="0e85b-104">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼 (iOS, Android, Windows Phone 8, Windows 스토어 등)에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="0e85b-105">이러한 허브는 개별 앱과 거의 동일 합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="0e85b-106">알림 허브는 네임 스페이스 라는 논리적 컨테이너 내에 구성 되며, 공유 액세스 서명 (SAS) 권한 부여 규칙은 허브 및 네임 스페이스에 대 한 액세스를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="0e85b-107">이러한 모든 요소는 알림 허브 cmdlet을 사용 하 여 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="0e85b-108">Az 허브 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e85b-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="0e85b-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0e85b-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="0e85b-110">알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="0e85b-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="0e85b-112">알림 허브에 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="0e85b-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="0e85b-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="0e85b-114">알림 허브 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="0e85b-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="0e85b-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="0e85b-116">알림 허브에 대 한 PNS 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="0e85b-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0e85b-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="0e85b-118">알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="0e85b-120">알림 허브 네임 스페이스와 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="0e85b-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="0e85b-122">알림 허브 네임 스페이스 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="0e85b-123">새로운 AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0e85b-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="0e85b-124">알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="0e85b-125">새로운 AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="0e85b-126">권한 부여 규칙을 만들고 알림 허브에 규칙을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="0e85b-127">새로운 AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="0e85b-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="0e85b-128">NotificationHub에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="0e85b-129">새로운 AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0e85b-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="0e85b-130">알림 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-131">새로운 AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="0e85b-132">권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임 스페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-133">새로운 AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="0e85b-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="0e85b-134">네임 스페이스에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="0e85b-135">제거-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0e85b-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="0e85b-136">기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="0e85b-137">제거-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="0e85b-138">알림 허브에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="0e85b-139">제거-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0e85b-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="0e85b-140">알림 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-141">제거-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="0e85b-142">알림 허브 네임 스페이스에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0e85b-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="0e85b-144">알림 허브에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="0e85b-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="0e85b-146">알림 허브에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="0e85b-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="0e85b-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="0e85b-148">알림 허브 네임 스페이스에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="0e85b-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0e85b-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="0e85b-150">알림 허브 네임 스페이스에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e85b-150">Sets authorization rules for a notification hub namespace.</span></span>

