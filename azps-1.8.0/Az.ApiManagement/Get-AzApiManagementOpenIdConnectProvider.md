---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b6c8c0260e1f45b55dedca4d0a9f1f5ab3fed59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689144"
---
# <span data-ttu-id="56fe0-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="56fe0-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="56fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="56fe0-103">OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="56fe0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56fe0-104">SYNTAX</span></span>

### <span data-ttu-id="56fe0-105">GetAllOpenIdConnectProviders (기본값)</span><span class="sxs-lookup"><span data-stu-id="56fe0-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fe0-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="56fe0-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fe0-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="56fe0-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56fe0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="56fe0-108">DESCRIPTION</span></span>
<span data-ttu-id="56fe0-109">**AzApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="56fe0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="56fe0-110">EXAMPLES</span></span>

### <span data-ttu-id="56fe0-111">예제 1: 모든 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="56fe0-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="56fe0-112">이 명령은 지정 된 컨텍스트에 대 한 모든 OpenID Connect 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="56fe0-113">예제 2: ID를 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="56fe0-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="56fe0-114">이 명령은 ID OICProvicer01 인 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="56fe0-115">예제 3: 이름을 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="56fe0-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="56fe0-116">이 명령은 Contoso OpenID Connect Provider 라는 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="56fe0-117">변수</span><span class="sxs-lookup"><span data-stu-id="56fe0-117">PARAMETERS</span></span>

### <span data-ttu-id="56fe0-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="56fe0-118">-Context</span></span>
<span data-ttu-id="56fe0-119">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="56fe0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fe0-120">-DefaultProfile</span></span>
<span data-ttu-id="56fe0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56fe0-122">-이름</span><span class="sxs-lookup"><span data-stu-id="56fe0-122">-Name</span></span>
<span data-ttu-id="56fe0-123">공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="56fe0-124">이름을 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="56fe0-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="56fe0-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="56fe0-126">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="56fe0-127">ID를 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="56fe0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fe0-128">CommonParameters</span></span>
<span data-ttu-id="56fe0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56fe0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fe0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56fe0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fe0-131">입력</span><span class="sxs-lookup"><span data-stu-id="56fe0-131">INPUTS</span></span>

### <span data-ttu-id="56fe0-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="56fe0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="56fe0-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56fe0-133">System.String</span></span>

## <span data-ttu-id="56fe0-134">출력</span><span class="sxs-lookup"><span data-stu-id="56fe0-134">OUTPUTS</span></span>

### <span data-ttu-id="56fe0-135">ApiManagement. ServiceManagement. \ PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="56fe0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="56fe0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="56fe0-136">NOTES</span></span>

## <span data-ttu-id="56fe0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56fe0-137">RELATED LINKS</span></span>

[<span data-ttu-id="56fe0-138">새로운 AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="56fe0-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="56fe0-139">제거-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="56fe0-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="56fe0-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="56fe0-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


