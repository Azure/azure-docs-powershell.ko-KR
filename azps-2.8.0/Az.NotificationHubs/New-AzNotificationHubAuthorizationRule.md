---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 436ed6aaa720074be2014d9c736ab0636a09869f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872001"
---
# <span data-ttu-id="081b1-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="081b1-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="081b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="081b1-102">SYNOPSIS</span></span>
<span data-ttu-id="081b1-103">권한 부여 규칙을 만들고 알림 허브에 규칙을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="081b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="081b1-104">SYNTAX</span></span>

### <span data-ttu-id="081b1-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="081b1-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="081b1-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="081b1-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="081b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="081b1-107">DESCRIPTION</span></span>
<span data-ttu-id="081b1-108">**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브 Sa (공유 액세스 서명) 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="081b1-109">인증 규칙은 알림 허브에 대 한 액세스를 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="081b1-110">이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="081b1-111">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="081b1-112">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 권한의 URI로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="081b1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="081b1-113">EXAMPLES</span></span>

### <span data-ttu-id="081b1-114">예제 1: 알림 허브 권한 부여 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="081b1-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="081b1-115">이 명령은 새 권한 부여 규칙을 만들어 ContosoInternalHub 이라는 알림 허브에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="081b1-116">이 허브는 ContosoNamespace 네임 스페이스에 있으며 ContosoNotificationsGroup 리소스 그룹에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="081b1-117">규칙 이름을 포함 하 여 해당 규칙에 대 한 모든 구성 정보는 C:\Configuration\ExternalAccessRule.js입력 파일에서 가져온 것을 참고 하세요.</span><span class="sxs-lookup"><span data-stu-id="081b1-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="081b1-118">변수</span><span class="sxs-lookup"><span data-stu-id="081b1-118">PARAMETERS</span></span>

### <span data-ttu-id="081b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081b1-119">-DefaultProfile</span></span>
<span data-ttu-id="081b1-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="081b1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="081b1-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="081b1-121">-InputFile</span></span>
<span data-ttu-id="081b1-122">이 cmdlet이 만드는 권한 부여 규칙에 대 한 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="081b1-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="081b1-123">-Namespace</span></span>
<span data-ttu-id="081b1-124">권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="081b1-125">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="081b1-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="081b1-126">-NotificationHub</span></span>
<span data-ttu-id="081b1-127">권한 부여 규칙이 할당 될 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="081b1-128">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="081b1-129">기존 알림 허브의 이름을 지정 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="081b1-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="081b1-130">**AzNotificationHubAuthorizationRule** cmdlet은 새 알림 허브를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="081b1-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="081b1-131">-ResourceGroup</span></span>
<span data-ttu-id="081b1-132">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="081b1-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="081b1-133">-SASRule</span></span>
<span data-ttu-id="081b1-134">새 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="081b1-135">-확인</span><span class="sxs-lookup"><span data-stu-id="081b1-135">-Confirm</span></span>
<span data-ttu-id="081b1-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="081b1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="081b1-137">-WhatIf</span></span>
<span data-ttu-id="081b1-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="081b1-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="081b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081b1-140">CommonParameters</span></span>
<span data-ttu-id="081b1-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="081b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081b1-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081b1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081b1-143">입력</span><span class="sxs-lookup"><span data-stu-id="081b1-143">INPUTS</span></span>

### <span data-ttu-id="081b1-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="081b1-144">System.String</span></span>

## <span data-ttu-id="081b1-145">출력</span><span class="sxs-lookup"><span data-stu-id="081b1-145">OUTPUTS</span></span>

### <span data-ttu-id="081b1-146">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="081b1-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="081b1-147">상속자</span><span class="sxs-lookup"><span data-stu-id="081b1-147">NOTES</span></span>

## <span data-ttu-id="081b1-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="081b1-148">RELATED LINKS</span></span>

[<span data-ttu-id="081b1-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="081b1-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="081b1-150">제거-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="081b1-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="081b1-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="081b1-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


