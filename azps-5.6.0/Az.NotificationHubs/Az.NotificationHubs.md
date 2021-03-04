---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951424"
---
# <span data-ttu-id="496d8-101">Az.NotificationHubs 모듈</span><span class="sxs-lookup"><span data-stu-id="496d8-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="496d8-102">설명</span><span class="sxs-lookup"><span data-stu-id="496d8-102">Description</span></span>
<span data-ttu-id="496d8-103">이 항목에서는 Azure Notification Hub cmdlet에 대한 도움말 항목을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="496d8-104">알림 허브는 해당 클라이언트에서 사용하는 플랫폼(iOS, Android, Windows Phone 8, Windows Store 등)에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="496d8-105">이러한 허브는 개별 앱과 거의 동일합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="496d8-106">알림 허브는 네임스페이스라고 하는 논리 컨테이너 내에서 구성됩니다. SAS(공유 액세스 서명) 권한 부여 규칙은 허브 및 네임스페이스에 대한 액세스를 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="496d8-107">이러한 모든 요소는 Notification Hub cmdlet을 사용하여 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="496d8-108">Az.NotificationHubs Cmdlet</span><span class="sxs-lookup"><span data-stu-id="496d8-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="496d8-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="496d8-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="496d8-110">알림 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="496d8-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="496d8-112">알림 허브와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="496d8-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="496d8-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="496d8-114">알림 허브 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="496d8-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="496d8-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="496d8-116">알림 허브에 대한 PNS 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="496d8-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="496d8-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="496d8-118">알림 허브 네임스페이스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="496d8-120">알림 허브 네임스페이스와 연결된 권한 부여 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="496d8-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="496d8-122">알림 허브 네임스페이스 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="496d8-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="496d8-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="496d8-124">알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="496d8-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="496d8-126">권한 부여 규칙을 만들고 알림 허브에 규칙을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="496d8-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="496d8-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="496d8-128">NotificationHub에 대한 권한 부여 규칙 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="496d8-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="496d8-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="496d8-130">알림 허브 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="496d8-132">권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임스페이스에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="496d8-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="496d8-134">네임스페이스에 대한 권한 부여 규칙 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="496d8-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="496d8-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="496d8-136">기존 알림 허브를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="496d8-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="496d8-138">알림 허브에서 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="496d8-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="496d8-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="496d8-140">알림 허브 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="496d8-142">알림 허브 네임스페이스에서 권한 부여 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="496d8-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="496d8-144">알림 허브에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="496d8-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="496d8-146">알림 허브에 대한 권한 부여 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="496d8-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="496d8-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="496d8-148">알림 허브 네임스페이스에 대한 속성 값을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="496d8-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="496d8-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="496d8-150">알림 허브 네임스페이스에 대한 권한 부여 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="496d8-150">Sets authorization rules for a notification hub namespace.</span></span>

