---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 0c834f8ee24090fa0da11f6c01fb0ddad3251756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533027"
---
# <span data-ttu-id="aff12-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="aff12-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="aff12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff12-102">SYNOPSIS</span></span>
<span data-ttu-id="aff12-103">알림 허브 네임 스페이스 권한 부여 규칙과 연결 된 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aff12-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aff12-105">DESCRIPTION</span></span>
<span data-ttu-id="aff12-106">**AzureRmNotificationHubsNamespaceListKeys** cmdlet은 알림 허브 네임 스페이스에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="aff12-107">권한 부여 규칙은 알림 허브 네임 스페이스에 대 한 사용자 권한을 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="aff12-108">각 규칙에는 기본 및 보조 연결 문자열이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="aff12-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aff12-109">EXAMPLES</span></span>

### <span data-ttu-id="aff12-110">예제 1: 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열 가져오기</span><span class="sxs-lookup"><span data-stu-id="aff12-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="aff12-111">이 명령은 ContosoNamespace 네임 스페이스에 할당 된 ListenRule 이라는 권한 부여 규칙에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="aff12-112">이 명령을 실행할 때는 네임 스페이스에 할당 된 리소스 그룹의 이름을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="aff12-113">변수</span><span class="sxs-lookup"><span data-stu-id="aff12-113">PARAMETERS</span></span>

### <span data-ttu-id="aff12-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aff12-114">-AuthorizationRule</span></span>
<span data-ttu-id="aff12-115">SAS 인증 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="aff12-116">이러한 규칙은 사용자가 알림 허브에 대해 갖는 액세스 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="aff12-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aff12-117">-Namespace</span></span>
<span data-ttu-id="aff12-118">이 cmdlet이 가져오는 연결 문자열을 포함 하는 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-118">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="aff12-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aff12-119">-ResourceGroup</span></span>
<span data-ttu-id="aff12-120">네임 스페이스를 할당할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-120">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="aff12-121">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="aff12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff12-122">-DefaultProfile</span></span>
<span data-ttu-id="aff12-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff12-124">CommonParameters</span></span>
<span data-ttu-id="aff12-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff12-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff12-127">입력</span><span class="sxs-lookup"><span data-stu-id="aff12-127">INPUTS</span></span>

## <span data-ttu-id="aff12-128">출력</span><span class="sxs-lookup"><span data-stu-id="aff12-128">OUTPUTS</span></span>

### <span data-ttu-id="aff12-129">Microsoft. 관리.. i g m. 목록 키</span><span class="sxs-lookup"><span data-stu-id="aff12-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="aff12-130">상속자</span><span class="sxs-lookup"><span data-stu-id="aff12-130">NOTES</span></span>

## <span data-ttu-id="aff12-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aff12-131">RELATED LINKS</span></span>

[<span data-ttu-id="aff12-132">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="aff12-132">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="aff12-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="aff12-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


