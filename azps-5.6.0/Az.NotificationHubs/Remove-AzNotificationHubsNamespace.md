---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: a1e5a8b33ab9df4e48495d00b6a27e105088f4fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951136"
---
# <span data-ttu-id="90232-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90232-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="90232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90232-102">SYNOPSIS</span></span>
<span data-ttu-id="90232-103">알림 허브 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="90232-104">구문</span><span class="sxs-lookup"><span data-stu-id="90232-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90232-105">설명</span><span class="sxs-lookup"><span data-stu-id="90232-105">DESCRIPTION</span></span>
<span data-ttu-id="90232-106">**Remove-AzNotificationHubsNamespace** cmdlet은 배포에서 알림 허브 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="90232-107">네임스페이스는 알림 허브를 구성하고 관리하는 데 도움이 되는 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="90232-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="90232-108">**Remove-AzNotificationHubsNamespace** cmdlet은 배포에서 알림 허브 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="90232-109">이 cmdlet을 실행하면 지정된 네임스페이스가 해당 네임스페이스와 연결된 모든 알림 허브와 함께 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="90232-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="90232-110">예제</span><span class="sxs-lookup"><span data-stu-id="90232-110">EXAMPLES</span></span>

### <span data-ttu-id="90232-111">예제 1: 알림 허브 네임스페이스 제거</span><span class="sxs-lookup"><span data-stu-id="90232-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="90232-112">이 명령은 ContosoNamespace라는 네임스페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="90232-113">네임스페이스가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="90232-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90232-114">PARAMETERS</span></span>

### <span data-ttu-id="90232-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90232-115">-DefaultProfile</span></span>
<span data-ttu-id="90232-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90232-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90232-117">-Force</span><span class="sxs-lookup"><span data-stu-id="90232-117">-Force</span></span>
<span data-ttu-id="90232-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90232-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="90232-119">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="90232-119">-Namespace</span></span>
<span data-ttu-id="90232-120">이 cmdlet에서 제거하는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="90232-121">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="90232-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90232-122">-ResourceGroup</span></span>
<span data-ttu-id="90232-123">네임스페이스가 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="90232-124">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="90232-125">-확인</span><span class="sxs-lookup"><span data-stu-id="90232-125">-Confirm</span></span>
<span data-ttu-id="90232-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90232-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90232-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90232-127">-WhatIf</span></span>
<span data-ttu-id="90232-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90232-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90232-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90232-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90232-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90232-130">CommonParameters</span></span>
<span data-ttu-id="90232-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90232-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90232-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90232-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90232-133">입력</span><span class="sxs-lookup"><span data-stu-id="90232-133">INPUTS</span></span>

### <span data-ttu-id="90232-134">System.String</span><span class="sxs-lookup"><span data-stu-id="90232-134">System.String</span></span>

## <span data-ttu-id="90232-135">출력</span><span class="sxs-lookup"><span data-stu-id="90232-135">OUTPUTS</span></span>

### <span data-ttu-id="90232-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="90232-136">System.Void</span></span>

## <span data-ttu-id="90232-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90232-137">NOTES</span></span>

## <span data-ttu-id="90232-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90232-138">RELATED LINKS</span></span>

[<span data-ttu-id="90232-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90232-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="90232-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90232-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="90232-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="90232-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


