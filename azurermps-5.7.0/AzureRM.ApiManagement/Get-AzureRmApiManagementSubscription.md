---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525412"
---
# <span data-ttu-id="d19a5-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d19a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d19a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d19a5-103">구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d19a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d19a5-104">SYNTAX</span></span>

### <span data-ttu-id="d19a5-105">GetAllSubscriptions (기본값)</span><span class="sxs-lookup"><span data-stu-id="d19a5-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d19a5-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d19a5-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d19a5-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="d19a5-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d19a5-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="d19a5-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d19a5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d19a5-109">DESCRIPTION</span></span>
<span data-ttu-id="d19a5-110">**AzureRmApiManagementSubscription** cmdlet은 지정 된 구독 또는 구독이 지정 되지 않은 경우 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="d19a5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d19a5-111">EXAMPLES</span></span>

### <span data-ttu-id="d19a5-112">예제 1: 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="d19a5-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="d19a5-113">이 명령은 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="d19a5-114">예제 2: 지정 된 ID를 사용 하 여 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="d19a5-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="d19a5-115">이 명령은 ID를 기준으로 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="d19a5-116">예제 3: 사용자에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="d19a5-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="d19a5-117">이 명령은 사용자의 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="d19a5-118">예제 4: 제품에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="d19a5-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="d19a5-119">이 명령은 제품에 대 한 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="d19a5-120">변수</span><span class="sxs-lookup"><span data-stu-id="d19a5-120">PARAMETERS</span></span>

### <span data-ttu-id="d19a5-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d19a5-121">-Context</span></span>
<span data-ttu-id="d19a5-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19a5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19a5-123">-DefaultProfile</span></span>
<span data-ttu-id="d19a5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d19a5-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d19a5-125">-ProductId</span></span>
<span data-ttu-id="d19a5-126">제품 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-126">Specifies a product identifier.</span></span>
<span data-ttu-id="d19a5-127">지정 된 경우이 cmdlet은 제품 식별자를 기준으로 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19a5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d19a5-128">-SubscriptionId</span></span>
<span data-ttu-id="d19a5-129">구독 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="d19a5-130">지정 된 경우이 cmdlet은 식별자를 기준으로 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19a5-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="d19a5-131">-UserId</span></span>
<span data-ttu-id="d19a5-132">사용자 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-132">Specifies a user identifier.</span></span>
<span data-ttu-id="d19a5-133">지정 된 경우이 cmdlet은 사용자 식별자를 사용 하 여 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19a5-134">CommonParameters</span></span>
<span data-ttu-id="d19a5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19a5-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19a5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19a5-137">입력</span><span class="sxs-lookup"><span data-stu-id="d19a5-137">INPUTS</span></span>

### <span data-ttu-id="d19a5-138">않아야</span><span class="sxs-lookup"><span data-stu-id="d19a5-138">None</span></span>
<span data-ttu-id="d19a5-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d19a5-140">출력</span><span class="sxs-lookup"><span data-stu-id="d19a5-140">OUTPUTS</span></span>

### <span data-ttu-id="d19a5-141">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="d19a5-142">API Management 서비스의 구독에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="d19a5-143">IList를<ApiManagement> ServiceManagement. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="d19a5-144">API Management 서비스의 구독 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d19a5-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="d19a5-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d19a5-145">NOTES</span></span>

## <span data-ttu-id="d19a5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d19a5-146">RELATED LINKS</span></span>

[<span data-ttu-id="d19a5-147">새로운 AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d19a5-148">제거-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d19a5-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d19a5-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


