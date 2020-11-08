---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214643"
---
# <span data-ttu-id="7566b-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7566b-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="7566b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7566b-102">SYNOPSIS</span></span>
<span data-ttu-id="7566b-103">모든 또는 특정 API 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="7566b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7566b-104">SYNTAX</span></span>

### <span data-ttu-id="7566b-105">GetAllGateways (기본값)</span><span class="sxs-lookup"><span data-stu-id="7566b-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7566b-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="7566b-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7566b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7566b-107">DESCRIPTION</span></span>
<span data-ttu-id="7566b-108">**AzApiManagementGateway** cmdlet은 모든 또는 특정 API 관리 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="7566b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7566b-109">EXAMPLES</span></span>

### <span data-ttu-id="7566b-110">예제 1: 모든 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="7566b-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="7566b-111">이 명령은 모든 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-111">This command gets all gateways.</span></span>

### <span data-ttu-id="7566b-112">예제 2: ID로 게이트웨이 가져오기</span><span class="sxs-lookup"><span data-stu-id="7566b-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="7566b-113">이 명령은 게이트웨이 0123456789를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="7566b-114">변수</span><span class="sxs-lookup"><span data-stu-id="7566b-114">PARAMETERS</span></span>

### <span data-ttu-id="7566b-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7566b-115">-Context</span></span>
<span data-ttu-id="7566b-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7566b-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="7566b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7566b-118">-DefaultProfile</span></span>
<span data-ttu-id="7566b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7566b-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7566b-120">-GatewayId</span></span>
<span data-ttu-id="7566b-121">게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-121">Identifier of a gateway.</span></span>
<span data-ttu-id="7566b-122">지정 된 경우 식별자를 사용 하 여 게이트웨이를 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7566b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7566b-123">CommonParameters</span></span>
<span data-ttu-id="7566b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7566b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7566b-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7566b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7566b-126">입력</span><span class="sxs-lookup"><span data-stu-id="7566b-126">INPUTS</span></span>

### <span data-ttu-id="7566b-127">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7566b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7566b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7566b-128">System.String</span></span>

## <span data-ttu-id="7566b-129">출력</span><span class="sxs-lookup"><span data-stu-id="7566b-129">OUTPUTS</span></span>

### <span data-ttu-id="7566b-130">ApiManagement. ServiceManagement. \ PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="7566b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="7566b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7566b-131">NOTES</span></span>

## <span data-ttu-id="7566b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7566b-132">RELATED LINKS</span></span>
