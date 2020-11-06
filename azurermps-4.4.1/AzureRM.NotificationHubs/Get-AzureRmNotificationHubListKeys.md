---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 924b729ca8ba324a6f44cade48ed803b2867b6b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537040"
---
# <span data-ttu-id="b3567-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="b3567-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="b3567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3567-102">SYNOPSIS</span></span>
<span data-ttu-id="b3567-103">알림 허브 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3567-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3567-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3567-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3567-105">DESCRIPTION</span></span>
<span data-ttu-id="b3567-106">**AzureRmNotificationHubListKeys** cmdlet은 알림 허브 Sa (공유 액세스 서명) 권한 부여 규칙의 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="b3567-107">권한 부여 규칙은 허브에 대 한 사용자 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="b3567-108">각 규칙에는 기본 및 보조 연결 문자열이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="b3567-109">이러한 연결 문자열 (Uri)은 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-109">These connection strings (URIs) perform the following:</span></span>

- <span data-ttu-id="b3567-110">사용자를 리소스에 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-110">Point users to a resource.</span></span>
- <span data-ttu-id="b3567-111">쿼리 매개 변수를 포함 하는 토큰을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-111">Include a token containing query parameters.</span></span>

<span data-ttu-id="b3567-112">이러한 매개 변수 중 하나인 시그니처는 사용자를 인증 하 고 지정 된 수준의 액세스를 제공 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="b3567-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b3567-113">EXAMPLES</span></span>

### <span data-ttu-id="b3567-114">예제 1: 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3567-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b3567-115">이 명령은 ContosoInternalHub 알림 허브에 할당 된 규칙 인 권한 부여 규칙 ListenRule에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="b3567-116">명령에 허브 네임 스페이스 및 리소스 그룹이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="b3567-117">변수</span><span class="sxs-lookup"><span data-stu-id="b3567-117">PARAMETERS</span></span>

### <span data-ttu-id="b3567-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3567-118">-AuthorizationRule</span></span>
<span data-ttu-id="b3567-119">SA (공유 액세스 서명) 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="b3567-120">이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3567-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3567-121">-Namespace</span></span>
<span data-ttu-id="b3567-122">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-122">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="b3567-123">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b3567-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b3567-124">-NotificationHub</span></span>
<span data-ttu-id="b3567-125">이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-125">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="b3567-126">알림 허브는 해당 클라이언트에서 사용 하는 플랫폼에 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="b3567-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3567-127">-ResourceGroup</span></span>
<span data-ttu-id="b3567-128">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="b3567-129">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b3567-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3567-130">-DefaultProfile</span></span>
<span data-ttu-id="b3567-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3567-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3567-132">CommonParameters</span></span>
<span data-ttu-id="b3567-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3567-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3567-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3567-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3567-135">입력</span><span class="sxs-lookup"><span data-stu-id="b3567-135">INPUTS</span></span>

## <span data-ttu-id="b3567-136">출력</span><span class="sxs-lookup"><span data-stu-id="b3567-136">OUTPUTS</span></span>

### <span data-ttu-id="b3567-137">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="b3567-137">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b3567-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b3567-138">NOTES</span></span>

## <span data-ttu-id="b3567-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3567-139">RELATED LINKS</span></span>

[<span data-ttu-id="b3567-140">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="b3567-140">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)


