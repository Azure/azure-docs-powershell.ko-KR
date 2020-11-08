---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048560"
---
# <span data-ttu-id="d1acb-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="d1acb-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="d1acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1acb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1acb-103">구독 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-103">Gets subscription keys.</span></span>

## <span data-ttu-id="d1acb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1acb-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1acb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1acb-105">DESCRIPTION</span></span>
<span data-ttu-id="d1acb-106">**AzApiManagementSubscriptionKey** cmdlet은 지정 된 구독의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="d1acb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d1acb-107">EXAMPLES</span></span>

### <span data-ttu-id="d1acb-108">예제 1: 지정 된 ID를 사용 하 여 구독 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1acb-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="d1acb-109">이 명령은 ID를 기준으로 구독을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="d1acb-110">변수</span><span class="sxs-lookup"><span data-stu-id="d1acb-110">PARAMETERS</span></span>

### <span data-ttu-id="d1acb-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d1acb-111">-Context</span></span>
<span data-ttu-id="d1acb-112">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1acb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1acb-113">-DefaultProfile</span></span>
<span data-ttu-id="d1acb-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1acb-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1acb-115">-SubscriptionId</span></span>
<span data-ttu-id="d1acb-116">구독 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="d1acb-117">지정 된 경우이 cmdlet은 식별자를 기준으로 구독을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="d1acb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1acb-118">CommonParameters</span></span>
<span data-ttu-id="d1acb-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1acb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1acb-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1acb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1acb-121">입력</span><span class="sxs-lookup"><span data-stu-id="d1acb-121">INPUTS</span></span>

### <span data-ttu-id="d1acb-122">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1acb-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1acb-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1acb-123">System.String</span></span>

## <span data-ttu-id="d1acb-124">출력</span><span class="sxs-lookup"><span data-stu-id="d1acb-124">OUTPUTS</span></span>

### <span data-ttu-id="d1acb-125">ApiManagement. ServiceManagement. \ PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="d1acb-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="d1acb-126">상속자</span><span class="sxs-lookup"><span data-stu-id="d1acb-126">NOTES</span></span>

## <span data-ttu-id="d1acb-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1acb-127">RELATED LINKS</span></span>

[<span data-ttu-id="d1acb-128">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1acb-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="d1acb-129">새로운 AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1acb-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="d1acb-130">제거-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1acb-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="d1acb-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d1acb-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


