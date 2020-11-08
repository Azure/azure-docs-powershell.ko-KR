---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046131"
---
# <span data-ttu-id="299f0-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="299f0-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="299f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="299f0-102">SYNOPSIS</span></span>
<span data-ttu-id="299f0-103">기존 Service Bus 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="299f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="299f0-104">SYNTAX</span></span>

### <span data-ttu-id="299f0-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="299f0-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="299f0-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="299f0-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="299f0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="299f0-107">DESCRIPTION</span></span>
<span data-ttu-id="299f0-108">기존 Service Bus 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="299f0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="299f0-109">EXAMPLES</span></span>

### <span data-ttu-id="299f0-110">예제 1: 네임 스페이스 수준에서 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="299f0-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="299f0-111">MyNamespace에서 권한 부여 규칙 MyRule을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="299f0-112">예제 2: 큐에 대 한 권한 부여 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="299f0-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="299f0-113">MyNamespace의 Myrule Queue에 대해 MyRule 이라는 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="299f0-114">변수</span><span class="sxs-lookup"><span data-stu-id="299f0-114">PARAMETERS</span></span>

### <span data-ttu-id="299f0-115">-EntityName</span><span class="sxs-lookup"><span data-stu-id="299f0-115">-EntityName</span></span>
<span data-ttu-id="299f0-116">규칙을 적용할 엔터티 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="299f0-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="299f0-117">-EntityType</span></span>
<span data-ttu-id="299f0-118">엔터티 형식 (큐, 주제, 릴레이, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="299f0-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="299f0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="299f0-119">-Name</span></span>
<span data-ttu-id="299f0-120">고유한 인증 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="299f0-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="299f0-121">-Namespace</span></span>
<span data-ttu-id="299f0-122">권한 부여 규칙을 적용할 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="299f0-123">EntityName을 제공 하지 않으면 규칙은 네임 스페이스 수준에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="299f0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="299f0-124">-PassThru</span></span>
<span data-ttu-id="299f0-125">이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="299f0-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="299f0-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="299f0-127">-Profile</span></span>
<span data-ttu-id="299f0-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="299f0-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="299f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299f0-130">CommonParameters</span></span>
<span data-ttu-id="299f0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="299f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299f0-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299f0-133">입력</span><span class="sxs-lookup"><span data-stu-id="299f0-133">INPUTS</span></span>

## <span data-ttu-id="299f0-134">출력</span><span class="sxs-lookup"><span data-stu-id="299f0-134">OUTPUTS</span></span>

## <span data-ttu-id="299f0-135">상속자</span><span class="sxs-lookup"><span data-stu-id="299f0-135">NOTES</span></span>

## <span data-ttu-id="299f0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="299f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="299f0-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="299f0-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="299f0-138">새로운 AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="299f0-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="299f0-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="299f0-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


