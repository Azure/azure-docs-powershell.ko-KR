---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536747"
---
# <span data-ttu-id="43abf-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="43abf-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="43abf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43abf-102">SYNOPSIS</span></span>
<span data-ttu-id="43abf-103">알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43abf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43abf-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43abf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="43abf-105">DESCRIPTION</span></span>
<span data-ttu-id="43abf-106">**AzureRmNotificationHub** cmdlet은 지정 된 네임 스페이스의 notification hubs에 대 한 정보를 가져오고 지정 된 리소스 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="43abf-107">예를 들어 네임 스페이스 ContosoNamespace의 모든 알림 허브에 대 한 정보를 가져오고 ContosoNotificationsGroup 리소스 그룹에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="43abf-108">또는 *Notificationhub* 매개 변수를 사용 하 여 반환 된 데이터를 특정 알림 허브에 대 한 정보로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="43abf-109">알림 허브는 해당 클라이언트에서 사용 하는 iOS, Android, Windows Phone 8, Windows 스토어 등의 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="43abf-110">이러한 허브는 개별 앱과 거의 동일 하며 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="43abf-111">이 cmdlet은 허브 자체에 대 한 정보만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="43abf-112">AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys 및 Get-AzureRmNotificationHubPNSCredentials 등의 다른 cmdlet은 허브의 권한 부여 규칙, 연결 문자열 및 플랫폼 알림 서비스 자격 증명에 대 한 정보를 가져오기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="43abf-113">예제의</span><span class="sxs-lookup"><span data-stu-id="43abf-113">EXAMPLES</span></span>

### <span data-ttu-id="43abf-114">예제 1: 특정 네임 스페이스의 모든 알림 허브에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="43abf-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="43abf-115">이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 ContosoNamespace 이라는 네임 스페이스에 있는 모든 알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="43abf-116">변수</span><span class="sxs-lookup"><span data-stu-id="43abf-116">PARAMETERS</span></span>

### <span data-ttu-id="43abf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43abf-117">-DefaultProfile</span></span>
<span data-ttu-id="43abf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43abf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43abf-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="43abf-119">-Namespace</span></span>
<span data-ttu-id="43abf-120">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="43abf-121">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43abf-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="43abf-122">-NotificationHub</span></span>
<span data-ttu-id="43abf-123">이 cmdlet이 가져오는 알림 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="43abf-124">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43abf-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43abf-125">-ResourceGroup</span></span>
<span data-ttu-id="43abf-126">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="43abf-127">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43abf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43abf-128">CommonParameters</span></span>
<span data-ttu-id="43abf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43abf-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43abf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43abf-131">입력</span><span class="sxs-lookup"><span data-stu-id="43abf-131">INPUTS</span></span>

### <span data-ttu-id="43abf-132">않아야</span><span class="sxs-lookup"><span data-stu-id="43abf-132">None</span></span>
<span data-ttu-id="43abf-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43abf-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43abf-134">출력</span><span class="sxs-lookup"><span data-stu-id="43abf-134">OUTPUTS</span></span>

### <span data-ttu-id="43abf-135">NotificationHubAttributes의 목록 ' 1 [Microsoft. h t e.]</span><span class="sxs-lookup"><span data-stu-id="43abf-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="43abf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="43abf-136">NOTES</span></span>

## <span data-ttu-id="43abf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43abf-137">RELATED LINKS</span></span>

[<span data-ttu-id="43abf-138">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="43abf-138">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="43abf-139">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="43abf-139">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="43abf-140">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="43abf-140">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="43abf-141">새로운 AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="43abf-141">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="43abf-142">제거-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="43abf-142">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="43abf-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="43abf-143">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


