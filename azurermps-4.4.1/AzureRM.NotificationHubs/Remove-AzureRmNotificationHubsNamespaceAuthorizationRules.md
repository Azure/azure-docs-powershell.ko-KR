---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: e9b699e8839f2ba9426945ef0de883c4bfac40d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703678"
---
# <span data-ttu-id="c0fb3-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c0fb3-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="c0fb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fb3-103">알림 허브 네임 스페이스에서 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0fb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0fb3-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0fb3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c0fb3-105">DESCRIPTION</span></span>
<span data-ttu-id="c0fb3-106">**AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet은 알림 허브 네임 스페이스에서 SAS (공유 액세스 서명) 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="c0fb3-107">권한 부여 규칙은 네임 스페이스에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="c0fb3-108">이 작업은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="c0fb3-109">사용 권한 수준은 다음 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="c0fb3-110">듣기</span><span class="sxs-lookup"><span data-stu-id="c0fb3-110">Listen</span></span>
- <span data-ttu-id="c0fb3-111">보내기</span><span class="sxs-lookup"><span data-stu-id="c0fb3-111">Send</span></span>
- <span data-ttu-id="c0fb3-112">관리자</span><span class="sxs-lookup"><span data-stu-id="c0fb3-112">Manage</span></span>

<span data-ttu-id="c0fb3-113">클라이언트는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="c0fb3-114">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 권한에 대 한 URI로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="c0fb3-115">권한 부여 규칙을 제거 하면 해당 사용자 권한도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="c0fb3-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c0fb3-116">EXAMPLES</span></span>

### <span data-ttu-id="c0fb3-117">예제 1: 네임 스페이스에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="c0fb3-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c0fb3-118">이 명령은 ContosoNamespace 이라는 네임 스페이스에서 ListenRule 이라는 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="c0fb3-119">이 명령을 실행할 때 네임 스페이스에 할당 되는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="c0fb3-120">변수</span><span class="sxs-lookup"><span data-stu-id="c0fb3-120">PARAMETERS</span></span>

### <span data-ttu-id="c0fb3-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0fb3-121">-AuthorizationRule</span></span>
<span data-ttu-id="c0fb3-122">제거할 SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="c0fb3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c0fb3-123">-Force</span></span>
<span data-ttu-id="c0fb3-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c0fb3-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c0fb3-125">-Namespace</span></span>
<span data-ttu-id="c0fb3-126">권한 부여 규칙이 할당 되는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-126">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="c0fb3-127">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="c0fb3-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c0fb3-128">-ResourceGroup</span></span>
<span data-ttu-id="c0fb3-129">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-129">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="c0fb3-130">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c0fb3-131">-확인</span><span class="sxs-lookup"><span data-stu-id="c0fb3-131">-Confirm</span></span>
<span data-ttu-id="c0fb3-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0fb3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0fb3-133">-WhatIf</span></span>
<span data-ttu-id="c0fb3-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0fb3-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0fb3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fb3-136">-DefaultProfile</span></span>
<span data-ttu-id="c0fb3-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0fb3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fb3-138">CommonParameters</span></span>
<span data-ttu-id="c0fb3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0fb3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fb3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0fb3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fb3-141">입력</span><span class="sxs-lookup"><span data-stu-id="c0fb3-141">INPUTS</span></span>

## <span data-ttu-id="c0fb3-142">출력</span><span class="sxs-lookup"><span data-stu-id="c0fb3-142">OUTPUTS</span></span>

### <span data-ttu-id="c0fb3-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c0fb3-143">System.Boolean</span></span>

## <span data-ttu-id="c0fb3-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c0fb3-144">NOTES</span></span>

## <span data-ttu-id="c0fb3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0fb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="c0fb3-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c0fb3-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="c0fb3-147">새로운 AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c0fb3-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="c0fb3-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="c0fb3-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


