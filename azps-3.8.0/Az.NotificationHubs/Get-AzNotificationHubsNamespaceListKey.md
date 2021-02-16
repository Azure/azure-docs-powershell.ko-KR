---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 5244602a6b6266ebabf02bbb927facda93e61d8b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403802"
---
# <span data-ttu-id="f01fd-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="f01fd-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="f01fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f01fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f01fd-103">알림 허브 네임스페이스 권한 부여 규칙과 연결된 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="f01fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="f01fd-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f01fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="f01fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f01fd-106">**Get-AzNotificationHubsNamespaceListKey** cmdlet은 알림 허브 네임스페이스에 할당된 SAS(공유 액세스 서명) 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="f01fd-107">권한 부여 규칙은 알림 허브 네임스페이스에 대한 사용자 권한을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="f01fd-108">각 규칙에는 기본 및 보조 연결 문자열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="f01fd-109">예제</span><span class="sxs-lookup"><span data-stu-id="f01fd-109">EXAMPLES</span></span>

### <span data-ttu-id="f01fd-110">예제 1: 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="f01fd-111">이 명령은 ContosoNamespace 네임스페이스에 할당된 ListenRule이라는 권한 부여 규칙에 대한 기본 및 보조 연결 문자열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="f01fd-112">이 명령을 실행할 때 네임스페이스가 할당된 리소스 그룹의 이름을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="f01fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f01fd-113">PARAMETERS</span></span>

### <span data-ttu-id="f01fd-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f01fd-114">-AuthorizationRule</span></span>
<span data-ttu-id="f01fd-115">SAS 인증 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="f01fd-116">이러한 규칙은 사용자가 알림 허브에 대한 액세스 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="f01fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01fd-117">-DefaultProfile</span></span>
<span data-ttu-id="f01fd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f01fd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f01fd-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f01fd-119">-Namespace</span></span>
<span data-ttu-id="f01fd-120">이 cmdlet에서 얻을 연결 문자열을 포함하는 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f01fd-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f01fd-121">-ResourceGroup</span></span>
<span data-ttu-id="f01fd-122">네임스페이스가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="f01fd-123">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f01fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01fd-124">CommonParameters</span></span>
<span data-ttu-id="f01fd-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f01fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01fd-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f01fd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01fd-127">입력</span><span class="sxs-lookup"><span data-stu-id="f01fd-127">INPUTS</span></span>

### <span data-ttu-id="f01fd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f01fd-128">System.String</span></span>

## <span data-ttu-id="f01fd-129">출력</span><span class="sxs-lookup"><span data-stu-id="f01fd-129">OUTPUTS</span></span>

### <span data-ttu-id="f01fd-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="f01fd-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="f01fd-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f01fd-131">NOTES</span></span>

## <span data-ttu-id="f01fd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f01fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="f01fd-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f01fd-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



