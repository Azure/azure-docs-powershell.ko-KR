---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045820"
---
# <span data-ttu-id="1ac6e-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ac6e-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="1ac6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac6e-103">기존 Service Bus 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="1ac6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ac6e-104">SYNTAX</span></span>

### <span data-ttu-id="1ac6e-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="1ac6e-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1ac6e-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="1ac6e-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ac6e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1ac6e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac6e-108">기존 Service Bus 권한 부여 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="1ac6e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1ac6e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ac6e-110">예제 1: 네임 스페이스 수준에서 권한 부여 규칙에 대 한 기본 키 갱신</span><span class="sxs-lookup"><span data-stu-id="1ac6e-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="1ac6e-111">기본 키가 갱신 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-111">The primary key is renewed.</span></span>

### <span data-ttu-id="1ac6e-112">예제 2: 권한 부여 규칙 권한 업데이트</span><span class="sxs-lookup"><span data-stu-id="1ac6e-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="1ac6e-113">사용 권한을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-113">Updates the permissions.</span></span>

## <span data-ttu-id="1ac6e-114">변수</span><span class="sxs-lookup"><span data-stu-id="1ac6e-114">PARAMETERS</span></span>

### <span data-ttu-id="1ac6e-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="1ac6e-115">-EntityName</span></span>
<span data-ttu-id="1ac6e-116">규칙을 적용할 엔터티 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="1ac6e-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="1ac6e-117">-EntityType</span></span>
<span data-ttu-id="1ac6e-118">엔터티 형식 (큐, 주제, 릴레이, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="1ac6e-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="1ac6e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1ac6e-119">-Name</span></span>
<span data-ttu-id="1ac6e-120">고유한 인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="1ac6e-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1ac6e-121">-Namespace</span></span>
<span data-ttu-id="1ac6e-122">권한 부여 규칙을 적용할 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="1ac6e-123">EntityName을 제공 하지 않으면 규칙은 네임 스페이스 수준에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="1ac6e-124">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="1ac6e-124">-Permission</span></span>
<span data-ttu-id="1ac6e-125">권한 부여 권한 (보내기, 관리, 수신).</span><span class="sxs-lookup"><span data-stu-id="1ac6e-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac6e-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1ac6e-126">-PrimaryKey</span></span>
<span data-ttu-id="1ac6e-127">공유 액세스 서명 기본 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="1ac6e-128">제공 되지 않은 경우이 (가) 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac6e-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="1ac6e-129">-Profile</span></span>
<span data-ttu-id="1ac6e-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ac6e-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1ac6e-132">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1ac6e-132">-SecondaryKey</span></span>
<span data-ttu-id="1ac6e-133">공유 액세스 서명 보조 키입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac6e-134">CommonParameters</span></span>
<span data-ttu-id="1ac6e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac6e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac6e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac6e-137">입력</span><span class="sxs-lookup"><span data-stu-id="1ac6e-137">INPUTS</span></span>

## <span data-ttu-id="1ac6e-138">출력</span><span class="sxs-lookup"><span data-stu-id="1ac6e-138">OUTPUTS</span></span>

## <span data-ttu-id="1ac6e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1ac6e-139">NOTES</span></span>

## <span data-ttu-id="1ac6e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ac6e-140">RELATED LINKS</span></span>

[<span data-ttu-id="1ac6e-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ac6e-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="1ac6e-142">새로운 AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ac6e-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="1ac6e-143">제거-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ac6e-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


