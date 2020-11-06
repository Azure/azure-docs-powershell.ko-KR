---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535556"
---
# <span data-ttu-id="cb093-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb093-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="cb093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb093-102">SYNOPSIS</span></span>
<span data-ttu-id="cb093-103">구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb093-104">SYNTAX</span></span>

### <span data-ttu-id="cb093-105">모든 구독 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb093-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb093-106">Subsctiption ID로 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb093-107">사용자 ID로 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb093-108">제품 ID로 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb093-109">설명은</span><span class="sxs-lookup"><span data-stu-id="cb093-109">DESCRIPTION</span></span>
<span data-ttu-id="cb093-110">**AzureRmApiManagementSubscription** cmdlet은 지정 된 구독 또는 구독이 지정 되지 않은 경우 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="cb093-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cb093-111">EXAMPLES</span></span>

### <span data-ttu-id="cb093-112">예제 1: 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="cb093-113">이 명령은 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="cb093-114">예제 2: 지정 된 ID를 사용 하 여 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="cb093-115">이 명령은 ID를 기준으로 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="cb093-116">예제 3: 사용자에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="cb093-117">이 명령은 사용자의 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="cb093-118">예제 4: 제품에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="cb093-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="cb093-119">이 명령은 제품에 대 한 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="cb093-120">변수</span><span class="sxs-lookup"><span data-stu-id="cb093-120">PARAMETERS</span></span>

### <span data-ttu-id="cb093-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="cb093-121">-Context</span></span>
<span data-ttu-id="cb093-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb093-123">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cb093-123">-ProductId</span></span>
<span data-ttu-id="cb093-124">제품 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-124">Specifies a product identifier.</span></span>
<span data-ttu-id="cb093-125">지정 된 경우이 cmdlet은 제품 식별자를 기준으로 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb093-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb093-126">-SubscriptionId</span></span>
<span data-ttu-id="cb093-127">구독 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="cb093-128">지정 된 경우이 cmdlet은 식별자를 기준으로 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb093-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="cb093-129">-UserId</span></span>
<span data-ttu-id="cb093-130">사용자 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-130">Specifies a user identifier.</span></span>
<span data-ttu-id="cb093-131">지정 된 경우이 cmdlet은 사용자 식별자를 사용 하 여 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb093-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb093-132">-DefaultProfile</span></span>
<span data-ttu-id="cb093-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb093-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb093-134">CommonParameters</span></span>
<span data-ttu-id="cb093-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb093-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb093-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb093-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb093-137">입력</span><span class="sxs-lookup"><span data-stu-id="cb093-137">INPUTS</span></span>

## <span data-ttu-id="cb093-138">출력</span><span class="sxs-lookup"><span data-stu-id="cb093-138">OUTPUTS</span></span>

### <span data-ttu-id="cb093-139">IList를<ApiManagement> ServiceManagement. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb093-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="cb093-140">상속자</span><span class="sxs-lookup"><span data-stu-id="cb093-140">NOTES</span></span>

## <span data-ttu-id="cb093-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb093-141">RELATED LINKS</span></span>

[<span data-ttu-id="cb093-142">새로운 AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb093-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="cb093-143">제거-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb093-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="cb093-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb093-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


