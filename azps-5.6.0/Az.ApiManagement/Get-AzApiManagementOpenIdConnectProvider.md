---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014379"
---
# <span data-ttu-id="01ae9-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="01ae9-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="01ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="01ae9-103">OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="01ae9-104">구문</span><span class="sxs-lookup"><span data-stu-id="01ae9-104">SYNTAX</span></span>

### <span data-ttu-id="01ae9-105">GetAllOpenIdConnectProviders(기본값)</span><span class="sxs-lookup"><span data-stu-id="01ae9-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ae9-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="01ae9-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01ae9-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="01ae9-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ae9-108">설명</span><span class="sxs-lookup"><span data-stu-id="01ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="01ae9-109">**Get-AzApiManagementOpenIdConnectProvider** cmdlet은 Azure API Management에서 OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="01ae9-110">ClientSecret은 결과 세부 정보에는 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="01ae9-111">클라이언트 비밀을 얻기 위해 **Get-AzApiManagementOpenIdConnectProviderClientSecret을 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="01ae9-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="01ae9-112">예제</span><span class="sxs-lookup"><span data-stu-id="01ae9-112">EXAMPLES</span></span>

### <span data-ttu-id="01ae9-113">예제 1: 모든 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="01ae9-114">이 명령은 지정된 컨텍스트에 대한 모든 OpenID Connect 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="01ae9-115">예제 2: ID를 사용하여 공급자를 하세요.</span><span class="sxs-lookup"><span data-stu-id="01ae9-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="01ae9-116">이 명령은 ID OICProvider01이 있는 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="01ae9-117">예제 3: 이름을 사용하여 공급자를 하세요.</span><span class="sxs-lookup"><span data-stu-id="01ae9-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="01ae9-118">이 명령은 Contoso OpenID Connect 공급자라는 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="01ae9-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="01ae9-119">PARAMETERS</span></span>

### <span data-ttu-id="01ae9-120">-Context</span><span class="sxs-lookup"><span data-stu-id="01ae9-120">-Context</span></span>
<span data-ttu-id="01ae9-121">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="01ae9-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01ae9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ae9-122">-DefaultProfile</span></span>
<span data-ttu-id="01ae9-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ae9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="01ae9-124">-Name</span></span>
<span data-ttu-id="01ae9-125">공급자의 친숙한 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="01ae9-126">이름을 지정하면 이 cmdlet에서 해당 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="01ae9-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="01ae9-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="01ae9-128">이 cmdlet이 제거한 공급자의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="01ae9-129">ID를 지정하는 경우 이 cmdlet은 해당 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="01ae9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ae9-130">CommonParameters</span></span>
<span data-ttu-id="01ae9-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01ae9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ae9-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01ae9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ae9-133">입력</span><span class="sxs-lookup"><span data-stu-id="01ae9-133">INPUTS</span></span>

### <span data-ttu-id="01ae9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01ae9-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01ae9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="01ae9-135">System.String</span></span>

## <span data-ttu-id="01ae9-136">출력</span><span class="sxs-lookup"><span data-stu-id="01ae9-136">OUTPUTS</span></span>

### <span data-ttu-id="01ae9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="01ae9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="01ae9-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01ae9-138">NOTES</span></span>

## <span data-ttu-id="01ae9-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01ae9-139">RELATED LINKS</span></span>

[<span data-ttu-id="01ae9-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="01ae9-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="01ae9-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="01ae9-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="01ae9-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="01ae9-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


