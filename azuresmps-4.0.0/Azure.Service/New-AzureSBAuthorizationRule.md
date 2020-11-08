---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045987"
---
# <span data-ttu-id="54033-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="54033-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="54033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54033-102">SYNOPSIS</span></span>
<span data-ttu-id="54033-103">새 Service Bus 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54033-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="54033-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54033-104">SYNTAX</span></span>

### <span data-ttu-id="54033-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="54033-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54033-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="54033-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54033-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54033-107">DESCRIPTION</span></span>
<span data-ttu-id="54033-108">**AzureSBAuthorizationRule** Cmdlet은 서비스 버스 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54033-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="54033-109">예제의</span><span class="sxs-lookup"><span data-stu-id="54033-109">EXAMPLES</span></span>

### <span data-ttu-id="54033-110">예제 1: 생성 된 기본 키를 사용 하 여 권한 부여 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="54033-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="54033-111">보내기 권한을 사용 하 여 네임 스페이스 수준에 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54033-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="54033-112">예제 2: 기본 키를 제공 하 여 권한 부여 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="54033-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="54033-113">모든 권한을 사용 하 여 MyEntity Queue 수준에서 새 권한 부여 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54033-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="54033-114">변수</span><span class="sxs-lookup"><span data-stu-id="54033-114">PARAMETERS</span></span>

### <span data-ttu-id="54033-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="54033-115">-EntityName</span></span>
<span data-ttu-id="54033-116">규칙을 적용할 엔터티 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54033-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="54033-117">-EntityType</span></span>
<span data-ttu-id="54033-118">엔터티 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-118">Specifies the entity type.</span></span>
<span data-ttu-id="54033-119">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="54033-119">Valid values are:</span></span>
  
- <span data-ttu-id="54033-120">전담팀</span><span class="sxs-lookup"><span data-stu-id="54033-120">Queue</span></span>
- <span data-ttu-id="54033-121">주제인</span><span class="sxs-lookup"><span data-stu-id="54033-121">Topic</span></span>
- <span data-ttu-id="54033-122">오픈</span><span class="sxs-lookup"><span data-stu-id="54033-122">Relay</span></span>
- <span data-ttu-id="54033-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="54033-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54033-124">-이름</span><span class="sxs-lookup"><span data-stu-id="54033-124">-Name</span></span>
<span data-ttu-id="54033-125">고유한 인증 규칙 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54033-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="54033-126">-Namespace</span></span>
<span data-ttu-id="54033-127">권한 부여 규칙을 적용할 네임 스페이스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="54033-128">*EntityName* 을 제공 하지 않으면 규칙은 네임 스페이스 수준에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54033-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="54033-129">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="54033-129">-Permission</span></span>
<span data-ttu-id="54033-130">권한 부여 권한 (보내기, 관리, 수신).</span><span class="sxs-lookup"><span data-stu-id="54033-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="54033-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="54033-131">-PrimaryKey</span></span>
<span data-ttu-id="54033-132">공유 액세스 서명 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="54033-133">제공 되지 않은 경우이 (가) 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54033-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="54033-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="54033-134">-Profile</span></span>
<span data-ttu-id="54033-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54033-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="54033-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54033-137">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="54033-137">-SecondaryKey</span></span>
<span data-ttu-id="54033-138">공유 액세스 서명 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="54033-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54033-139">CommonParameters</span></span>
<span data-ttu-id="54033-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54033-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54033-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54033-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54033-142">입력</span><span class="sxs-lookup"><span data-stu-id="54033-142">INPUTS</span></span>

## <span data-ttu-id="54033-143">출력</span><span class="sxs-lookup"><span data-stu-id="54033-143">OUTPUTS</span></span>

## <span data-ttu-id="54033-144">상속자</span><span class="sxs-lookup"><span data-stu-id="54033-144">NOTES</span></span>

## <span data-ttu-id="54033-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54033-145">RELATED LINKS</span></span>

[<span data-ttu-id="54033-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="54033-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="54033-147">제거-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="54033-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="54033-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="54033-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


