---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333146"
---
# <span data-ttu-id="75917-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="75917-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="75917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75917-102">SYNOPSIS</span></span>
<span data-ttu-id="75917-103">구독 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75917-103">Gets subscription keys.</span></span>

## <span data-ttu-id="75917-104">구문</span><span class="sxs-lookup"><span data-stu-id="75917-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75917-105">설명</span><span class="sxs-lookup"><span data-stu-id="75917-105">DESCRIPTION</span></span>
<span data-ttu-id="75917-106">**Get-AzApiManagementSubscriptionKey** cmdlet은 지정된 구독의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75917-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="75917-107">예제</span><span class="sxs-lookup"><span data-stu-id="75917-107">EXAMPLES</span></span>

### <span data-ttu-id="75917-108">예제 1: 지정된 ID를 사용하여 구독 키 얻기</span><span class="sxs-lookup"><span data-stu-id="75917-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="75917-109">이 명령은 ID로 구독을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="75917-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="75917-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75917-110">PARAMETERS</span></span>

### <span data-ttu-id="75917-111">-Context</span><span class="sxs-lookup"><span data-stu-id="75917-111">-Context</span></span>
<span data-ttu-id="75917-112">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="75917-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="75917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75917-113">-DefaultProfile</span></span>
<span data-ttu-id="75917-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75917-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75917-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75917-115">-SubscriptionId</span></span>
<span data-ttu-id="75917-116">구독 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="75917-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="75917-117">지정된 경우 이 cmdlet은 식별자에 의해 구독을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="75917-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="75917-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75917-118">CommonParameters</span></span>
<span data-ttu-id="75917-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75917-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75917-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75917-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75917-121">입력</span><span class="sxs-lookup"><span data-stu-id="75917-121">INPUTS</span></span>

### <span data-ttu-id="75917-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75917-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75917-123">System.String</span><span class="sxs-lookup"><span data-stu-id="75917-123">System.String</span></span>

## <span data-ttu-id="75917-124">출력</span><span class="sxs-lookup"><span data-stu-id="75917-124">OUTPUTS</span></span>

### <span data-ttu-id="75917-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="75917-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="75917-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75917-126">NOTES</span></span>

## <span data-ttu-id="75917-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75917-127">RELATED LINKS</span></span>

[<span data-ttu-id="75917-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="75917-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="75917-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="75917-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="75917-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="75917-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="75917-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="75917-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


