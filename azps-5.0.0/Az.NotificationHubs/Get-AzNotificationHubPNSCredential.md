---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 282e8092050b5859809c8dad71c4da1ee86c779d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216056"
---
# <span data-ttu-id="566b1-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="566b1-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="566b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="566b1-102">SYNOPSIS</span></span>
<span data-ttu-id="566b1-103">알림 허브에 대 한 PNS 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="566b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="566b1-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="566b1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="566b1-105">DESCRIPTION</span></span>
<span data-ttu-id="566b1-106">**AzNotificationHubPNSCredential** cmdlet은 알림 허브에 대 한 PNS (플랫폼 알림 서비스) 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="566b1-107">각 알림 허브에는 단일 PNS 자격 증명 집합이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="566b1-108">이러한 자격 증명은 개별 푸시 알림 서비스 (예: 제한 되지 않음)에 적용 됩니다. iOS 푸시 알림 서비스, Android 푸시 알림 서비스, Windows Phone 8입니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="566b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="566b1-109">EXAMPLES</span></span>

### <span data-ttu-id="566b1-110">예제 1: 특정 알림 허브에 대 한 PNS 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="566b1-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="566b1-111">이 명령은 ContosoNotificationsGroup 이라는 리소스 그룹에 속하는 ContosoInternalHub 라는 알림 허브에 대 한 PNS 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="566b1-112">변수</span><span class="sxs-lookup"><span data-stu-id="566b1-112">PARAMETERS</span></span>

### <span data-ttu-id="566b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566b1-113">-DefaultProfile</span></span>
<span data-ttu-id="566b1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="566b1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="566b1-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="566b1-115">-Namespace</span></span>
<span data-ttu-id="566b1-116">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="566b1-117">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="566b1-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="566b1-118">-NotificationHub</span></span>
<span data-ttu-id="566b1-119">PNS 자격 증명이 할당 된 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="566b1-120">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="566b1-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="566b1-121">-ResourceGroup</span></span>
<span data-ttu-id="566b1-122">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="566b1-123">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="566b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566b1-124">CommonParameters</span></span>
<span data-ttu-id="566b1-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="566b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566b1-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="566b1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566b1-127">입력</span><span class="sxs-lookup"><span data-stu-id="566b1-127">INPUTS</span></span>

### <span data-ttu-id="566b1-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="566b1-128">System.String</span></span>

## <span data-ttu-id="566b1-129">출력</span><span class="sxs-lookup"><span data-stu-id="566b1-129">OUTPUTS</span></span>

### <span data-ttu-id="566b1-130">Microsoft. Azure. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="566b1-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="566b1-131">상속자</span><span class="sxs-lookup"><span data-stu-id="566b1-131">NOTES</span></span>

## <span data-ttu-id="566b1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="566b1-132">RELATED LINKS</span></span>

[<span data-ttu-id="566b1-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="566b1-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


