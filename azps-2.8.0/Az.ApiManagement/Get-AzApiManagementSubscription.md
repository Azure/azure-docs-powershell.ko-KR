---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698094"
---
# <span data-ttu-id="77dbb-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="77dbb-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="77dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="77dbb-103">구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-103">Gets subscriptions.</span></span>

## <span data-ttu-id="77dbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77dbb-104">SYNTAX</span></span>

### <span data-ttu-id="77dbb-105">GetAllSubscriptions (기본값)</span><span class="sxs-lookup"><span data-stu-id="77dbb-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77dbb-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77dbb-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dbb-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="77dbb-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dbb-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="77dbb-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dbb-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="77dbb-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77dbb-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="77dbb-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77dbb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="77dbb-111">DESCRIPTION</span></span>
<span data-ttu-id="77dbb-112">**AzApiManagementSubscription** cmdlet은 지정 된 구독 또는 구독이 지정 되지 않은 경우 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="77dbb-113">예제의</span><span class="sxs-lookup"><span data-stu-id="77dbb-113">EXAMPLES</span></span>

### <span data-ttu-id="77dbb-114">예제 1: 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="77dbb-115">이 명령은 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="77dbb-116">예제 2: 지정 된 ID를 사용 하 여 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="77dbb-117">이 명령은 ID를 기준으로 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="77dbb-118">예제 3: 사용자에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="77dbb-119">이 명령은 사용자의 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="77dbb-120">예제 4: 제품에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="77dbb-121">이 명령은 제품에 대 한 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="77dbb-122">예제 5: 범위에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="77dbb-123">이 명령은 전역 api 범위에 대해 구성 된 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="77dbb-124">예제 5: 제품 및 사용자 범위에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="77dbb-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="77dbb-125">이 명령은 전역 api 범위에 대해 구성 된 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="77dbb-126">변수</span><span class="sxs-lookup"><span data-stu-id="77dbb-126">PARAMETERS</span></span>

### <span data-ttu-id="77dbb-127">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="77dbb-127">-Context</span></span>
<span data-ttu-id="77dbb-128">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dbb-129">-DefaultProfile</span></span>
<span data-ttu-id="77dbb-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77dbb-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="77dbb-131">-ProductId</span></span>
<span data-ttu-id="77dbb-132">제품 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-132">Specifies a product identifier.</span></span>
<span data-ttu-id="77dbb-133">지정 된 경우이 cmdlet은 제품 식별자를 기준으로 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbb-134">-범위</span><span class="sxs-lookup"><span data-stu-id="77dbb-134">-Scope</span></span>
<span data-ttu-id="77dbb-135">범위 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-135">Scope identifier.</span></span> <span data-ttu-id="77dbb-136">Api 범위/Apis/{apiid} 또는 Product Scope/products/{productId} 또는 전역 범위/전역 scope/api 인지 여부에 관계 없이 구독의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbb-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77dbb-137">-SubscriptionId</span></span>
<span data-ttu-id="77dbb-138">구독 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="77dbb-139">지정 된 경우이 cmdlet은 식별자를 기준으로 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbb-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="77dbb-140">-UserId</span></span>
<span data-ttu-id="77dbb-141">사용자 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-141">Specifies a user identifier.</span></span>
<span data-ttu-id="77dbb-142">지정 된 경우이 cmdlet은 사용자 식별자를 사용 하 여 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77dbb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dbb-143">CommonParameters</span></span>
<span data-ttu-id="77dbb-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77dbb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dbb-145">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77dbb-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dbb-146">입력</span><span class="sxs-lookup"><span data-stu-id="77dbb-146">INPUTS</span></span>

### <span data-ttu-id="77dbb-147">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77dbb-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="77dbb-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77dbb-148">System.String</span></span>

## <span data-ttu-id="77dbb-149">출력</span><span class="sxs-lookup"><span data-stu-id="77dbb-149">OUTPUTS</span></span>

### <span data-ttu-id="77dbb-150">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="77dbb-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="77dbb-151">상속자</span><span class="sxs-lookup"><span data-stu-id="77dbb-151">NOTES</span></span>

## <span data-ttu-id="77dbb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77dbb-152">RELATED LINKS</span></span>

[<span data-ttu-id="77dbb-153">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="77dbb-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="77dbb-154">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="77dbb-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="77dbb-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="77dbb-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


