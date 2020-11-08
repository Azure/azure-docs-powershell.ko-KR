---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045614"
---
# <span data-ttu-id="d06c8-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d06c8-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="d06c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d06c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d06c8-103">서비스 버스 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="d06c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d06c8-104">SYNTAX</span></span>

### <span data-ttu-id="d06c8-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="d06c8-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d06c8-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="d06c8-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d06c8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d06c8-107">DESCRIPTION</span></span>
<span data-ttu-id="d06c8-108">서비스 버스 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="d06c8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d06c8-109">EXAMPLES</span></span>

### <span data-ttu-id="d06c8-110">예제 1: 네임 스페이스 수준에서 권한 부여 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d06c8-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="d06c8-111">MyNamespace에서 사용 가능한 모든 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="d06c8-112">예제 2: 큐에 대 한 권한 부여 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d06c8-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="d06c8-113">MyNamespace의 MyEntity 큐에서 사용 가능한 모든 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="d06c8-114">예제 3: 이름으로 권한 부여 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d06c8-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="d06c8-115">MyNamespace 수준에서 MyRule 이라는 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="d06c8-116">예제 4: 권한으로 권한 부여 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="d06c8-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="d06c8-117">네임 스페이스 수준에 대 한 보내기 권한이 있는 모든 권한 부여 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="d06c8-118">변수</span><span class="sxs-lookup"><span data-stu-id="d06c8-118">PARAMETERS</span></span>

### <span data-ttu-id="d06c8-119">-EntityName</span><span class="sxs-lookup"><span data-stu-id="d06c8-119">-EntityName</span></span>
<span data-ttu-id="d06c8-120">규칙을 적용할 엔터티 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-120">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="d06c8-121">-EntityType</span></span>
<span data-ttu-id="d06c8-122">엔터티 형식 (큐, 주제, 릴레이, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="d06c8-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d06c8-123">-Name</span></span>
<span data-ttu-id="d06c8-124">고유한 인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d06c8-125">-Namespace</span></span>
<span data-ttu-id="d06c8-126">권한 부여 규칙을 적용할 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="d06c8-127">EntityName을 제공 하지 않으면 규칙은 네임 스페이스 수준에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-127">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-128">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="d06c8-128">-Permission</span></span>
<span data-ttu-id="d06c8-129">필터링 할 승인 권한 (보내기, 관리, 수신 대기)입니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="d06c8-130">정확한 일치를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="d06c8-131">-Profile</span></span>
<span data-ttu-id="d06c8-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d06c8-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d06c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06c8-134">CommonParameters</span></span>
<span data-ttu-id="d06c8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06c8-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06c8-137">입력</span><span class="sxs-lookup"><span data-stu-id="d06c8-137">INPUTS</span></span>

## <span data-ttu-id="d06c8-138">출력</span><span class="sxs-lookup"><span data-stu-id="d06c8-138">OUTPUTS</span></span>

## <span data-ttu-id="d06c8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d06c8-139">NOTES</span></span>

## <span data-ttu-id="d06c8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d06c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="d06c8-141">새로운 AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d06c8-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d06c8-142">제거-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d06c8-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="d06c8-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d06c8-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


