---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531261"
---
# <span data-ttu-id="597fa-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="597fa-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="597fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="597fa-102">SYNOPSIS</span></span>
<span data-ttu-id="597fa-103">OpenID Connect provider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="597fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="597fa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="597fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="597fa-105">DESCRIPTION</span></span>
<span data-ttu-id="597fa-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="597fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="597fa-107">EXAMPLES</span></span>

### <span data-ttu-id="597fa-108">예제 1: 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="597fa-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="597fa-109">이 명령은 Contoso OpenID Connect Provider 라는 OpenID Connect **provider** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="597fa-110">변수</span><span class="sxs-lookup"><span data-stu-id="597fa-110">PARAMETERS</span></span>

### <span data-ttu-id="597fa-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="597fa-111">-ClientId</span></span>
<span data-ttu-id="597fa-112">개발자 콘솔의 클라이언트 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="597fa-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="597fa-113">-ClientSecret</span></span>
<span data-ttu-id="597fa-114">개발자 콘솔의 클라이언트 비밀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="597fa-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="597fa-115">-Context</span></span>
<span data-ttu-id="597fa-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="597fa-117">-설명</span><span class="sxs-lookup"><span data-stu-id="597fa-117">-Description</span></span>
<span data-ttu-id="597fa-118">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-118">Specifies a description.</span></span>

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

### <span data-ttu-id="597fa-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="597fa-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="597fa-120">공급자의 메타 데이터 끝점 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="597fa-121">-이름</span><span class="sxs-lookup"><span data-stu-id="597fa-121">-Name</span></span>
<span data-ttu-id="597fa-122">공급자에 대 한 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="597fa-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="597fa-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="597fa-124">공급자에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="597fa-125">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="597fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597fa-126">-DefaultProfile</span></span>
<span data-ttu-id="597fa-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="597fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597fa-128">CommonParameters</span></span>
<span data-ttu-id="597fa-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="597fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597fa-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597fa-131">입력</span><span class="sxs-lookup"><span data-stu-id="597fa-131">INPUTS</span></span>

## <span data-ttu-id="597fa-132">출력</span><span class="sxs-lookup"><span data-stu-id="597fa-132">OUTPUTS</span></span>

### <span data-ttu-id="597fa-133">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="597fa-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="597fa-134">상속자</span><span class="sxs-lookup"><span data-stu-id="597fa-134">NOTES</span></span>

## <span data-ttu-id="597fa-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="597fa-135">RELATED LINKS</span></span>

[<span data-ttu-id="597fa-136">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="597fa-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="597fa-137">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="597fa-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="597fa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="597fa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


