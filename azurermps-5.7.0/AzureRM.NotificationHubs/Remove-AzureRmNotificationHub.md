---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: 2a5ec9ee9c24ed0612f43ffc03f80d5dfe9df464
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711131"
---
# <span data-ttu-id="65947-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="65947-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="65947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65947-102">SYNOPSIS</span></span>
<span data-ttu-id="65947-103">기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65947-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65947-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65947-105">DESCRIPTION</span></span>
<span data-ttu-id="65947-106">**AzureRmNotificationHub** cmdlet에서는 기존 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="65947-107">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65947-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="65947-108">플랫폼에는 iOS, Android, Windows Phone 8, Windows 스토어가 포함 되지만이에 국한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="65947-109">알림 허브는 개별 앱과 거의 동일 합니다. 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="65947-110">**제거-AzureRmNotificationHub** cmdlet을 사용 하 여 기존 알림 허브를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="65947-111">허브가 제거 된 후에는 더 이상 해당 허브를 사용 하 여 사용자에 게 푸시 알림을 보낼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="65947-112">예제의</span><span class="sxs-lookup"><span data-stu-id="65947-112">EXAMPLES</span></span>

### <span data-ttu-id="65947-113">예제 1: 알림 허브 제거</span><span class="sxs-lookup"><span data-stu-id="65947-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="65947-114">이 명령은 ContosoInternalHub 이라는 알림 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="65947-115">허브를 제거 하려면 허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="65947-116">변수</span><span class="sxs-lookup"><span data-stu-id="65947-116">PARAMETERS</span></span>

### <span data-ttu-id="65947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65947-117">-DefaultProfile</span></span>
<span data-ttu-id="65947-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65947-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65947-119">-Force</span><span class="sxs-lookup"><span data-stu-id="65947-119">-Force</span></span>
<span data-ttu-id="65947-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65947-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65947-121">-Namespace</span></span>
<span data-ttu-id="65947-122">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="65947-123">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="65947-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="65947-124">-NotificationHub</span></span>
<span data-ttu-id="65947-125">제거할 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-125">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="65947-126">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65947-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65947-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="65947-127">-ResourceGroup</span></span>
<span data-ttu-id="65947-128">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-128">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="65947-129">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="65947-130">-확인</span><span class="sxs-lookup"><span data-stu-id="65947-130">-Confirm</span></span>
<span data-ttu-id="65947-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65947-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65947-132">-WhatIf</span></span>
<span data-ttu-id="65947-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="65947-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65947-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65947-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65947-135">CommonParameters</span></span>
<span data-ttu-id="65947-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65947-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65947-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65947-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65947-138">입력</span><span class="sxs-lookup"><span data-stu-id="65947-138">INPUTS</span></span>

### <span data-ttu-id="65947-139">않아야</span><span class="sxs-lookup"><span data-stu-id="65947-139">None</span></span>
<span data-ttu-id="65947-140">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65947-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65947-141">출력</span><span class="sxs-lookup"><span data-stu-id="65947-141">OUTPUTS</span></span>

## <span data-ttu-id="65947-142">상속자</span><span class="sxs-lookup"><span data-stu-id="65947-142">NOTES</span></span>

## <span data-ttu-id="65947-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65947-143">RELATED LINKS</span></span>

[<span data-ttu-id="65947-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="65947-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="65947-145">새로운 AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="65947-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="65947-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="65947-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


