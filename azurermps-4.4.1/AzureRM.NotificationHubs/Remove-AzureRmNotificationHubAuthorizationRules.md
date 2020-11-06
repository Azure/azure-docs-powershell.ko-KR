---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: bb92344616c79db26b37bd9b18bdff7973946c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529246"
---
# <span data-ttu-id="c1bd8-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c1bd8-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="c1bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bd8-103">알림 허브에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1bd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1bd8-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bd8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="c1bd8-106">**AzureRmNotificationHubAuthorizationRules** cmdlet은 알림 허브에서 SAS (공유 액세스 서명) 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="c1bd8-107">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="c1bd8-108">사용 권한 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="c1bd8-109">듣기</span><span class="sxs-lookup"><span data-stu-id="c1bd8-109">Listen</span></span>
- <span data-ttu-id="c1bd8-110">보내기</span><span class="sxs-lookup"><span data-stu-id="c1bd8-110">Send</span></span>
- <span data-ttu-id="c1bd8-111">관리자</span><span class="sxs-lookup"><span data-stu-id="c1bd8-111">Manage</span></span>

<span data-ttu-id="c1bd8-112">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="c1bd8-113">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 사용 권한에 대 한 URI로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="c1bd8-114">권한 부여 규칙을 제거 하면 해당 사용자 권한도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="c1bd8-115">예제의</span><span class="sxs-lookup"><span data-stu-id="c1bd8-115">EXAMPLES</span></span>

### <span data-ttu-id="c1bd8-116">예제 1: 알림 허브에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="c1bd8-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c1bd8-117">이 명령은 ContosoExternalHub 이라는 알림 허브에서 ListenRule 이라는 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="c1bd8-118">이 명령을 실행할 때는 네임 스페이스와 허브가 할당 된 리소스 그룹을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="c1bd8-119">변수</span><span class="sxs-lookup"><span data-stu-id="c1bd8-119">PARAMETERS</span></span>

### <span data-ttu-id="c1bd8-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c1bd8-120">-AuthorizationRule</span></span>
<span data-ttu-id="c1bd8-121">이 cmdlet이 제거 하는 SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1bd8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c1bd8-122">-Force</span></span>
<span data-ttu-id="c1bd8-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c1bd8-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c1bd8-124">-Namespace</span></span>
<span data-ttu-id="c1bd8-125">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-125">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c1bd8-126">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c1bd8-127">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c1bd8-127">-NotificationHub</span></span>
<span data-ttu-id="c1bd8-128">권한 부여 규칙이 할당 되는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-128">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="c1bd8-129">알림 허브는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-129">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="c1bd8-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1bd8-130">-ResourceGroup</span></span>
<span data-ttu-id="c1bd8-131">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-131">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c1bd8-132">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c1bd8-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c1bd8-133">-Confirm</span></span>
<span data-ttu-id="c1bd8-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bd8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1bd8-135">-WhatIf</span></span>
<span data-ttu-id="c1bd8-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1bd8-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bd8-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bd8-138">-DefaultProfile</span></span>
<span data-ttu-id="c1bd8-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1bd8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bd8-140">CommonParameters</span></span>
<span data-ttu-id="c1bd8-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1bd8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bd8-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1bd8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bd8-143">입력</span><span class="sxs-lookup"><span data-stu-id="c1bd8-143">INPUTS</span></span>

## <span data-ttu-id="c1bd8-144">출력</span><span class="sxs-lookup"><span data-stu-id="c1bd8-144">OUTPUTS</span></span>

## <span data-ttu-id="c1bd8-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c1bd8-145">NOTES</span></span>

## <span data-ttu-id="c1bd8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1bd8-146">RELATED LINKS</span></span>

[<span data-ttu-id="c1bd8-147">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c1bd8-147">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="c1bd8-148">새로운 AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c1bd8-148">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="c1bd8-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c1bd8-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


