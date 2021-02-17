---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205781"
---
# <span data-ttu-id="28ab1-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="28ab1-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="28ab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="28ab1-103">기존 게이트웨이에 대한 전체 또는 특정 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="28ab1-104">구문</span><span class="sxs-lookup"><span data-stu-id="28ab1-104">SYNTAX</span></span>

### <span data-ttu-id="28ab1-105">GetByGatewayId(기본값)</span><span class="sxs-lookup"><span data-stu-id="28ab1-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28ab1-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="28ab1-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ab1-107">설명</span><span class="sxs-lookup"><span data-stu-id="28ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="28ab1-108">**Get-AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에 대한 전체 또는 특정 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="28ab1-109">예제</span><span class="sxs-lookup"><span data-stu-id="28ab1-109">EXAMPLES</span></span>

### <span data-ttu-id="28ab1-110">예제 1: 게이트웨이에 대한 모든 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="28ab1-111">이 명령은 "0123456789" 게이트웨이에 대한 모든 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="28ab1-112">예제 2: 게이트웨이에 대한 호스트 이름 구성을 얻게</span><span class="sxs-lookup"><span data-stu-id="28ab1-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="28ab1-113">이 명령은 "0123456789" 게이트웨이에 대한 "123" 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="28ab1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28ab1-114">PARAMETERS</span></span>

### <span data-ttu-id="28ab1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="28ab1-115">-Context</span></span>
<span data-ttu-id="28ab1-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="28ab1-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="28ab1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ab1-118">-DefaultProfile</span></span>
<span data-ttu-id="28ab1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28ab1-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="28ab1-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="28ab1-121">호스트 이름 구성 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="28ab1-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ab1-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="28ab1-123">-GatewayId</span></span>
<span data-ttu-id="28ab1-124">게이트웨이 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-124">Gateway identifier.</span></span>
<span data-ttu-id="28ab1-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="28ab1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ab1-126">CommonParameters</span></span>
<span data-ttu-id="28ab1-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28ab1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ab1-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28ab1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ab1-129">입력</span><span class="sxs-lookup"><span data-stu-id="28ab1-129">INPUTS</span></span>

### <span data-ttu-id="28ab1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="28ab1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="28ab1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="28ab1-131">System.String</span></span>

## <span data-ttu-id="28ab1-132">출력</span><span class="sxs-lookup"><span data-stu-id="28ab1-132">OUTPUTS</span></span>

### <span data-ttu-id="28ab1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="28ab1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="28ab1-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28ab1-134">NOTES</span></span>

## <span data-ttu-id="28ab1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28ab1-135">RELATED LINKS</span></span>
