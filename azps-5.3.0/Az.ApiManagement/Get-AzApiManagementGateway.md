---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494459"
---
# <span data-ttu-id="f9325-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="f9325-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="f9325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9325-102">SYNOPSIS</span></span>
<span data-ttu-id="f9325-103">전체 또는 특정 API 관리 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="f9325-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9325-104">SYNTAX</span></span>

### <span data-ttu-id="f9325-105">GetAllGateways(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9325-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9325-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="f9325-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9325-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9325-107">DESCRIPTION</span></span>
<span data-ttu-id="f9325-108">**Get-AzApiManagementGateway** cmdlet은 전체 또는 특정 API 관리 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="f9325-109">예제</span><span class="sxs-lookup"><span data-stu-id="f9325-109">EXAMPLES</span></span>

### <span data-ttu-id="f9325-110">예제 1: 모든 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="f9325-111">이 명령은 모든 게이트웨이를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-111">This command gets all gateways.</span></span>

### <span data-ttu-id="f9325-112">예제 2: ID로 게이트웨이를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="f9325-113">이 명령은 게이트웨이 0123456789를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="f9325-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9325-114">PARAMETERS</span></span>

### <span data-ttu-id="f9325-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f9325-115">-Context</span></span>
<span data-ttu-id="f9325-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f9325-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f9325-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9325-118">-DefaultProfile</span></span>
<span data-ttu-id="f9325-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9325-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f9325-120">-GatewayId</span></span>
<span data-ttu-id="f9325-121">게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-121">Identifier of a gateway.</span></span>
<span data-ttu-id="f9325-122">지정된 경우 식별자에 의해 게이트웨이를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="f9325-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9325-123">CommonParameters</span></span>
<span data-ttu-id="f9325-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9325-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9325-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9325-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9325-126">입력</span><span class="sxs-lookup"><span data-stu-id="f9325-126">INPUTS</span></span>

### <span data-ttu-id="f9325-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9325-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9325-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f9325-128">System.String</span></span>

## <span data-ttu-id="f9325-129">출력</span><span class="sxs-lookup"><span data-stu-id="f9325-129">OUTPUTS</span></span>

### <span data-ttu-id="f9325-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="f9325-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="f9325-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9325-131">NOTES</span></span>

## <span data-ttu-id="f9325-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9325-132">RELATED LINKS</span></span>
