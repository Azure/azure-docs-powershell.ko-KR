---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494443"
---
# <span data-ttu-id="cb9ee-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="cb9ee-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="cb9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ee-103">OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="cb9ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb9ee-104">SYNTAX</span></span>

### <span data-ttu-id="cb9ee-105">GetAllOpenIdConnectProviders(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb9ee-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb9ee-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="cb9ee-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb9ee-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="cb9ee-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9ee-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb9ee-108">DESCRIPTION</span></span>
<span data-ttu-id="cb9ee-109">**Get-AzApiManagementOpenIdConnectProvider** cmdlet은 Azure API Management에서 OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="cb9ee-110">ClientSecret은 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="cb9ee-111">클라이언트 비밀을 얻습니다. **Get-AzApiManagementOpenIdConnectProviderClientSecret을 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="cb9ee-112">예제</span><span class="sxs-lookup"><span data-stu-id="cb9ee-112">EXAMPLES</span></span>

### <span data-ttu-id="cb9ee-113">예제 1: 모든 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="cb9ee-114">이 명령은 지정된 컨텍스트에 대한 모든 OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="cb9ee-115">예제 2: ID를 사용하여 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="cb9ee-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="cb9ee-116">이 명령은 ID OICProvider01이 있는 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="cb9ee-117">예제 3: 이름을 사용하여 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="cb9ee-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="cb9ee-118">이 명령은 Contoso OpenID Connect 공급자라는 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="cb9ee-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9ee-119">PARAMETERS</span></span>

### <span data-ttu-id="cb9ee-120">-Context</span><span class="sxs-lookup"><span data-stu-id="cb9ee-120">-Context</span></span>
<span data-ttu-id="cb9ee-121">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cb9ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ee-122">-DefaultProfile</span></span>
<span data-ttu-id="cb9ee-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb9ee-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb9ee-124">-Name</span></span>
<span data-ttu-id="cb9ee-125">공급자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="cb9ee-126">이름을 지정하면 이 cmdlet은 해당 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ee-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="cb9ee-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="cb9ee-128">이 cmdlet이 제거하는 공급자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="cb9ee-129">ID를 지정하면 이 cmdlet은 해당 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ee-130">CommonParameters</span></span>
<span data-ttu-id="cb9ee-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ee-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ee-133">입력</span><span class="sxs-lookup"><span data-stu-id="cb9ee-133">INPUTS</span></span>

### <span data-ttu-id="cb9ee-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb9ee-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb9ee-135">System.String</span><span class="sxs-lookup"><span data-stu-id="cb9ee-135">System.String</span></span>

## <span data-ttu-id="cb9ee-136">출력</span><span class="sxs-lookup"><span data-stu-id="cb9ee-136">OUTPUTS</span></span>

### <span data-ttu-id="cb9ee-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="cb9ee-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="cb9ee-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb9ee-138">NOTES</span></span>

## <span data-ttu-id="cb9ee-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb9ee-139">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ee-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="cb9ee-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="cb9ee-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="cb9ee-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="cb9ee-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="cb9ee-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


