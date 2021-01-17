---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382383"
---
# <span data-ttu-id="7d181-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7d181-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7d181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d181-102">SYNOPSIS</span></span>
<span data-ttu-id="7d181-103">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-103">Creates a subscription.</span></span>

## <span data-ttu-id="7d181-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d181-104">SYNTAX</span></span>

### <span data-ttu-id="7d181-105">OldSubscriptionModel(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d181-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d181-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="7d181-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d181-107">설명</span><span class="sxs-lookup"><span data-stu-id="7d181-107">DESCRIPTION</span></span>
<span data-ttu-id="7d181-108">**New-AzApiManagementSubscription** cmdlet은 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="7d181-109">예제</span><span class="sxs-lookup"><span data-stu-id="7d181-109">EXAMPLES</span></span>

### <span data-ttu-id="7d181-110">예제 1: 제품 구독</span><span class="sxs-lookup"><span data-stu-id="7d181-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="7d181-111">이 명령은 기존 사용자를 제품에 구독합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="7d181-112">예제 2: 모든 API 범위에 대한 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="7d181-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="7d181-113">예제 3: 제품 범위에 대한 구독 만들기</span><span class="sxs-lookup"><span data-stu-id="7d181-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="7d181-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d181-114">PARAMETERS</span></span>

### <span data-ttu-id="7d181-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="7d181-115">-AllowTracing</span></span>
<span data-ttu-id="7d181-116">구독 수준에서 추적을 사용할 수 있는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="7d181-117">선택적 매개 변수이며 기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="7d181-117">This is optional parameter and default is $null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-118">-Context</span><span class="sxs-lookup"><span data-stu-id="7d181-118">-Context</span></span>
<span data-ttu-id="7d181-119">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="7d181-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7d181-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d181-120">-DefaultProfile</span></span>
<span data-ttu-id="7d181-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d181-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7d181-122">-Name</span></span>
<span data-ttu-id="7d181-123">구독 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-123">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7d181-124">-PrimaryKey</span></span>
<span data-ttu-id="7d181-125">구독 기본 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7d181-126">이 매개 변수를 지정하지 않으면 키가 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="7d181-127">이 매개 변수는 1~300자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-127">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7d181-128">-ProductId</span></span>
<span data-ttu-id="7d181-129">구독할 제품의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-130">-Scope</span><span class="sxs-lookup"><span data-stu-id="7d181-130">-Scope</span></span>
<span data-ttu-id="7d181-131">구독 범위는 Api Scope /apis/{apiId} 또는 제품 범위 /products/{productId} 또는 글로벌 API 범위 /apis 또는 전역 범위 /입니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="7d181-132">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7d181-133">-SecondaryKey</span></span>
<span data-ttu-id="7d181-134">구독 보조 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7d181-135">이 매개 변수는 지정되지 않은 경우 자동으로 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="7d181-136">이 매개 변수는 1~300자 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-136">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-137">-State</span><span class="sxs-lookup"><span data-stu-id="7d181-137">-State</span></span>
<span data-ttu-id="7d181-138">구독 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-138">Specifies the subscription state.</span></span>
<span data-ttu-id="7d181-139">기본값은 $Null.</span><span class="sxs-lookup"><span data-stu-id="7d181-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d181-140">-SubscriptionId</span></span>
<span data-ttu-id="7d181-141">구독 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="7d181-142">이 매개 변수는 지정되지 않은 경우 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-142">This parameter is generated if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="7d181-143">-UserId</span></span>
<span data-ttu-id="7d181-144">구독자 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d181-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d181-145">CommonParameters</span></span>
<span data-ttu-id="7d181-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d181-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d181-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d181-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d181-148">입력</span><span class="sxs-lookup"><span data-stu-id="7d181-148">INPUTS</span></span>

### <span data-ttu-id="7d181-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7d181-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7d181-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7d181-150">System.String</span></span>

### <span data-ttu-id="7d181-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7d181-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7d181-152">출력</span><span class="sxs-lookup"><span data-stu-id="7d181-152">OUTPUTS</span></span>

### <span data-ttu-id="7d181-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7d181-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7d181-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d181-154">NOTES</span></span>

## <span data-ttu-id="7d181-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d181-155">RELATED LINKS</span></span>

[<span data-ttu-id="7d181-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7d181-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7d181-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7d181-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="7d181-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7d181-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


