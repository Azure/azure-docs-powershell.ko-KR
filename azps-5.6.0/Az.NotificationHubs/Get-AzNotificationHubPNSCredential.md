---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 44da06fa8237880be154100d05eeee60cd7db7b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951312"
---
# <span data-ttu-id="ef1da-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="ef1da-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="ef1da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef1da-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1da-103">알림 허브에 대한 PNS 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="ef1da-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef1da-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef1da-105">설명</span><span class="sxs-lookup"><span data-stu-id="ef1da-105">DESCRIPTION</span></span>
<span data-ttu-id="ef1da-106">**Get-AzNotificationHubPNSCredential** cmdlet은 알림 허브에 대한 PNS(플랫폼 알림 서비스) 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="ef1da-107">각 알림 허브에는 단일 PNS 자격 증명 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="ef1da-108">이러한 자격 증명은 개별 푸시 알림 서비스에 적용되지만 이에 국한되지는 않습니다. iOS 푸시 알림 서비스, Android 푸시 알림 서비스 및 Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ef1da-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="ef1da-109">예제</span><span class="sxs-lookup"><span data-stu-id="ef1da-109">EXAMPLES</span></span>

### <span data-ttu-id="ef1da-110">예제 1: 특정 알림 허브에 대한 PNS 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="ef1da-111">이 명령은 ContosoNotificationsGroup이라는 리소스 그룹에 속하는 ContosoInternalHub라는 알림 허브에 대한 PNS 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="ef1da-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef1da-112">PARAMETERS</span></span>

### <span data-ttu-id="ef1da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1da-113">-DefaultProfile</span></span>
<span data-ttu-id="ef1da-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef1da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef1da-115">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ef1da-115">-Namespace</span></span>
<span data-ttu-id="ef1da-116">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ef1da-117">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ef1da-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ef1da-118">-NotificationHub</span></span>
<span data-ttu-id="ef1da-119">PNS 자격 증명이 할당된 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="ef1da-120">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="ef1da-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef1da-121">-ResourceGroup</span></span>
<span data-ttu-id="ef1da-122">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ef1da-123">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ef1da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1da-124">CommonParameters</span></span>
<span data-ttu-id="ef1da-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef1da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1da-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ef1da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1da-127">입력</span><span class="sxs-lookup"><span data-stu-id="ef1da-127">INPUTS</span></span>

### <span data-ttu-id="ef1da-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ef1da-128">System.String</span></span>

## <span data-ttu-id="ef1da-129">출력</span><span class="sxs-lookup"><span data-stu-id="ef1da-129">OUTPUTS</span></span>

### <span data-ttu-id="ef1da-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="ef1da-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="ef1da-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef1da-131">NOTES</span></span>

## <span data-ttu-id="ef1da-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef1da-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef1da-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ef1da-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


