---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 9ae94e039d91f8f21015fb28b726ef5bacfb4ae4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528896"
---
# <span data-ttu-id="417c4-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="417c4-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="417c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417c4-102">SYNOPSIS</span></span>
<span data-ttu-id="417c4-103">알림 허브에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="417c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="417c4-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="417c4-105">DESCRIPTION</span></span>
<span data-ttu-id="417c4-106">**AzureRmNotificationHubAuthorizationRules** cmdlet은 알림 허브에서 SAS (공유 액세스 서명) 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="417c4-107">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="417c4-108">사용 권한 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="417c4-109">듣기</span><span class="sxs-lookup"><span data-stu-id="417c4-109">Listen</span></span>
- <span data-ttu-id="417c4-110">보내기</span><span class="sxs-lookup"><span data-stu-id="417c4-110">Send</span></span>
- <span data-ttu-id="417c4-111">관리자</span><span class="sxs-lookup"><span data-stu-id="417c4-111">Manage</span></span>

<span data-ttu-id="417c4-112">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="417c4-113">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="417c4-114">권한 부여 규칙을 제거 하면 해당 사용자 권한도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="417c4-115">예제의</span><span class="sxs-lookup"><span data-stu-id="417c4-115">EXAMPLES</span></span>

### <span data-ttu-id="417c4-116">예제 1: 알림 허브에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="417c4-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="417c4-117">이 명령은 ContosoExternalHub 이라는 알림 허브에서 ListenRule 이라는 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="417c4-118">이 명령을 실행할 때는 네임 스페이스와 허브가 할당 된 리소스 그룹을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="417c4-119">변수</span><span class="sxs-lookup"><span data-stu-id="417c4-119">PARAMETERS</span></span>

### <span data-ttu-id="417c4-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="417c4-120">-AuthorizationRule</span></span>
<span data-ttu-id="417c4-121">이 cmdlet이 제거 하는 SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417c4-122">-DefaultProfile</span></span>
<span data-ttu-id="417c4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="417c4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="417c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="417c4-124">-Force</span></span>
<span data-ttu-id="417c4-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="417c4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="417c4-126">-Namespace</span></span>
<span data-ttu-id="417c4-127">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-127">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="417c4-128">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="417c4-129">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="417c4-129">-NotificationHub</span></span>
<span data-ttu-id="417c4-130">권한 부여 규칙이 할당 되는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-130">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="417c4-131">알림 허브는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-131">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="417c4-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="417c4-132">-ResourceGroup</span></span>
<span data-ttu-id="417c4-133">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-133">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="417c4-134">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="417c4-135">-확인</span><span class="sxs-lookup"><span data-stu-id="417c4-135">-Confirm</span></span>
<span data-ttu-id="417c4-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="417c4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417c4-137">-WhatIf</span></span>
<span data-ttu-id="417c4-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="417c4-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="417c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417c4-140">CommonParameters</span></span>
<span data-ttu-id="417c4-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417c4-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417c4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417c4-143">입력</span><span class="sxs-lookup"><span data-stu-id="417c4-143">INPUTS</span></span>

### <span data-ttu-id="417c4-144">않아야</span><span class="sxs-lookup"><span data-stu-id="417c4-144">None</span></span>
<span data-ttu-id="417c4-145">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="417c4-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="417c4-146">출력</span><span class="sxs-lookup"><span data-stu-id="417c4-146">OUTPUTS</span></span>

## <span data-ttu-id="417c4-147">상속자</span><span class="sxs-lookup"><span data-stu-id="417c4-147">NOTES</span></span>

## <span data-ttu-id="417c4-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="417c4-148">RELATED LINKS</span></span>

[<span data-ttu-id="417c4-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="417c4-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="417c4-150">새로운 AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="417c4-150">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="417c4-151">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="417c4-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


