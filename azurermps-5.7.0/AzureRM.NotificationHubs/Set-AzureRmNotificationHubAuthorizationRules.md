---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 6203c5554dcdbfbd40c861a3f73e1a5947228030
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537659"
---
# <span data-ttu-id="6e290-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6e290-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="6e290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e290-102">SYNOPSIS</span></span>
<span data-ttu-id="6e290-103">알림 허브에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e290-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e290-104">SYNTAX</span></span>

### <span data-ttu-id="6e290-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e290-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e290-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e290-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e290-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6e290-107">DESCRIPTION</span></span>
<span data-ttu-id="6e290-108">**AzureRmNotificationHubAuthorizationRules** cmdlet은 알림 허브에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="6e290-109">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="6e290-110">사용 권한 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="6e290-111">듣기</span><span class="sxs-lookup"><span data-stu-id="6e290-111">Listen</span></span>
- <span data-ttu-id="6e290-112">보내기</span><span class="sxs-lookup"><span data-stu-id="6e290-112">Send</span></span>
- <span data-ttu-id="6e290-113">관리자</span><span class="sxs-lookup"><span data-stu-id="6e290-113">Manage</span></span>

<span data-ttu-id="6e290-114">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="6e290-115">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 권한의 URI로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="6e290-116">이 cmdlet은 알림 허브에 할당 된 권한 부여 규칙을 수정 하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="6e290-117">하나를 사용 하는 경우 **Sharedaccessauthorizationruleattributes** 개체의 인스턴스를 만든 다음 규칙을 적용할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="6e290-118">.NET Framework를 통해 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="6e290-119">그런 다음 *SASRule* 매개 변수를 사용 하 여 해당 속성 값을 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="6e290-120">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="6e290-121">JSON 파일은 다음과 같은 구문을 사용 하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="6e290-122">{"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="6e290-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="6e290-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="6e290-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="6e290-124">"권한": \[</span><span class="sxs-lookup"><span data-stu-id="6e290-124">"Rights": \[</span></span>  
        <span data-ttu-id="6e290-125">"듣기",</span><span class="sxs-lookup"><span data-stu-id="6e290-125">"Listen",</span></span>  
        <span data-ttu-id="6e290-126">보내며</span><span class="sxs-lookup"><span data-stu-id="6e290-126">"Send"</span></span>  
    \]  
<span data-ttu-id="6e290-127">}</span><span class="sxs-lookup"><span data-stu-id="6e290-127">}</span></span>

<span data-ttu-id="6e290-128">앞의 JSON 샘플에서는 New-AzureRmNotificationHubAuthorizationRules cmdlet과 함께 사용 하는 경우 사용자가 허브에 대 한 수신 권한을 주고 받을 수 있도록 ContosoAuthorizationRule 이라는 인증 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="6e290-129">예제의</span><span class="sxs-lookup"><span data-stu-id="6e290-129">EXAMPLES</span></span>

### <span data-ttu-id="6e290-130">예제 1: 알림 허브에 할당 된 권한 부여 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="6e290-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="6e290-131">이 명령은 ContosoExternalHub 이라는 알림 허브에 할당 된 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="6e290-132">허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="6e290-133">명령 자체에는 수정 되는 규칙에 대 한 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="6e290-134">대신이 정보는 입력 파일 C:\Configuration\AuthorizationRules.js에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="6e290-135">변수</span><span class="sxs-lookup"><span data-stu-id="6e290-135">PARAMETERS</span></span>

### <span data-ttu-id="6e290-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e290-136">-DefaultProfile</span></span>
<span data-ttu-id="6e290-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6e290-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-138">-Force</span><span class="sxs-lookup"><span data-stu-id="6e290-138">-Force</span></span>
<span data-ttu-id="6e290-139">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-139">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-140">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6e290-140">-InputFile</span></span>
<span data-ttu-id="6e290-141">새 규칙에 대 한 구성 정보를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-141">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-142">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e290-142">-Namespace</span></span>
<span data-ttu-id="6e290-143">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-143">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6e290-144">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-144">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-145">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e290-145">-NotificationHub</span></span>
<span data-ttu-id="6e290-146">이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-146">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="6e290-147">알림 허브는 해당 클라이언트에서 사용 하는 것과 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-147">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-148">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e290-148">-ResourceGroup</span></span>
<span data-ttu-id="6e290-149">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-149">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="6e290-150">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-150">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-151">-SASRule</span><span class="sxs-lookup"><span data-stu-id="6e290-151">-SASRule</span></span>
<span data-ttu-id="6e290-152">수정 되는 권한 부여 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-152">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-153">-확인</span><span class="sxs-lookup"><span data-stu-id="6e290-153">-Confirm</span></span>
<span data-ttu-id="6e290-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e290-155">-WhatIf</span></span>
<span data-ttu-id="6e290-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e290-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e290-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e290-158">CommonParameters</span></span>
<span data-ttu-id="6e290-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e290-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e290-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e290-161">입력</span><span class="sxs-lookup"><span data-stu-id="6e290-161">INPUTS</span></span>

### <span data-ttu-id="6e290-162">않아야</span><span class="sxs-lookup"><span data-stu-id="6e290-162">None</span></span>
<span data-ttu-id="6e290-163">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e290-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e290-164">출력</span><span class="sxs-lookup"><span data-stu-id="6e290-164">OUTPUTS</span></span>

### <span data-ttu-id="6e290-165">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6e290-165">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="6e290-166">상속자</span><span class="sxs-lookup"><span data-stu-id="6e290-166">NOTES</span></span>

## <span data-ttu-id="6e290-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e290-167">RELATED LINKS</span></span>

[<span data-ttu-id="6e290-168">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6e290-168">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="6e290-169">새로운 AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6e290-169">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="6e290-170">제거-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="6e290-170">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)


