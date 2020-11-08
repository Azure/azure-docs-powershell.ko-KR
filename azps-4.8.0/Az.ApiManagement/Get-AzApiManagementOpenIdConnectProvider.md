---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048017"
---
# <span data-ttu-id="606b3-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="606b3-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="606b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606b3-102">SYNOPSIS</span></span>
<span data-ttu-id="606b3-103">OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="606b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="606b3-104">SYNTAX</span></span>

### <span data-ttu-id="606b3-105">GetAllOpenIdConnectProviders (기본값)</span><span class="sxs-lookup"><span data-stu-id="606b3-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="606b3-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="606b3-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="606b3-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="606b3-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="606b3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="606b3-108">DESCRIPTION</span></span>
<span data-ttu-id="606b3-109">**AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="606b3-110">ClientSecret는 결과 정보에 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="606b3-111">클라이언트 비밀을 가져오려면 Get-help를 **AzApiManagementOpenIdConnectProviderClientSecret** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="606b3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="606b3-112">EXAMPLES</span></span>

### <span data-ttu-id="606b3-113">예제 1: 모든 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="606b3-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="606b3-114">이 명령은 지정 된 컨텍스트에 대 한 모든 OpenID Connect 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="606b3-115">예제 2: ID를 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="606b3-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="606b3-116">이 명령은 ID OICProvider01 인 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="606b3-117">예제 3: 이름을 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="606b3-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="606b3-118">이 명령은 Contoso OpenID Connect Provider 라는 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="606b3-119">변수</span><span class="sxs-lookup"><span data-stu-id="606b3-119">PARAMETERS</span></span>

### <span data-ttu-id="606b3-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="606b3-120">-Context</span></span>
<span data-ttu-id="606b3-121">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="606b3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606b3-122">-DefaultProfile</span></span>
<span data-ttu-id="606b3-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="606b3-124">-이름</span><span class="sxs-lookup"><span data-stu-id="606b3-124">-Name</span></span>
<span data-ttu-id="606b3-125">공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="606b3-126">이름을 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="606b3-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="606b3-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="606b3-128">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="606b3-129">ID를 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="606b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606b3-130">CommonParameters</span></span>
<span data-ttu-id="606b3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="606b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606b3-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="606b3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606b3-133">입력</span><span class="sxs-lookup"><span data-stu-id="606b3-133">INPUTS</span></span>

### <span data-ttu-id="606b3-134">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="606b3-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="606b3-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="606b3-135">System.String</span></span>

## <span data-ttu-id="606b3-136">출력</span><span class="sxs-lookup"><span data-stu-id="606b3-136">OUTPUTS</span></span>

### <span data-ttu-id="606b3-137">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="606b3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="606b3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="606b3-138">NOTES</span></span>

## <span data-ttu-id="606b3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="606b3-139">RELATED LINKS</span></span>

[<span data-ttu-id="606b3-140">새로운 AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="606b3-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="606b3-141">제거-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="606b3-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="606b3-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="606b3-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


