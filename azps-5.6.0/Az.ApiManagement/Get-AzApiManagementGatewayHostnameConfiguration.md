---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981328"
---
# <span data-ttu-id="802ef-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="802ef-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="802ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="802ef-102">SYNOPSIS</span></span>
<span data-ttu-id="802ef-103">기존 게이트웨이에 대한 전체 또는 특정 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="802ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="802ef-104">SYNTAX</span></span>

### <span data-ttu-id="802ef-105">GetByGatewayId(기본값)</span><span class="sxs-lookup"><span data-stu-id="802ef-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="802ef-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="802ef-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="802ef-107">설명</span><span class="sxs-lookup"><span data-stu-id="802ef-107">DESCRIPTION</span></span>
<span data-ttu-id="802ef-108">**Get-AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에 대한 전체 또는 특정 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="802ef-109">예제</span><span class="sxs-lookup"><span data-stu-id="802ef-109">EXAMPLES</span></span>

### <span data-ttu-id="802ef-110">예제 1: 게이트웨이에 대한 모든 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="802ef-111">이 명령은 "0123456789" 게이트웨이에 대한 모든 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="802ef-112">예제 2: 게이트웨이에 대한 호스트 이름 구성을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="802ef-113">이 명령은 "0123456789" 게이트웨이에 대해 "123" 호스트 이름 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="802ef-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="802ef-114">PARAMETERS</span></span>

### <span data-ttu-id="802ef-115">-Context</span><span class="sxs-lookup"><span data-stu-id="802ef-115">-Context</span></span>
<span data-ttu-id="802ef-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="802ef-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-117">This parameter is required.</span></span>

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

### <span data-ttu-id="802ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802ef-118">-DefaultProfile</span></span>
<span data-ttu-id="802ef-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802ef-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="802ef-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="802ef-121">호스트 이름 구성 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="802ef-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="802ef-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="802ef-123">-GatewayId</span></span>
<span data-ttu-id="802ef-124">게이트웨이 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-124">Gateway identifier.</span></span>
<span data-ttu-id="802ef-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-125">This parameter is required.</span></span>

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

### <span data-ttu-id="802ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802ef-126">CommonParameters</span></span>
<span data-ttu-id="802ef-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="802ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802ef-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="802ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802ef-129">입력</span><span class="sxs-lookup"><span data-stu-id="802ef-129">INPUTS</span></span>

### <span data-ttu-id="802ef-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="802ef-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="802ef-131">System.String</span><span class="sxs-lookup"><span data-stu-id="802ef-131">System.String</span></span>

## <span data-ttu-id="802ef-132">출력</span><span class="sxs-lookup"><span data-stu-id="802ef-132">OUTPUTS</span></span>

### <span data-ttu-id="802ef-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="802ef-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="802ef-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="802ef-134">NOTES</span></span>

## <span data-ttu-id="802ef-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="802ef-135">RELATED LINKS</span></span>
