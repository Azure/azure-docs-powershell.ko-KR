---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523555"
---
# <span data-ttu-id="3f4ae-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3f4ae-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="3f4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4ae-103">Cmdlet에 대 한 테 넌 트, 구독 및 환경을 현재 세션에서 사용할 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="3f4ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f4ae-104">SYNTAX</span></span>

### <span data-ttu-id="3f4ae-105">SubscriptionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f4ae-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4ae-106">상황별</span><span class="sxs-lookup"><span data-stu-id="3f4ae-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4ae-107">Id</span><span class="sxs-lookup"><span data-stu-id="3f4ae-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4ae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3f4ae-108">DESCRIPTION</span></span>
<span data-ttu-id="3f4ae-109">Set-AzureRmContext cmdlet은 현재 세션에서 실행 하는 cmdlet에 대 한 인증 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="3f4ae-110">컨텍스트에는 테 넌 트, 구독 및 환경 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="3f4ae-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3f4ae-111">EXAMPLES</span></span>

### <span data-ttu-id="3f4ae-112">예제 1: 구독 컨텍스트 설정</span><span class="sxs-lookup"><span data-stu-id="3f4ae-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="3f4ae-113">이 명령은 지정 된 구독을 사용 하도록 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="3f4ae-114">변수</span><span class="sxs-lookup"><span data-stu-id="3f4ae-114">PARAMETERS</span></span>

### <span data-ttu-id="3f4ae-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3f4ae-115">-Context</span></span>
<span data-ttu-id="3f4ae-116">현재 세션에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f4ae-117">-SubscriptionId</span></span>
<span data-ttu-id="3f4ae-118">이 cmdlet이 현재 세션에 대해 설정 하는 컨텍스트에 대 한 구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f4ae-119">-SubscriptionName</span></span>
<span data-ttu-id="3f4ae-120">이 cmdlet이 현재 세션에 대해 설정 하는 컨텍스트에 대 한 구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3f4ae-121">-TenantId</span></span>
<span data-ttu-id="3f4ae-122">이 cmdlet이 현재 세션에 대해 설정 하는 컨텍스트에 대 한 테 넌 트의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3f4ae-123">-Confirm</span></span>
<span data-ttu-id="3f4ae-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4ae-125">-WhatIf</span></span>
<span data-ttu-id="3f4ae-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f4ae-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4ae-128">CommonParameters</span></span>
<span data-ttu-id="3f4ae-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f4ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4ae-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4ae-131">입력</span><span class="sxs-lookup"><span data-stu-id="3f4ae-131">INPUTS</span></span>

## <span data-ttu-id="3f4ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="3f4ae-132">OUTPUTS</span></span>

### <span data-ttu-id="3f4ae-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3f4ae-133">PSAzureContext</span></span>

## <span data-ttu-id="3f4ae-134">상속자</span><span class="sxs-lookup"><span data-stu-id="3f4ae-134">NOTES</span></span>

## <span data-ttu-id="3f4ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f4ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f4ae-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="3f4ae-136">Get-AzureRMContext</span></span>]()

