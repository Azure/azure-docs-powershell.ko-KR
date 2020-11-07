---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869494"
---
# <span data-ttu-id="b91a7-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b91a7-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="b91a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b91a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b91a7-103">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-103">Creates a subscription.</span></span>

## <span data-ttu-id="b91a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b91a7-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b91a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b91a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b91a7-106">**새 AzApiManagementSubscription** cmdlet은 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="b91a7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b91a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b91a7-108">예제 1: 제품에 사용자 가입</span><span class="sxs-lookup"><span data-stu-id="b91a7-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="b91a7-109">이 명령은 기존 사용자를 제품에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="b91a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="b91a7-110">PARAMETERS</span></span>

### <span data-ttu-id="b91a7-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b91a7-111">-Context</span></span>
<span data-ttu-id="b91a7-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b91a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91a7-113">-DefaultProfile</span></span>
<span data-ttu-id="b91a7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b91a7-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b91a7-115">-Name</span></span>
<span data-ttu-id="b91a7-116">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="b91a7-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b91a7-117">-PrimaryKey</span></span>
<span data-ttu-id="b91a7-118">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b91a7-119">이 매개 변수를 지정 하지 않으면 키가 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="b91a7-120">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b91a7-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b91a7-121">-ProductId</span></span>
<span data-ttu-id="b91a7-122">구독할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="b91a7-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b91a7-123">-SecondaryKey</span></span>
<span data-ttu-id="b91a7-124">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b91a7-125">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="b91a7-126">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b91a7-127">-상태</span><span class="sxs-lookup"><span data-stu-id="b91a7-127">-State</span></span>
<span data-ttu-id="b91a7-128">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-128">Specifies the subscription state.</span></span>
<span data-ttu-id="b91a7-129">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="b91a7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b91a7-130">-SubscriptionId</span></span>
<span data-ttu-id="b91a7-131">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="b91a7-132">이 매개 변수는 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="b91a7-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="b91a7-133">-UserId</span></span>
<span data-ttu-id="b91a7-134">구독자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="b91a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91a7-135">CommonParameters</span></span>
<span data-ttu-id="b91a7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b91a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91a7-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91a7-138">입력</span><span class="sxs-lookup"><span data-stu-id="b91a7-138">INPUTS</span></span>

### <span data-ttu-id="b91a7-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b91a7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b91a7-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b91a7-140">System.String</span></span>

### <span data-ttu-id="b91a7-141">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementSubscriptionState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b91a7-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b91a7-142">출력</span><span class="sxs-lookup"><span data-stu-id="b91a7-142">OUTPUTS</span></span>

### <span data-ttu-id="b91a7-143">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b91a7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="b91a7-144">상속자</span><span class="sxs-lookup"><span data-stu-id="b91a7-144">NOTES</span></span>

## <span data-ttu-id="b91a7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b91a7-145">RELATED LINKS</span></span>

[<span data-ttu-id="b91a7-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b91a7-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="b91a7-147">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b91a7-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="b91a7-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b91a7-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


