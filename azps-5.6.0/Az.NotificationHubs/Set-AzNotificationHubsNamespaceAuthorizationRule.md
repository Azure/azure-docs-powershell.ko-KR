---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 2f5ff44e6d96900afe36b9ade8360fb0a69ec726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951099"
---
# <span data-ttu-id="1c6d3-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1c6d3-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="1c6d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6d3-103">알림 허브 네임스페이스에 대한 권한 부여 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="1c6d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c6d3-104">SYNTAX</span></span>

### <span data-ttu-id="1c6d3-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c6d3-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c6d3-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c6d3-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c6d3-107">설명</span><span class="sxs-lookup"><span data-stu-id="1c6d3-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6d3-108">**Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet은 알림 허브 네임스페이스에 할당된 SAS(공유 액세스 서명) 권한 부여 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="1c6d3-109">권한 부여 규칙은 네임스페이스 및 해당 네임스페이스에 포함된 알림 허브에 대한 사용자 권한을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="1c6d3-110">이 cmdlet은 네임스페이스에 할당된 권한 부여 규칙을 수정하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="1c6d3-111">하나에 대해 **SharedAccessAuthorizationRuleAttributes** 개체의 인스턴스를 만든 다음 규칙을 소유할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="1c6d3-112">이 작업을 수행하기 위해 .NET Framework 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="1c6d3-113">그런 다음 *SASRule* 매개 변수를 통해 해당 속성 값을 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="1c6d3-114">또는 관련 구성 값이 포함된 JSON(JavaScript 개체표시) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="1c6d3-115">JSON 파일은 이와 유사한 구문을 사용하는 텍스트 파일입니다. {</span><span class="sxs-lookup"><span data-stu-id="1c6d3-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="1c6d3-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="1c6d3-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="1c6d3-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="1c6d3-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="1c6d3-118">"권한": \[</span><span class="sxs-lookup"><span data-stu-id="1c6d3-118">"Rights": \[</span></span>  
        <span data-ttu-id="1c6d3-119">"수신",</span><span class="sxs-lookup"><span data-stu-id="1c6d3-119">"Listen",</span></span>  
        <span data-ttu-id="1c6d3-120">"보내기"</span><span class="sxs-lookup"><span data-stu-id="1c6d3-120">"Send"</span></span>  
    \]  
<span data-ttu-id="1c6d3-121">} **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet과 함께 사용하는 경우 앞의 JSON 샘플에서는 ContosoAuthorizationRule이라는 권한 부여 규칙을 수정하여 사용자에게 네임스페이스에 대한 수신 및 보내기 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="1c6d3-122">예제</span><span class="sxs-lookup"><span data-stu-id="1c6d3-122">EXAMPLES</span></span>

### <span data-ttu-id="1c6d3-123">예제 1: 네임스페이스에 할당된 권한 부여 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="1c6d3-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="1c6d3-124">이 명령은 ContosoNamespace라는 네임스페이스에 할당된 권한 부여 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="1c6d3-125">네임스페이스가 할당된 리소스 그룹을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="1c6d3-126">권한 부여 규칙에 대한 정보는 명령 자체에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="1c6d3-127">대신 입력 파일에서 해당 C:\Configuration\AuthorizationRules.js있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="1c6d3-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c6d3-128">PARAMETERS</span></span>

### <span data-ttu-id="1c6d3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6d3-129">-DefaultProfile</span></span>
<span data-ttu-id="1c6d3-130">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c6d3-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6d3-131">-Force</span><span class="sxs-lookup"><span data-stu-id="1c6d3-131">-Force</span></span>
<span data-ttu-id="1c6d3-132">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1c6d3-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1c6d3-133">-InputFile</span></span>
<span data-ttu-id="1c6d3-134">새 규칙에 대한 구성 정보가 포함된 JSON 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="1c6d3-135">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="1c6d3-135">-Namespace</span></span>
<span data-ttu-id="1c6d3-136">이 cmdlet에서 수정하는 권한 부여 규칙을 포함하는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="1c6d3-137">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="1c6d3-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c6d3-138">-ResourceGroup</span></span>
<span data-ttu-id="1c6d3-139">네임스페이스가 할당되는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="1c6d3-140">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="1c6d3-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="1c6d3-141">-SASRule</span></span>
<span data-ttu-id="1c6d3-142">이 cmdlet이 수정하는 권한 부여 규칙에 대한 구성 정보가 포함된 **SharedAccesAuthorizationRuleAttributes** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1c6d3-143">-확인</span><span class="sxs-lookup"><span data-stu-id="1c6d3-143">-Confirm</span></span>
<span data-ttu-id="1c6d3-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6d3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6d3-145">-WhatIf</span></span>
<span data-ttu-id="1c6d3-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c6d3-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6d3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6d3-148">CommonParameters</span></span>
<span data-ttu-id="1c6d3-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6d3-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c6d3-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6d3-151">입력</span><span class="sxs-lookup"><span data-stu-id="1c6d3-151">INPUTS</span></span>

### <span data-ttu-id="1c6d3-152">System.String</span><span class="sxs-lookup"><span data-stu-id="1c6d3-152">System.String</span></span>

## <span data-ttu-id="1c6d3-153">출력</span><span class="sxs-lookup"><span data-stu-id="1c6d3-153">OUTPUTS</span></span>

### <span data-ttu-id="1c6d3-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="1c6d3-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="1c6d3-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c6d3-155">NOTES</span></span>

## <span data-ttu-id="1c6d3-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c6d3-156">RELATED LINKS</span></span>

[<span data-ttu-id="1c6d3-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1c6d3-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1c6d3-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1c6d3-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="1c6d3-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1c6d3-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)


