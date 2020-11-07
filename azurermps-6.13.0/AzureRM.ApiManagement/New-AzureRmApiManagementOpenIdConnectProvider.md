---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c338cd8b2ea3ce2a464a7975ecac959bc1e52140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703192"
---
# <span data-ttu-id="2b231-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2b231-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2b231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b231-102">SYNOPSIS</span></span>
<span data-ttu-id="2b231-103">OpenID Connect provider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b231-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b231-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b231-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b231-105">DESCRIPTION</span></span>
<span data-ttu-id="2b231-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="2b231-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b231-107">EXAMPLES</span></span>

### <span data-ttu-id="2b231-108">예제 1: 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="2b231-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="2b231-109">이 명령은 Contoso OpenID Connect Provider 라는 OpenID Connect **provider** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="2b231-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b231-110">PARAMETERS</span></span>

### <span data-ttu-id="2b231-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2b231-111">-ClientId</span></span>
<span data-ttu-id="2b231-112">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="2b231-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2b231-113">-ClientSecret</span></span>
<span data-ttu-id="2b231-114">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b231-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2b231-115">-Context</span></span>
<span data-ttu-id="2b231-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b231-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b231-117">-DefaultProfile</span></span>
<span data-ttu-id="2b231-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b231-119">-설명</span><span class="sxs-lookup"><span data-stu-id="2b231-119">-Description</span></span>
<span data-ttu-id="2b231-120">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b231-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="2b231-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="2b231-122">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="2b231-123">-이름</span><span class="sxs-lookup"><span data-stu-id="2b231-123">-Name</span></span>
<span data-ttu-id="2b231-124">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="2b231-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2b231-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2b231-126">공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="2b231-127">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b231-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b231-128">CommonParameters</span></span>
<span data-ttu-id="2b231-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b231-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b231-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b231-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b231-131">입력</span><span class="sxs-lookup"><span data-stu-id="2b231-131">INPUTS</span></span>

### <span data-ttu-id="2b231-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b231-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b231-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b231-133">System.String</span></span>

## <span data-ttu-id="2b231-134">출력</span><span class="sxs-lookup"><span data-stu-id="2b231-134">OUTPUTS</span></span>

### <span data-ttu-id="2b231-135">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2b231-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2b231-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2b231-136">NOTES</span></span>

## <span data-ttu-id="2b231-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b231-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b231-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2b231-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2b231-139">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2b231-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2b231-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2b231-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


