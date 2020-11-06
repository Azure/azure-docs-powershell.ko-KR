---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524728"
---
# <span data-ttu-id="4cbc1-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4cbc1-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="4cbc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbc1-103">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cbc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cbc1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cbc1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cbc1-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbc1-106">**새 AzureRmApiManagementSubscription** cmdlet은 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="4cbc1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4cbc1-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbc1-108">예제 1: 제품에 사용자 가입</span><span class="sxs-lookup"><span data-stu-id="4cbc1-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="4cbc1-109">이 명령은 기존 사용자를 제품에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="4cbc1-110">변수</span><span class="sxs-lookup"><span data-stu-id="4cbc1-110">PARAMETERS</span></span>

### <span data-ttu-id="4cbc1-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4cbc1-111">-Context</span></span>
<span data-ttu-id="4cbc1-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4cbc1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbc1-113">-DefaultProfile</span></span>
<span data-ttu-id="4cbc1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbc1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4cbc1-115">-Name</span></span>
<span data-ttu-id="4cbc1-116">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="4cbc1-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4cbc1-117">-PrimaryKey</span></span>
<span data-ttu-id="4cbc1-118">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4cbc1-119">이 매개 변수를 지정 하지 않으면 키가 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="4cbc1-120">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4cbc1-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4cbc1-121">-ProductId</span></span>
<span data-ttu-id="4cbc1-122">구독할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="4cbc1-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4cbc1-123">-SecondaryKey</span></span>
<span data-ttu-id="4cbc1-124">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4cbc1-125">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="4cbc1-126">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4cbc1-127">-상태</span><span class="sxs-lookup"><span data-stu-id="4cbc1-127">-State</span></span>
<span data-ttu-id="4cbc1-128">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-128">Specifies the subscription state.</span></span>
<span data-ttu-id="4cbc1-129">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="4cbc1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cbc1-130">-SubscriptionId</span></span>
<span data-ttu-id="4cbc1-131">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="4cbc1-132">이 매개 변수는 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="4cbc1-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="4cbc1-133">-UserId</span></span>
<span data-ttu-id="4cbc1-134">구독자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="4cbc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbc1-135">CommonParameters</span></span>
<span data-ttu-id="4cbc1-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbc1-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbc1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbc1-138">입력</span><span class="sxs-lookup"><span data-stu-id="4cbc1-138">INPUTS</span></span>

### <span data-ttu-id="4cbc1-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cbc1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cbc1-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4cbc1-140">System.String</span></span>

### <span data-ttu-id="4cbc1-141">시스템 Null 허용 ' 1 [[ApiManagement, ServiceManagement. PsApiManagementSubscriptionState, Microsoft Azure. ServiceManagement, Version = 6.1.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4cbc1-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4cbc1-142">출력</span><span class="sxs-lookup"><span data-stu-id="4cbc1-142">OUTPUTS</span></span>

### <span data-ttu-id="4cbc1-143">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4cbc1-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="4cbc1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4cbc1-144">NOTES</span></span>

## <span data-ttu-id="4cbc1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cbc1-145">RELATED LINKS</span></span>

[<span data-ttu-id="4cbc1-146">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4cbc1-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4cbc1-147">제거-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4cbc1-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4cbc1-148">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4cbc1-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


