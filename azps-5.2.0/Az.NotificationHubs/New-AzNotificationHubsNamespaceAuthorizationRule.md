---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350654"
---
# <span data-ttu-id="7cc5c-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7cc5c-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="7cc5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc5c-103">권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임스페이스에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="7cc5c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cc5c-104">SYNTAX</span></span>

### <span data-ttu-id="7cc5c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc5c-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cc5c-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc5c-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc5c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7cc5c-107">DESCRIPTION</span></span>
<span data-ttu-id="7cc5c-108">**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 SAS(공유 액세스 서명) 권한 부여 규칙을 만들고 알림 허브 네임스페이스에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="7cc5c-109">권한 부여 규칙은 네임스페이스 및 해당 네임스페이스에 포함된 알림 허브에 대한 사용자 권한을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="7cc5c-110">이 cmdlet은 새 권한 부여 규칙을 만들고 네임스페이스에 할당하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="7cc5c-111">**SharedAccessAuthorizationRuleAttributes** 개체의 인스턴스를 만든 다음 새 규칙에서 소유하려는 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="7cc5c-112">.NET Framework를 사용하여 이 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="7cc5c-113">그런 다음 *SASRule* 매개 변수를 사용하여 해당 속성 값을 새 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="7cc5c-114">또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 사용하여 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="7cc5c-115">JSON 파일은 {과 유사한 구문을 사용하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="7cc5c-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="7cc5c-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7cc5c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="7cc5c-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7cc5c-118">"Rights": \[</span><span class="sxs-lookup"><span data-stu-id="7cc5c-118">"Rights": \[</span></span>  
        <span data-ttu-id="7cc5c-119">"수신",</span><span class="sxs-lookup"><span data-stu-id="7cc5c-119">"Listen",</span></span>  
        <span data-ttu-id="7cc5c-120">"보내기"</span><span class="sxs-lookup"><span data-stu-id="7cc5c-120">"Send"</span></span>  
    \]  
<span data-ttu-id="7cc5c-121">} **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet과 함께 사용하는 경우 이전 JSON 샘플은 사용자에게 네임스페이스에 대한 수신 및 보내기 권한을 부여하는 ContosoAuthorizationRule이라는 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="7cc5c-122">인증에 사용되는 *PrimaryKey는* 다음 Windows PowerShell 명령을 사용하여 임의로 생성될 수 있습니다. \[ Convert \] ::ToBase64String((1..32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="7cc5c-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="7cc5c-123">예제</span><span class="sxs-lookup"><span data-stu-id="7cc5c-123">EXAMPLES</span></span>

### <span data-ttu-id="7cc5c-124">예제 1: 권한 부여 규칙 만들기 및 네임스페이스에 할당</span><span class="sxs-lookup"><span data-stu-id="7cc5c-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="7cc5c-125">이 명령은 권한 부여 규칙을 만들고 ContosoNamespace 네임스페이스에 해당 규칙을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="7cc5c-126">이 규칙을 만들 때 네임스페이스가 할당된 적절한 네임스페이스 및 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="7cc5c-127">그러나 규칙 자체에 대한 정보를 지정할 필요는 없습니다. 규칙 정보는 규칙이 설정되어 있는 입력 파일에서 C:\Configuration\NamespaceAuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="7cc5c-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cc5c-128">PARAMETERS</span></span>

### <span data-ttu-id="7cc5c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc5c-129">-DefaultProfile</span></span>
<span data-ttu-id="7cc5c-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7cc5c-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc5c-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7cc5c-131">-InputFile</span></span>
<span data-ttu-id="7cc5c-132">새 권한 부여 규칙에 대한 구성 정보를 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc5c-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7cc5c-133">-Namespace</span></span>
<span data-ttu-id="7cc5c-134">권한 부여 규칙이 할당될 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="7cc5c-135">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="7cc5c-136">새 규칙은 기존 네임스페이스에 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="7cc5c-137">**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 새 네임스페이스를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="7cc5c-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7cc5c-138">-ResourceGroup</span></span>
<span data-ttu-id="7cc5c-139">네임스페이스가 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="7cc5c-140">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="7cc5c-141">기존 리소스 그룹을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-141">You must use an existing resource group.</span></span>
<span data-ttu-id="7cc5c-142">이 cmdlet은 새 리소스 그룹을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="7cc5c-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7cc5c-143">-SASRule</span></span>
<span data-ttu-id="7cc5c-144">새 규칙에 대한 구성 정보를 포함하는 **SharedAccessAuthorizationRuleAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc5c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cc5c-145">-Confirm</span></span>
<span data-ttu-id="7cc5c-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc5c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc5c-147">-WhatIf</span></span>
<span data-ttu-id="7cc5c-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7cc5c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cc5c-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc5c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc5c-150">CommonParameters</span></span>
<span data-ttu-id="7cc5c-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc5c-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc5c-153">입력</span><span class="sxs-lookup"><span data-stu-id="7cc5c-153">INPUTS</span></span>

### <span data-ttu-id="7cc5c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="7cc5c-154">System.String</span></span>

## <span data-ttu-id="7cc5c-155">출력</span><span class="sxs-lookup"><span data-stu-id="7cc5c-155">OUTPUTS</span></span>

### <span data-ttu-id="7cc5c-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7cc5c-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7cc5c-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cc5c-157">NOTES</span></span>

## <span data-ttu-id="7cc5c-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cc5c-158">RELATED LINKS</span></span>

[<span data-ttu-id="7cc5c-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7cc5c-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7cc5c-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7cc5c-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7cc5c-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7cc5c-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


