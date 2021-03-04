---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74ad4f80a25250129d050ed3a2769dca6f776376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951275"
---
# <span data-ttu-id="ecffe-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecffe-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="ecffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecffe-102">SYNOPSIS</span></span>
<span data-ttu-id="ecffe-103">권한 부여 규칙을 만들고 알림 허브에 규칙을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="ecffe-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecffe-104">SYNTAX</span></span>

### <span data-ttu-id="ecffe-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecffe-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecffe-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecffe-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecffe-107">설명</span><span class="sxs-lookup"><span data-stu-id="ecffe-107">DESCRIPTION</span></span>
<span data-ttu-id="ecffe-108">**New-AzNotificationHubAuthorizationRule** cmdlet은 SAS(알림 허브 공유 액세스 서명) 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="ecffe-109">권한 부여 규칙은 알림 허브에 대한 액세스를 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="ecffe-110">이는 다른 사용 권한 수준에 따라 URIS로 링크를 만들어서 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ecffe-111">클라이언트는 적절한 사용 권한 수준에 따라 이러한 URIS 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ecffe-112">예를 들어 수신 권한을 부여한 클라이언트는 해당 사용 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="ecffe-113">예제</span><span class="sxs-lookup"><span data-stu-id="ecffe-113">EXAMPLES</span></span>

### <span data-ttu-id="ecffe-114">예제 1: 알림 허브 권한 부여 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ecffe-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="ecffe-115">이 명령은 새 권한 부여 규칙을 만들고 ContosoInternalHub라는 알림 허브에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="ecffe-116">이 허브는 ContosoNamespace 네임스페이스에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="ecffe-117">규칙 이름을 포함하여 규칙에 대한 모든 구성 정보는 에 있는 입력 파일에서 C:\Configuration\ExternalAccessRule.js있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="ecffe-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecffe-118">PARAMETERS</span></span>

### <span data-ttu-id="ecffe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecffe-119">-DefaultProfile</span></span>
<span data-ttu-id="ecffe-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ecffe-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecffe-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ecffe-121">-InputFile</span></span>
<span data-ttu-id="ecffe-122">이 cmdlet이 만드는 권한 부여 규칙에 대한 입력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecffe-123">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="ecffe-123">-Namespace</span></span>
<span data-ttu-id="ecffe-124">권한 부여 규칙이 할당되는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ecffe-125">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ecffe-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ecffe-126">-NotificationHub</span></span>
<span data-ttu-id="ecffe-127">권한 부여 규칙이 할당될 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="ecffe-128">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="ecffe-129">기존 알림 허브의 이름을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="ecffe-130">**New-AzNotificationHubAuthorizationRule** cmdlet은 새 알림 허브를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="ecffe-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ecffe-131">-ResourceGroup</span></span>
<span data-ttu-id="ecffe-132">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="ecffe-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="ecffe-133">-SASRule</span></span>
<span data-ttu-id="ecffe-134">새 규칙에 대한 구성 정보가 포함된 **SharedAccessAuthorizationRuleAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecffe-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ecffe-135">-Confirm</span></span>
<span data-ttu-id="ecffe-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecffe-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecffe-137">-WhatIf</span></span>
<span data-ttu-id="ecffe-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecffe-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecffe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecffe-140">CommonParameters</span></span>
<span data-ttu-id="ecffe-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecffe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecffe-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecffe-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecffe-143">입력</span><span class="sxs-lookup"><span data-stu-id="ecffe-143">INPUTS</span></span>

### <span data-ttu-id="ecffe-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ecffe-144">System.String</span></span>

## <span data-ttu-id="ecffe-145">출력</span><span class="sxs-lookup"><span data-stu-id="ecffe-145">OUTPUTS</span></span>

### <span data-ttu-id="ecffe-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ecffe-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ecffe-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecffe-147">NOTES</span></span>

## <span data-ttu-id="ecffe-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecffe-148">RELATED LINKS</span></span>

[<span data-ttu-id="ecffe-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecffe-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ecffe-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecffe-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ecffe-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecffe-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


