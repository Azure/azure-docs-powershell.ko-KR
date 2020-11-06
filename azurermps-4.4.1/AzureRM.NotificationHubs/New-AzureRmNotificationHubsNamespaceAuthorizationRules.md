---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: baccd437f98a12376d564bee35bdb74d736ec225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529244"
---
# <span data-ttu-id="a6f5c-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a6f5c-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="a6f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f5c-103">권한 부여 규칙을 만들고 해당 규칙을 알림 허브 네임 스페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6f5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6f5c-104">SYNTAX</span></span>

### <span data-ttu-id="a6f5c-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6f5c-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6f5c-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6f5c-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f5c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a6f5c-107">DESCRIPTION</span></span>
<span data-ttu-id="a6f5c-108">**AzureRmNotificationHubsNamespaceAuthorizationRules** CMDLET은 SAS (공유 액세스 서명) 권한 부여 규칙을 만들어 알림 허브 네임 스페이스에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="a6f5c-109">권한 부여 규칙은 해당 네임 스페이스에 포함 된 알림 허브 및 네임 스페이스에 대 한 사용자 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="a6f5c-110">이 cmdlet은 새 권한 부여 규칙을 만들어 네임 스페이스에 할당 하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="a6f5c-111">**Sharedaccessauthorizationruleattributes** 개체의 인스턴스를 만든 다음 새 규칙을 포함할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="a6f5c-112">.NET Framework를 사용 하 여이 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="a6f5c-113">그런 다음 *SASRule* 매개 변수를 사용 하 여 해당 속성 값을 새 규칙으로 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="a6f5c-114">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 사용 하 여 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="a6f5c-115">JSON 파일은 다음과 같은 구문을 사용 하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="a6f5c-116">{</span><span class="sxs-lookup"><span data-stu-id="a6f5c-116">{</span></span>  
    <span data-ttu-id="a6f5c-117">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="a6f5c-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="a6f5c-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="a6f5c-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="a6f5c-119">"권한": \[</span><span class="sxs-lookup"><span data-stu-id="a6f5c-119">"Rights": \[</span></span>  
        <span data-ttu-id="a6f5c-120">"듣기",</span><span class="sxs-lookup"><span data-stu-id="a6f5c-120">"Listen",</span></span>  
        <span data-ttu-id="a6f5c-121">보내며</span><span class="sxs-lookup"><span data-stu-id="a6f5c-121">"Send"</span></span>  
    \]  
<span data-ttu-id="a6f5c-122">}</span><span class="sxs-lookup"><span data-stu-id="a6f5c-122">}</span></span>

<span data-ttu-id="a6f5c-123">앞의 JSON 샘플에서는 **AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet을 함께 사용 하는 경우 사용자가 네임 스페이스에 대 한 수신을 보내고 받을 수 있도록 하는 ContosoAuthorizationRule 라는 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="a6f5c-124">인증에 사용 되는 *PrimaryKey* 는 다음 Windows PowerShell 명령을 사용 하 여 임의로 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="a6f5c-125">\[Convert \] :: ToBase64String ((1.32 |% { \[ byte/] (가져오기-임의-최소 0-최대 255)))))))))</span><span class="sxs-lookup"><span data-stu-id="a6f5c-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="a6f5c-126">예제의</span><span class="sxs-lookup"><span data-stu-id="a6f5c-126">EXAMPLES</span></span>

### <span data-ttu-id="a6f5c-127">예제 1: 권한 부여 규칙을 만들어 네임 스페이스에 할당</span><span class="sxs-lookup"><span data-stu-id="a6f5c-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="a6f5c-128">이 명령은 권한 부여 규칙을 만들고이 규칙을 네임 스페이스 ContosoNamespace에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="a6f5c-129">이 규칙을 만들 때 네임 스페이스에 할당 되는 적절 한 네임 스페이스와 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="a6f5c-130">그러나 규칙 자체에 대 한 정보를 지정할 필요는 없습니다. C:\Configuration\NamespaceAuthorizationRules.js입력 파일에서 규칙 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="a6f5c-131">변수</span><span class="sxs-lookup"><span data-stu-id="a6f5c-131">PARAMETERS</span></span>

### <span data-ttu-id="a6f5c-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a6f5c-132">-InputFile</span></span>
<span data-ttu-id="a6f5c-133">새 권한 부여 규칙에 대 한 구성 정보를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-133">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="a6f5c-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6f5c-134">-Namespace</span></span>
<span data-ttu-id="a6f5c-135">권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-135">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="a6f5c-136">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-136">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="a6f5c-137">새 규칙을 기존 네임 스페이스에 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-137">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="a6f5c-138">**AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet이 새 네임 스페이스를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-138">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="a6f5c-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6f5c-139">-ResourceGroup</span></span>
<span data-ttu-id="a6f5c-140">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-140">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="a6f5c-141">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-141">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="a6f5c-142">기존 리소스 그룹을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-142">You must use an existing resource group.</span></span>
<span data-ttu-id="a6f5c-143">이 cmdlet은 새 리소스 그룹을 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-143">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="a6f5c-144">-SASRule</span><span class="sxs-lookup"><span data-stu-id="a6f5c-144">-SASRule</span></span>
<span data-ttu-id="a6f5c-145">새 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-145">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="a6f5c-146">-확인</span><span class="sxs-lookup"><span data-stu-id="a6f5c-146">-Confirm</span></span>
<span data-ttu-id="a6f5c-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f5c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f5c-148">-WhatIf</span></span>
<span data-ttu-id="a6f5c-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6f5c-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f5c-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f5c-151">-DefaultProfile</span></span>
<span data-ttu-id="a6f5c-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f5c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f5c-153">CommonParameters</span></span>
<span data-ttu-id="a6f5c-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f5c-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f5c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f5c-156">입력</span><span class="sxs-lookup"><span data-stu-id="a6f5c-156">INPUTS</span></span>

## <span data-ttu-id="a6f5c-157">출력</span><span class="sxs-lookup"><span data-stu-id="a6f5c-157">OUTPUTS</span></span>

### <span data-ttu-id="a6f5c-158">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a6f5c-158">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a6f5c-159">상속자</span><span class="sxs-lookup"><span data-stu-id="a6f5c-159">NOTES</span></span>

## <span data-ttu-id="a6f5c-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6f5c-160">RELATED LINKS</span></span>

[<span data-ttu-id="a6f5c-161">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a6f5c-161">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a6f5c-162">제거-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a6f5c-162">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="a6f5c-163">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="a6f5c-163">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


