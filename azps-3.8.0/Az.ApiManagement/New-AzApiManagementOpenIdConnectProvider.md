---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042223"
---
# <span data-ttu-id="55ecf-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="55ecf-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="55ecf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="55ecf-103">OpenID Connect provider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="55ecf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55ecf-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ecf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="55ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="55ecf-106">**AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="55ecf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="55ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="55ecf-108">예제 1: 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="55ecf-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="55ecf-109">이 명령은 Contoso OpenID Connect Provider 라는 OpenID Connect **provider** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="55ecf-110">변수</span><span class="sxs-lookup"><span data-stu-id="55ecf-110">PARAMETERS</span></span>

### <span data-ttu-id="55ecf-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="55ecf-111">-ClientId</span></span>
<span data-ttu-id="55ecf-112">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="55ecf-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="55ecf-113">-ClientSecret</span></span>
<span data-ttu-id="55ecf-114">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="55ecf-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="55ecf-115">-Context</span></span>
<span data-ttu-id="55ecf-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="55ecf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ecf-117">-DefaultProfile</span></span>
<span data-ttu-id="55ecf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55ecf-119">-설명</span><span class="sxs-lookup"><span data-stu-id="55ecf-119">-Description</span></span>
<span data-ttu-id="55ecf-120">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-120">Specifies a description.</span></span>

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

### <span data-ttu-id="55ecf-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="55ecf-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="55ecf-122">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="55ecf-123">-이름</span><span class="sxs-lookup"><span data-stu-id="55ecf-123">-Name</span></span>
<span data-ttu-id="55ecf-124">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="55ecf-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="55ecf-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="55ecf-126">공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="55ecf-127">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="55ecf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ecf-128">CommonParameters</span></span>
<span data-ttu-id="55ecf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55ecf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ecf-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55ecf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ecf-131">입력</span><span class="sxs-lookup"><span data-stu-id="55ecf-131">INPUTS</span></span>

### <span data-ttu-id="55ecf-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="55ecf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="55ecf-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55ecf-133">System.String</span></span>

## <span data-ttu-id="55ecf-134">출력</span><span class="sxs-lookup"><span data-stu-id="55ecf-134">OUTPUTS</span></span>

### <span data-ttu-id="55ecf-135">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="55ecf-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="55ecf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="55ecf-136">NOTES</span></span>

## <span data-ttu-id="55ecf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55ecf-137">RELATED LINKS</span></span>

[<span data-ttu-id="55ecf-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="55ecf-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="55ecf-139">제거-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="55ecf-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="55ecf-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="55ecf-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


