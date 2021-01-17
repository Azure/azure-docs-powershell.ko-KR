---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385036"
---
# <span data-ttu-id="0908d-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0908d-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="0908d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0908d-102">SYNOPSIS</span></span>
<span data-ttu-id="0908d-103">알림 허브에 대한 권한 부여 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="0908d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0908d-104">SYNTAX</span></span>

### <span data-ttu-id="0908d-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0908d-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0908d-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="0908d-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0908d-107">설명</span><span class="sxs-lookup"><span data-stu-id="0908d-107">DESCRIPTION</span></span>
<span data-ttu-id="0908d-108">**Set-AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에 할당된 SAS(공유 액세스 서명) 권한 부여 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="0908d-109">권한 부여 규칙은 다른 사용 권한 수준에 따라 URIS로 링크를 만들어 알림 허브에 대한 액세스를 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="0908d-110">사용 권한 수준은 다음 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="0908d-111">수신</span><span class="sxs-lookup"><span data-stu-id="0908d-111">Listen</span></span>
- <span data-ttu-id="0908d-112">보내기</span><span class="sxs-lookup"><span data-stu-id="0908d-112">Send</span></span>
- <span data-ttu-id="0908d-113">관리 클라이언트는 적절한 사용 권한 수준에 따라 이러한 UR 중 하나로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="0908d-114">예를 들어 수신 권한이 부여된 클라이언트는 해당 권한에 대한 URI로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="0908d-115">이 cmdlet은 알림 허브에 할당된 권한 부여 규칙을 수정하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="0908d-116">하나의 경우 **SharedAccessAuthorizationRuleAttributes** 개체의 인스턴스를 만든 다음 규칙에서 소유할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="0908d-117">.NET Framework를 통해 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="0908d-118">그런 다음 *SASRule* 매개 변수를 사용하여 해당 속성 값을 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="0908d-119">또는 관련 구성 값을 포함하는 JSON(JavaScript Object Notation) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="0908d-120">JSON 파일은 { "Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="0908d-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="0908d-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="0908d-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="0908d-122">"Rights": \[</span><span class="sxs-lookup"><span data-stu-id="0908d-122">"Rights": \[</span></span>  
        <span data-ttu-id="0908d-123">"수신",</span><span class="sxs-lookup"><span data-stu-id="0908d-123">"Listen",</span></span>  
        <span data-ttu-id="0908d-124">"보내기"</span><span class="sxs-lookup"><span data-stu-id="0908d-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="0908d-125">} New-AzNotificationHubAuthorizationRule cmdlet과 함께 사용하는 경우 앞의 JSON 샘플은 사용자에게 허브에 수신 및 보내기 권한을 부여하기 위해 ContosoAuthorizationRule이라는 권한 부여 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="0908d-126">예제</span><span class="sxs-lookup"><span data-stu-id="0908d-126">EXAMPLES</span></span>

### <span data-ttu-id="0908d-127">예제 1: 알림 허브에 할당된 권한 부여 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="0908d-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="0908d-128">이 명령은 ContosoExternalHub라는 알림 허브에 할당된 권한 부여 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="0908d-129">허브가 있는 네임스페이스와 허브가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="0908d-130">수정된 규칙에 대한 정보는 명령 자체에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="0908d-131">대신, 해당 정보는 입력 파일에서 찾을 수 C:\Configuration\AuthorizationRules.js.</span><span class="sxs-lookup"><span data-stu-id="0908d-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="0908d-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0908d-132">PARAMETERS</span></span>

### <span data-ttu-id="0908d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0908d-133">-DefaultProfile</span></span>
<span data-ttu-id="0908d-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0908d-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0908d-135">-Force</span><span class="sxs-lookup"><span data-stu-id="0908d-135">-Force</span></span>
<span data-ttu-id="0908d-136">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0908d-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0908d-137">-InputFile</span></span>
<span data-ttu-id="0908d-138">새 규칙에 대한 구성 정보를 포함하는 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="0908d-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0908d-139">-Namespace</span></span>
<span data-ttu-id="0908d-140">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="0908d-141">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0908d-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0908d-142">-NotificationHub</span></span>
<span data-ttu-id="0908d-143">이 cmdlet이 권한 부여 규칙을 할당하는 알림 허브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="0908d-144">알림 허브는 해당 클라이언트에서 사용하는 경우와 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="0908d-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0908d-145">-ResourceGroup</span></span>
<span data-ttu-id="0908d-146">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="0908d-147">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0908d-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="0908d-148">-SASRule</span></span>
<span data-ttu-id="0908d-149">수정된 권한 부여 규칙에 대한 구성 정보를 포함하는 **SharedAccessAuthorizationRuleAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="0908d-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0908d-150">-Confirm</span></span>
<span data-ttu-id="0908d-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0908d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0908d-152">-WhatIf</span></span>
<span data-ttu-id="0908d-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0908d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0908d-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0908d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0908d-155">CommonParameters</span></span>
<span data-ttu-id="0908d-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0908d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0908d-157">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0908d-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0908d-158">입력</span><span class="sxs-lookup"><span data-stu-id="0908d-158">INPUTS</span></span>

### <span data-ttu-id="0908d-159">System.String</span><span class="sxs-lookup"><span data-stu-id="0908d-159">System.String</span></span>

## <span data-ttu-id="0908d-160">출력</span><span class="sxs-lookup"><span data-stu-id="0908d-160">OUTPUTS</span></span>

### <span data-ttu-id="0908d-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0908d-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0908d-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0908d-162">NOTES</span></span>

## <span data-ttu-id="0908d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0908d-163">RELATED LINKS</span></span>

[<span data-ttu-id="0908d-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0908d-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="0908d-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0908d-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="0908d-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0908d-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)


