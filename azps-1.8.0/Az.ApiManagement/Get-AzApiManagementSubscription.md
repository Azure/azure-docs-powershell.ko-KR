---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689129"
---
# <span data-ttu-id="c4bfd-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c4bfd-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="c4bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bfd-103">구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-103">Gets subscriptions.</span></span>

## <span data-ttu-id="c4bfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4bfd-104">SYNTAX</span></span>

### <span data-ttu-id="c4bfd-105">GetAllSubscriptions (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4bfd-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4bfd-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4bfd-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4bfd-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4bfd-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c4bfd-109">DESCRIPTION</span></span>
<span data-ttu-id="c4bfd-110">**AzApiManagementSubscription** cmdlet은 지정 된 구독 또는 구독이 지정 되지 않은 경우 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="c4bfd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c4bfd-111">EXAMPLES</span></span>

### <span data-ttu-id="c4bfd-112">예제 1: 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="c4bfd-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="c4bfd-113">이 명령은 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="c4bfd-114">예제 2: 지정 된 ID를 사용 하 여 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="c4bfd-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="c4bfd-115">이 명령은 ID를 기준으로 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="c4bfd-116">예제 3: 사용자에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="c4bfd-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="c4bfd-117">이 명령은 사용자의 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="c4bfd-118">예제 4: 제품에 대 한 모든 구독 가져오기</span><span class="sxs-lookup"><span data-stu-id="c4bfd-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="c4bfd-119">이 명령은 제품에 대 한 모든 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="c4bfd-120">변수</span><span class="sxs-lookup"><span data-stu-id="c4bfd-120">PARAMETERS</span></span>

### <span data-ttu-id="c4bfd-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c4bfd-121">-Context</span></span>
<span data-ttu-id="c4bfd-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4bfd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bfd-123">-DefaultProfile</span></span>
<span data-ttu-id="c4bfd-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4bfd-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-125">-ProductId</span></span>
<span data-ttu-id="c4bfd-126">제품 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-126">Specifies a product identifier.</span></span>
<span data-ttu-id="c4bfd-127">지정 된 경우이 cmdlet은 제품 식별자를 기준으로 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="c4bfd-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-128">-SubscriptionId</span></span>
<span data-ttu-id="c4bfd-129">구독 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="c4bfd-130">지정 된 경우이 cmdlet은 식별자를 기준으로 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="c4bfd-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="c4bfd-131">-UserId</span></span>
<span data-ttu-id="c4bfd-132">사용자 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-132">Specifies a user identifier.</span></span>
<span data-ttu-id="c4bfd-133">지정 된 경우이 cmdlet은 사용자 식별자를 사용 하 여 모든 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="c4bfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bfd-134">CommonParameters</span></span>
<span data-ttu-id="c4bfd-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4bfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bfd-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4bfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bfd-137">입력</span><span class="sxs-lookup"><span data-stu-id="c4bfd-137">INPUTS</span></span>

### <span data-ttu-id="c4bfd-138">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4bfd-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4bfd-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4bfd-139">System.String</span></span>

## <span data-ttu-id="c4bfd-140">출력</span><span class="sxs-lookup"><span data-stu-id="c4bfd-140">OUTPUTS</span></span>

### <span data-ttu-id="c4bfd-141">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c4bfd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c4bfd-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c4bfd-142">NOTES</span></span>

## <span data-ttu-id="c4bfd-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4bfd-143">RELATED LINKS</span></span>

[<span data-ttu-id="c4bfd-144">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c4bfd-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="c4bfd-145">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c4bfd-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="c4bfd-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c4bfd-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


