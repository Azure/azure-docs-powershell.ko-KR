---
external help file: Microsoft.Azure.Commands.Subscription.dll-Help.xml
Module Name: AzureRM.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription/new-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
ms.openlocfilehash: cc88f762f1e965eb4e46462f7d43074fa3fe4646
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536484"
---
# <span data-ttu-id="edc62-101">New-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="edc62-101">New-AzureRmSubscription</span></span>

## <span data-ttu-id="edc62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc62-102">SYNOPSIS</span></span>
<span data-ttu-id="edc62-103">Azure 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-103">Creates an Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edc62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="edc62-104">SYNTAX</span></span>

```
New-AzureRmSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edc62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="edc62-105">DESCRIPTION</span></span>
<span data-ttu-id="edc62-106">**새 AzureRmSubscription** Cmdlet은 Azure 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-106">The **New-AzureRmSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="edc62-107">예제의</span><span class="sxs-lookup"><span data-stu-id="edc62-107">EXAMPLES</span></span>

### <span data-ttu-id="edc62-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="edc62-108">Example 1</span></span>
```
PS C:\> New-AzureRmSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzureRmEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="edc62-109">지정 된 제공 형식의 등록 계정으로 Azure 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="edc62-110">변수</span><span class="sxs-lookup"><span data-stu-id="edc62-110">PARAMETERS</span></span>

### <span data-ttu-id="edc62-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="edc62-111">-AsJob</span></span>
<span data-ttu-id="edc62-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="edc62-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="edc62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc62-113">-DefaultProfile</span></span>
<span data-ttu-id="edc62-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc62-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="edc62-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="edc62-116">구독을 만들 때 사용할 등록 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-117">-이름</span><span class="sxs-lookup"><span data-stu-id="edc62-117">-Name</span></span>
<span data-ttu-id="edc62-118">만들 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="edc62-119">-OfferType</span></span>
<span data-ttu-id="edc62-120">구독을 만들 때 사용할 제공의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-121">-소유자 Applicationid</span><span class="sxs-lookup"><span data-stu-id="edc62-121">-OwnerApplicationId</span></span>
<span data-ttu-id="edc62-122">구독에 소유자 액세스 권한을 부여할 앱 SPN</span><span class="sxs-lookup"><span data-stu-id="edc62-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-123">-소유자 Id</span><span class="sxs-lookup"><span data-stu-id="edc62-123">-OwnerObjectId</span></span>
<span data-ttu-id="edc62-124">구독에 대 한 소유자 액세스 권한을 부여 받을 사용자 또는 그룹 개체 id (들)입니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="edc62-125">-OwnerSignInName</span></span>
<span data-ttu-id="edc62-126">사용자에 게 구독에 대 한 소유자 액세스 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc62-127">-확인</span><span class="sxs-lookup"><span data-stu-id="edc62-127">-Confirm</span></span>
<span data-ttu-id="edc62-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc62-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc62-129">-WhatIf</span></span>
<span data-ttu-id="edc62-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edc62-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc62-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc62-132">CommonParameters</span></span>
<span data-ttu-id="edc62-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="edc62-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc62-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc62-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc62-135">입력</span><span class="sxs-lookup"><span data-stu-id="edc62-135">INPUTS</span></span>

### <span data-ttu-id="edc62-136">않아야</span><span class="sxs-lookup"><span data-stu-id="edc62-136">None</span></span>

## <span data-ttu-id="edc62-137">출력</span><span class="sxs-lookup"><span data-stu-id="edc62-137">OUTPUTS</span></span>

### <span data-ttu-id="edc62-138">PSAzureSubscription에 대 한.</span><span class="sxs-lookup"><span data-stu-id="edc62-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="edc62-139">상속자</span><span class="sxs-lookup"><span data-stu-id="edc62-139">NOTES</span></span>

## <span data-ttu-id="edc62-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edc62-140">RELATED LINKS</span></span>
