---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214640"
---
# <span data-ttu-id="47340-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47340-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="47340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47340-102">SYNOPSIS</span></span>
<span data-ttu-id="47340-103">기존 게이트웨이에 대 한 모든 또는 특정 호스트 이름 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47340-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="47340-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47340-104">SYNTAX</span></span>

### <span data-ttu-id="47340-105">GetByGatewayId (기본값)</span><span class="sxs-lookup"><span data-stu-id="47340-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47340-106">Getby게이트웨이 Hostnameid</span><span class="sxs-lookup"><span data-stu-id="47340-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47340-107">설명은</span><span class="sxs-lookup"><span data-stu-id="47340-107">DESCRIPTION</span></span>
<span data-ttu-id="47340-108">**AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에 대 한 모든 또는 특정 호스트 이름 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47340-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="47340-109">예제의</span><span class="sxs-lookup"><span data-stu-id="47340-109">EXAMPLES</span></span>

### <span data-ttu-id="47340-110">예제 1: 게이트웨이에 대 한 모든 호스트 이름 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="47340-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="47340-111">이 명령은 "0123456789" 게이트웨이에 대 한 모든 호스트 이름 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47340-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="47340-112">예제 2: 게이트웨이에 대 한 호스트 이름 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="47340-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="47340-113">이 명령은 "0123456789" 게이트웨이에 대 한 "123" 호스트 이름 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47340-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="47340-114">변수</span><span class="sxs-lookup"><span data-stu-id="47340-114">PARAMETERS</span></span>

### <span data-ttu-id="47340-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="47340-115">-Context</span></span>
<span data-ttu-id="47340-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="47340-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-117">This parameter is required.</span></span>

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

### <span data-ttu-id="47340-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47340-118">-DefaultProfile</span></span>
<span data-ttu-id="47340-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47340-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="47340-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="47340-121">호스트 이름 구성 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="47340-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="47340-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="47340-123">-GatewayId</span></span>
<span data-ttu-id="47340-124">게이트웨이 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-124">Gateway identifier.</span></span>
<span data-ttu-id="47340-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="47340-125">This parameter is required.</span></span>

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

### <span data-ttu-id="47340-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47340-126">CommonParameters</span></span>
<span data-ttu-id="47340-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47340-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47340-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47340-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47340-129">입력</span><span class="sxs-lookup"><span data-stu-id="47340-129">INPUTS</span></span>

### <span data-ttu-id="47340-130">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47340-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47340-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47340-131">System.String</span></span>

## <span data-ttu-id="47340-132">출력</span><span class="sxs-lookup"><span data-stu-id="47340-132">OUTPUTS</span></span>

### <span data-ttu-id="47340-133">ApiManagement. ServiceManagement. \ PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47340-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="47340-134">상속자</span><span class="sxs-lookup"><span data-stu-id="47340-134">NOTES</span></span>

## <span data-ttu-id="47340-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47340-135">RELATED LINKS</span></span>
