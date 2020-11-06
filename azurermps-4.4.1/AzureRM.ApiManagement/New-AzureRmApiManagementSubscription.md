---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535531"
---
# <span data-ttu-id="4b27d-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b27d-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="4b27d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b27d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b27d-103">구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b27d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b27d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b27d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b27d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b27d-106">**새 AzureRmApiManagementSubscription** cmdlet은 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="4b27d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4b27d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b27d-108">예제 1: 제품에 사용자 가입</span><span class="sxs-lookup"><span data-stu-id="4b27d-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="4b27d-109">이 명령은 기존 사용자를 제품에 가입 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="4b27d-110">변수</span><span class="sxs-lookup"><span data-stu-id="4b27d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b27d-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4b27d-111">-Context</span></span>
<span data-ttu-id="4b27d-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4b27d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4b27d-113">-Name</span></span>
<span data-ttu-id="4b27d-114">구독 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="4b27d-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4b27d-115">-PrimaryKey</span></span>
<span data-ttu-id="4b27d-116">구독 기본 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="4b27d-117">이 매개 변수를 지정 하지 않으면 키가 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="4b27d-118">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4b27d-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4b27d-119">-ProductId</span></span>
<span data-ttu-id="4b27d-120">구독할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="4b27d-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4b27d-121">-SecondaryKey</span></span>
<span data-ttu-id="4b27d-122">구독 보조 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="4b27d-123">이 매개 변수는 지정 되지 않은 경우 자동으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="4b27d-124">이 매개 변수는 1 ~ 300 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="4b27d-125">-상태</span><span class="sxs-lookup"><span data-stu-id="4b27d-125">-State</span></span>
<span data-ttu-id="4b27d-126">구독 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-126">Specifies the subscription state.</span></span>
<span data-ttu-id="4b27d-127">기본값은 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="4b27d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b27d-128">-SubscriptionId</span></span>
<span data-ttu-id="4b27d-129">구독 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="4b27d-130">이 매개 변수는 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="4b27d-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="4b27d-131">-UserId</span></span>
<span data-ttu-id="4b27d-132">구독자 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="4b27d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b27d-133">-DefaultProfile</span></span>
<span data-ttu-id="4b27d-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b27d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b27d-135">CommonParameters</span></span>
<span data-ttu-id="4b27d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b27d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b27d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b27d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b27d-138">입력</span><span class="sxs-lookup"><span data-stu-id="4b27d-138">INPUTS</span></span>

## <span data-ttu-id="4b27d-139">출력</span><span class="sxs-lookup"><span data-stu-id="4b27d-139">OUTPUTS</span></span>

### <span data-ttu-id="4b27d-140">ApiManagement. ServiceManagement. \ PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b27d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="4b27d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="4b27d-141">NOTES</span></span>

## <span data-ttu-id="4b27d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b27d-142">RELATED LINKS</span></span>

[<span data-ttu-id="4b27d-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b27d-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4b27d-144">제거-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b27d-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="4b27d-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4b27d-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


