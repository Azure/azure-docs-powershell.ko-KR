---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187713"
---
# <span data-ttu-id="8a7d7-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8a7d7-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="8a7d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7d7-103">구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-103">Gets subscriptions.</span></span>

## <span data-ttu-id="8a7d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a7d7-104">SYNTAX</span></span>

### <span data-ttu-id="8a7d7-105">GetAllSubscriptions(기본값)</span><span class="sxs-lookup"><span data-stu-id="8a7d7-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a7d7-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a7d7-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="8a7d7-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a7d7-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a7d7-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a7d7-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="8a7d7-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a7d7-111">설명</span><span class="sxs-lookup"><span data-stu-id="8a7d7-111">DESCRIPTION</span></span>
<span data-ttu-id="8a7d7-112">**Get-AzApiManagementSubscription** cmdlet은 지정된 구독 또는 구독이 지정되지 않은 경우 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="8a7d7-113">키는 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-113">Keys will not be included into result details.</span></span> <span data-ttu-id="8a7d7-114">키를 얻습니다. **Get-AzApiManagementSubscriptionKey를 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="8a7d7-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="8a7d7-115">예제</span><span class="sxs-lookup"><span data-stu-id="8a7d7-115">EXAMPLES</span></span>

### <span data-ttu-id="8a7d7-116">예제 1: 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="8a7d7-117">이 명령은 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="8a7d7-118">예제 2: 지정된 ID로 구독을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="8a7d7-119">이 명령은 ID로 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="8a7d7-120">예제 3: 사용자에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="8a7d7-121">이 명령은 사용자의 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="8a7d7-122">예제 4: 제품에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="8a7d7-123">이 명령은 제품에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="8a7d7-124">예제 5: 범위에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="8a7d7-125">이 명령은 전역 API 범위에 대해 구성된 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="8a7d7-126">예제 6: 제품 및 사용자 범위에 대한 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="8a7d7-127">이 명령은 전역 API 범위에 대해 구성된 모든 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="8a7d7-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a7d7-128">PARAMETERS</span></span>

### <span data-ttu-id="8a7d7-129">-Context</span><span class="sxs-lookup"><span data-stu-id="8a7d7-129">-Context</span></span>
<span data-ttu-id="8a7d7-130">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="8a7d7-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8a7d7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a7d7-131">-DefaultProfile</span></span>
<span data-ttu-id="8a7d7-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a7d7-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-133">-ProductId</span></span>
<span data-ttu-id="8a7d7-134">제품 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-134">Specifies a product identifier.</span></span>
<span data-ttu-id="8a7d7-135">지정된 경우 이 cmdlet은 제품 식별자에 의해 모든 구독을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="8a7d7-136">-Scope</span><span class="sxs-lookup"><span data-stu-id="8a7d7-136">-Scope</span></span>
<span data-ttu-id="8a7d7-137">범위 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-137">Scope identifier.</span></span> <span data-ttu-id="8a7d7-138">구독 범위( Api Scope /apis/{apiId} 또는 제품 범위 /products/{productId} 또는 글로벌 API 범위 /apis 또는 전역 범위 /)입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="8a7d7-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-139">-SubscriptionId</span></span>
<span data-ttu-id="8a7d7-140">구독 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="8a7d7-141">지정된 경우 이 cmdlet은 식별자에 의해 구독을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="8a7d7-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="8a7d7-142">-UserId</span></span>
<span data-ttu-id="8a7d7-143">사용자 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-143">Specifies a user identifier.</span></span>
<span data-ttu-id="8a7d7-144">지정된 경우 이 cmdlet은 사용자 식별자에 의해 모든 구독을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="8a7d7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7d7-145">CommonParameters</span></span>
<span data-ttu-id="8a7d7-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7d7-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a7d7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7d7-148">입력</span><span class="sxs-lookup"><span data-stu-id="8a7d7-148">INPUTS</span></span>

### <span data-ttu-id="8a7d7-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8a7d7-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a7d7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8a7d7-150">System.String</span></span>

## <span data-ttu-id="8a7d7-151">출력</span><span class="sxs-lookup"><span data-stu-id="8a7d7-151">OUTPUTS</span></span>

### <span data-ttu-id="8a7d7-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8a7d7-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="8a7d7-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a7d7-153">NOTES</span></span>

## <span data-ttu-id="8a7d7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a7d7-154">RELATED LINKS</span></span>

[<span data-ttu-id="8a7d7-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8a7d7-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="8a7d7-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8a7d7-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="8a7d7-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8a7d7-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


