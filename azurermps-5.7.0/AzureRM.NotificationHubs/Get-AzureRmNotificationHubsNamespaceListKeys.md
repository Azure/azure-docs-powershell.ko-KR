---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespacelistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 2fb9eeb3b5d6bcc3a2183bc652b74caa370e4d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530419"
---
# <span data-ttu-id="58886-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="58886-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="58886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58886-102">SYNOPSIS</span></span>
<span data-ttu-id="58886-103">알림 허브 네임 스페이스 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58886-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58886-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58886-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58886-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58886-105">DESCRIPTION</span></span>
<span data-ttu-id="58886-106">**AzureRmNotificationHubsNamespaceListKeys** cmdlet은 알림 허브 네임 스페이스에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="58886-107">권한 부여 규칙은 알림 허브 네임 스페이스에 대 한 사용자 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="58886-108">각 규칙에는 기본 및 보조 연결 문자열이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58886-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="58886-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58886-109">EXAMPLES</span></span>

### <span data-ttu-id="58886-110">예제 1: 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="58886-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="58886-111">이 명령은 ContosoNamespace 네임 스페이스에 할당 된 ListenRule 이라는 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="58886-112">이 명령을 실행할 때는 네임 스페이스에 할당 된 리소스 그룹의 이름을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="58886-113">변수</span><span class="sxs-lookup"><span data-stu-id="58886-113">PARAMETERS</span></span>

### <span data-ttu-id="58886-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="58886-114">-AuthorizationRule</span></span>
<span data-ttu-id="58886-115">SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="58886-116">이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="58886-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58886-117">-DefaultProfile</span></span>
<span data-ttu-id="58886-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="58886-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58886-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="58886-119">-Namespace</span></span>
<span data-ttu-id="58886-120">이 cmdlet이 가져오는 연결 문자열을 포함 하는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="58886-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="58886-121">-ResourceGroup</span></span>
<span data-ttu-id="58886-122">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-122">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="58886-123">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="58886-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58886-124">CommonParameters</span></span>
<span data-ttu-id="58886-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58886-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58886-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58886-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58886-127">입력</span><span class="sxs-lookup"><span data-stu-id="58886-127">INPUTS</span></span>

### <span data-ttu-id="58886-128">않아야</span><span class="sxs-lookup"><span data-stu-id="58886-128">None</span></span>
<span data-ttu-id="58886-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58886-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58886-130">출력</span><span class="sxs-lookup"><span data-stu-id="58886-130">OUTPUTS</span></span>

### <span data-ttu-id="58886-131">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="58886-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="58886-132">상속자</span><span class="sxs-lookup"><span data-stu-id="58886-132">NOTES</span></span>

## <span data-ttu-id="58886-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58886-133">RELATED LINKS</span></span>

[<span data-ttu-id="58886-134">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="58886-134">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="58886-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="58886-135">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


