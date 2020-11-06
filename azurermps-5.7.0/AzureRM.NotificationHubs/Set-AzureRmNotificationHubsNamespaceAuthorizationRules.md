---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537655"
---
# <span data-ttu-id="60120-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="60120-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="60120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60120-102">SYNOPSIS</span></span>
<span data-ttu-id="60120-103">알림 허브 네임 스페이스에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60120-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60120-104">SYNTAX</span></span>

### <span data-ttu-id="60120-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="60120-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60120-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="60120-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60120-107">설명은</span><span class="sxs-lookup"><span data-stu-id="60120-107">DESCRIPTION</span></span>
<span data-ttu-id="60120-108">**AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet은 알림 허브 네임 스페이스에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="60120-109">권한 부여 규칙은 해당 네임 스페이스에 포함 된 알림 허브 및 네임 스페이스에 대 한 사용자 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="60120-110">이 cmdlet은 네임 스페이스에 할당 된 권한 부여 규칙을 수정 하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="60120-111">하나를 사용 하는 경우 **Sharedaccessauthorizationruleattributes** 개체의 인스턴스를 만든 다음 규칙을 적용할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="60120-112">.NET Framework를 사용 하 여이를 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="60120-113">그런 다음 *SASRule* 매개 변수를 통해 해당 속성 값을 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="60120-114">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="60120-115">JSON 파일은 다음과 같은 구문을 사용 하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="60120-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="60120-116">{</span><span class="sxs-lookup"><span data-stu-id="60120-116">{</span></span>  
    <span data-ttu-id="60120-117">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="60120-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="60120-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="60120-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="60120-119">"권한": \[</span><span class="sxs-lookup"><span data-stu-id="60120-119">"Rights": \[</span></span>  
        <span data-ttu-id="60120-120">"듣기",</span><span class="sxs-lookup"><span data-stu-id="60120-120">"Listen",</span></span>  
        <span data-ttu-id="60120-121">보내며</span><span class="sxs-lookup"><span data-stu-id="60120-121">"Send"</span></span>  
    \]  
<span data-ttu-id="60120-122">}</span><span class="sxs-lookup"><span data-stu-id="60120-122">}</span></span>

<span data-ttu-id="60120-123">앞의 JSON 샘플에서는 **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet을 함께 사용 하는 경우 사용자에 게 네임 스페이스에 대 한 수신 및 보내기 권한을 제공 하도록 ContosoAuthorizationRule 이라는 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="60120-124">예제의</span><span class="sxs-lookup"><span data-stu-id="60120-124">EXAMPLES</span></span>

### <span data-ttu-id="60120-125">예제 1: 네임 스페이스에 할당 된 권한 부여 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="60120-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="60120-126">이 명령은 ContosoNamespace 이라는 네임 스페이스에 할당 된 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="60120-127">네임 스페이스에 할당 되는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="60120-128">권한 부여 규칙에 대 한 정보는 명령 자체에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="60120-129">대신, C:\Configuration\AuthorizationRules.js입력 파일에서 해당 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60120-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="60120-130">변수</span><span class="sxs-lookup"><span data-stu-id="60120-130">PARAMETERS</span></span>

### <span data-ttu-id="60120-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60120-131">-DefaultProfile</span></span>
<span data-ttu-id="60120-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60120-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60120-133">-Force</span><span class="sxs-lookup"><span data-stu-id="60120-133">-Force</span></span>
<span data-ttu-id="60120-134">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-134">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60120-135">-InputFile</span><span class="sxs-lookup"><span data-stu-id="60120-135">-InputFile</span></span>
<span data-ttu-id="60120-136">새 규칙에 대 한 구성 정보를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60120-137">-Namespace</span><span class="sxs-lookup"><span data-stu-id="60120-137">-Namespace</span></span>
<span data-ttu-id="60120-138">이 cmdlet이 수정 하는 권한 부여 규칙을 포함 하는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="60120-139">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="60120-140">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60120-140">-ResourceGroup</span></span>
<span data-ttu-id="60120-141">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="60120-142">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="60120-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="60120-143">-SASRule</span></span>
<span data-ttu-id="60120-144">이 cmdlet이 수정 하는 권한 부여 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60120-145">-확인</span><span class="sxs-lookup"><span data-stu-id="60120-145">-Confirm</span></span>
<span data-ttu-id="60120-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60120-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60120-147">-WhatIf</span></span>
<span data-ttu-id="60120-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60120-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60120-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60120-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60120-150">CommonParameters</span></span>
<span data-ttu-id="60120-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60120-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60120-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60120-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60120-153">입력</span><span class="sxs-lookup"><span data-stu-id="60120-153">INPUTS</span></span>

### <span data-ttu-id="60120-154">않아야</span><span class="sxs-lookup"><span data-stu-id="60120-154">None</span></span>
<span data-ttu-id="60120-155">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60120-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60120-156">출력</span><span class="sxs-lookup"><span data-stu-id="60120-156">OUTPUTS</span></span>

### <span data-ttu-id="60120-157">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="60120-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="60120-158">상속자</span><span class="sxs-lookup"><span data-stu-id="60120-158">NOTES</span></span>

## <span data-ttu-id="60120-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60120-159">RELATED LINKS</span></span>

[<span data-ttu-id="60120-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="60120-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="60120-161">새로운 AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="60120-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="60120-162">제거-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="60120-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


