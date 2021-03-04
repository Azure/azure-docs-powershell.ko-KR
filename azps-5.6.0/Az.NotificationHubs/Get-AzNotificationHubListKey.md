---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: dce2736329fe4cfac6406a6646de7388869d20e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951323"
---
# <span data-ttu-id="4286d-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="4286d-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="4286d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4286d-102">SYNOPSIS</span></span>
<span data-ttu-id="4286d-103">알림 허브 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="4286d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4286d-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4286d-105">설명</span><span class="sxs-lookup"><span data-stu-id="4286d-105">DESCRIPTION</span></span>
<span data-ttu-id="4286d-106">**Get-AzNotificationHubListKey** cmdlet은 SAS(공유 액세스 서명) 권한 부여 규칙의 기본 및 보조 연결 문자열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="4286d-107">권한 부여 규칙은 허브에 대한 사용자 권한을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="4286d-108">각 규칙에는 기본 및 보조 연결 문자열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="4286d-109">이러한 연결 문자열(URIS)은 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="4286d-110">사용자를 리소스로 지 습니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-110">Point users to a resource.</span></span>
- <span data-ttu-id="4286d-111">쿼리 매개 변수를 포함하는 토큰을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="4286d-112">이러한 매개 변수 중 하나인 서명은 사용자를 인증하고 지정된 액세스 수준을 제공하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="4286d-113">예제</span><span class="sxs-lookup"><span data-stu-id="4286d-113">EXAMPLES</span></span>

### <span data-ttu-id="4286d-114">예제 1: 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="4286d-115">이 명령은 ContosoInternalHub 알림 허브에 할당된 규칙인 ListenRule 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="4286d-116">명령에는 허브 네임스페이스 및 리소스 그룹이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="4286d-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4286d-117">PARAMETERS</span></span>

### <span data-ttu-id="4286d-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4286d-118">-AuthorizationRule</span></span>
<span data-ttu-id="4286d-119">SAS(공유 액세스 서명) 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="4286d-120">이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="4286d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4286d-121">-DefaultProfile</span></span>
<span data-ttu-id="4286d-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4286d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4286d-123">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="4286d-123">-Namespace</span></span>
<span data-ttu-id="4286d-124">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4286d-125">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4286d-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4286d-126">-NotificationHub</span></span>
<span data-ttu-id="4286d-127">이 cmdlet에서 권한 부여 규칙을 할당하는 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="4286d-128">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="4286d-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4286d-129">-ResourceGroup</span></span>
<span data-ttu-id="4286d-130">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4286d-131">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4286d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4286d-132">CommonParameters</span></span>
<span data-ttu-id="4286d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4286d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4286d-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4286d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4286d-135">입력</span><span class="sxs-lookup"><span data-stu-id="4286d-135">INPUTS</span></span>

### <span data-ttu-id="4286d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4286d-136">System.String</span></span>

## <span data-ttu-id="4286d-137">출력</span><span class="sxs-lookup"><span data-stu-id="4286d-137">OUTPUTS</span></span>

### <span data-ttu-id="4286d-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="4286d-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="4286d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4286d-139">NOTES</span></span>

## <span data-ttu-id="4286d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4286d-140">RELATED LINKS</span></span>

[<span data-ttu-id="4286d-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4286d-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)


