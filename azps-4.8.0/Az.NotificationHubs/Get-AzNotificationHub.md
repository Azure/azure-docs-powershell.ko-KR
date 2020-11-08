---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214307"
---
# <span data-ttu-id="2321e-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2321e-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="2321e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2321e-102">SYNOPSIS</span></span>
<span data-ttu-id="2321e-103">알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="2321e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2321e-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2321e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2321e-105">DESCRIPTION</span></span>
<span data-ttu-id="2321e-106">**AzNotificationHub** cmdlet은 지정 된 네임 스페이스의 notification hubs에 대 한 정보를 가져오고 지정 된 리소스 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="2321e-107">예를 들어 네임 스페이스 ContosoNamespace의 모든 알림 허브에 대 한 정보를 가져오고 ContosoNotificationsGroup 리소스 그룹에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="2321e-108">또는 *Notificationhub* 매개 변수를 사용 하 여 반환 된 데이터를 특정 알림 허브에 대 한 정보로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="2321e-109">알림 허브는 해당 클라이언트에서 사용 하는 iOS, Android, Windows Phone 8, Windows 스토어 등의 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="2321e-110">이러한 허브는 개별 앱과 거의 동일 하며 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="2321e-111">이 cmdlet은 허브 자체에 대 한 정보만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="2321e-112">AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys 및 Get-AzNotificationHubPNSCredentials 등의 다른 cmdlet은 허브의 권한 부여 규칙, 연결 문자열 및 플랫폼 알림 서비스 자격 증명에 대 한 정보를 가져오기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="2321e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2321e-113">EXAMPLES</span></span>

### <span data-ttu-id="2321e-114">예제 1: 특정 네임 스페이스의 모든 알림 허브에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="2321e-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="2321e-115">이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당 된 ContosoNamespace 이라는 네임 스페이스에 있는 모든 알림 허브에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="2321e-116">변수</span><span class="sxs-lookup"><span data-stu-id="2321e-116">PARAMETERS</span></span>

### <span data-ttu-id="2321e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2321e-117">-DefaultProfile</span></span>
<span data-ttu-id="2321e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2321e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2321e-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2321e-119">-Namespace</span></span>
<span data-ttu-id="2321e-120">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="2321e-121">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="2321e-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2321e-122">-NotificationHub</span></span>
<span data-ttu-id="2321e-123">이 cmdlet이 가져오는 알림 허브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="2321e-124">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2321e-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2321e-125">-ResourceGroup</span></span>
<span data-ttu-id="2321e-126">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="2321e-127">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="2321e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2321e-128">CommonParameters</span></span>
<span data-ttu-id="2321e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2321e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2321e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2321e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2321e-131">입력</span><span class="sxs-lookup"><span data-stu-id="2321e-131">INPUTS</span></span>

### <span data-ttu-id="2321e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2321e-132">System.String</span></span>

## <span data-ttu-id="2321e-133">출력</span><span class="sxs-lookup"><span data-stu-id="2321e-133">OUTPUTS</span></span>

### <span data-ttu-id="2321e-134">Microsoft. Azure. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2321e-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="2321e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2321e-135">NOTES</span></span>

## <span data-ttu-id="2321e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2321e-136">RELATED LINKS</span></span>

[<span data-ttu-id="2321e-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2321e-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="2321e-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="2321e-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="2321e-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="2321e-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="2321e-140">새로운 AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2321e-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="2321e-141">제거-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2321e-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="2321e-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="2321e-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


