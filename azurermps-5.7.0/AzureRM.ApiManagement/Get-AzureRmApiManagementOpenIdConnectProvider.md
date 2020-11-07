---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703593"
---
# <span data-ttu-id="5c53d-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5c53d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c53d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c53d-103">OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c53d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c53d-104">SYNTAX</span></span>

### <span data-ttu-id="5c53d-105">GetAllOpenIdConnectProviders (기본값)</span><span class="sxs-lookup"><span data-stu-id="5c53d-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c53d-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5c53d-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c53d-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="5c53d-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c53d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5c53d-108">DESCRIPTION</span></span>
<span data-ttu-id="5c53d-109">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="5c53d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5c53d-110">EXAMPLES</span></span>

### <span data-ttu-id="5c53d-111">예제 1: 모든 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c53d-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="5c53d-112">이 명령은 지정 된 컨텍스트에 대 한 모든 OpenID Connect 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="5c53d-113">예제 2: ID를 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c53d-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="5c53d-114">이 명령은 ID OICProvicer01 인 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="5c53d-115">예제 3: 이름을 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c53d-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="5c53d-116">이 명령은 Contoso OpenID Connect Provider 라는 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="5c53d-117">변수</span><span class="sxs-lookup"><span data-stu-id="5c53d-117">PARAMETERS</span></span>

### <span data-ttu-id="5c53d-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5c53d-118">-Context</span></span>
<span data-ttu-id="5c53d-119">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-119">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c53d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c53d-120">-DefaultProfile</span></span>
<span data-ttu-id="5c53d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c53d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5c53d-122">-Name</span></span>
<span data-ttu-id="5c53d-123">공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="5c53d-124">이름을 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c53d-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5c53d-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5c53d-126">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="5c53d-127">ID를 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c53d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c53d-128">CommonParameters</span></span>
<span data-ttu-id="5c53d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c53d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c53d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c53d-131">입력</span><span class="sxs-lookup"><span data-stu-id="5c53d-131">INPUTS</span></span>

### <span data-ttu-id="5c53d-132">않아야</span><span class="sxs-lookup"><span data-stu-id="5c53d-132">None</span></span>
<span data-ttu-id="5c53d-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c53d-134">출력</span><span class="sxs-lookup"><span data-stu-id="5c53d-134">OUTPUTS</span></span>

### <span data-ttu-id="5c53d-135">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="5c53d-136">API Management 서비스에서 구성 된 OpenId connect Provider의 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="5c53d-137">IList를<ApiManagement> ServiceManagement. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="5c53d-138">API Management 서비스에서 구성 된 OpenId Connect 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5c53d-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="5c53d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="5c53d-139">NOTES</span></span>

## <span data-ttu-id="5c53d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c53d-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c53d-141">새로운 AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5c53d-142">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5c53d-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5c53d-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


