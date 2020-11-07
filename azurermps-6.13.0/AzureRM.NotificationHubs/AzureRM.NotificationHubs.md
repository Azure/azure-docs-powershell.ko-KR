---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93688764"
---
# <span data-ttu-id="9366d-101">AzureRM Hub 모듈</span><span class="sxs-lookup"><span data-stu-id="9366d-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="9366d-102">설명은</span><span class="sxs-lookup"><span data-stu-id="9366d-102">Description</span></span>
<span data-ttu-id="9366d-103">이 항목에서는 Azure 알림 허브 cmdlet에 대 한 도움말 항목을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="9366d-104">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼 (iOS, Android, Windows Phone 8, Windows 스토어 등)에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="9366d-105">이러한 허브는 개별 앱과 거의 동일 합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="9366d-106">알림 허브는 네임 스페이스 라는 논리적 컨테이너 내에 구성 되며, 공유 액세스 서명 (SAS) 권한 부여 규칙은 허브 및 네임 스페이스에 대 한 액세스를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="9366d-107">이러한 모든 요소는 알림 허브 cmdlet을 사용 하 여 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="9366d-108">AzureRM Hub Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9366d-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="9366d-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9366d-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="9366d-110">알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="9366d-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="9366d-112">알림 허브에 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="9366d-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="9366d-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="9366d-114">알림 허브 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="9366d-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="9366d-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="9366d-116">알림 허브에 대 한 PNS 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="9366d-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9366d-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="9366d-118">알림 허브 네임 스페이스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="9366d-120">알림 허브 네임 스페이스와 연결 된 권한 부여 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="9366d-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="9366d-122">알림 허브 네임 스페이스 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="9366d-123">새로운 AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9366d-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="9366d-124">알림 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="9366d-125">새로운 AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="9366d-126">권한 부여 규칙을 만들고 알림 허브에 규칙을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="9366d-127">새로운 AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="9366d-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="9366d-128">NotificationHub에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="9366d-129">새로운 AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9366d-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="9366d-130">알림 허브 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-131">새로운 AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="9366d-132">권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임 스페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-133">새로운 AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="9366d-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="9366d-134">네임 스페이스에 대 한 권한 부여 규칙 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="9366d-135">제거-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9366d-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="9366d-136">기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="9366d-137">제거-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="9366d-138">알림 허브에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="9366d-139">제거-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9366d-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="9366d-140">알림 허브 네임 스페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-141">제거-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="9366d-142">알림 허브 네임 스페이스에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="9366d-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="9366d-144">알림 허브에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="9366d-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="9366d-146">알림 허브에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="9366d-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9366d-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="9366d-148">알림 허브 네임 스페이스에 대 한 속성 값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="9366d-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9366d-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="9366d-150">알림 허브 네임 스페이스에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9366d-150">Sets authorization rules for a notification hub namespace.</span></span>

