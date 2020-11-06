---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525803"
---
# <span data-ttu-id="156ae-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="156ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156ae-102">SYNOPSIS</span></span>
<span data-ttu-id="156ae-103">OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="156ae-104">SYNTAX</span></span>

### <span data-ttu-id="156ae-105">모든 OpenID 연결 공급자 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="156ae-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156ae-106">Get by OpenID 연결 공급자 ID</span><span class="sxs-lookup"><span data-stu-id="156ae-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="156ae-107">OpenID에서 찾기 공급자 이름 연결</span><span class="sxs-lookup"><span data-stu-id="156ae-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="156ae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="156ae-108">DESCRIPTION</span></span>
<span data-ttu-id="156ae-109">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet은 Azure API Management에서 OpenID 연결 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="156ae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="156ae-110">EXAMPLES</span></span>

### <span data-ttu-id="156ae-111">예제 1: 모든 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="156ae-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="156ae-112">이 명령은 지정 된 컨텍스트에 대 한 모든 OpenID Connect 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="156ae-113">예제 2: ID를 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="156ae-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="156ae-114">이 명령은 ID OICProvicer01 인 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="156ae-115">예제 3: 이름을 사용 하 여 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="156ae-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="156ae-116">이 명령은 Contoso OpenID Connect Provider 라는 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="156ae-117">변수</span><span class="sxs-lookup"><span data-stu-id="156ae-117">PARAMETERS</span></span>

### <span data-ttu-id="156ae-118">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="156ae-118">-Context</span></span>
<span data-ttu-id="156ae-119">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="156ae-120">-이름</span><span class="sxs-lookup"><span data-stu-id="156ae-120">-Name</span></span>
<span data-ttu-id="156ae-121">공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="156ae-122">이름을 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156ae-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="156ae-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="156ae-124">이 cmdlet이 제거 하는 공급자의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="156ae-125">ID를 지정 하면이 cmdlet은 해당 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156ae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156ae-126">-DefaultProfile</span></span>
<span data-ttu-id="156ae-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="156ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ae-128">CommonParameters</span></span>
<span data-ttu-id="156ae-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="156ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ae-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156ae-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ae-131">입력</span><span class="sxs-lookup"><span data-stu-id="156ae-131">INPUTS</span></span>

## <span data-ttu-id="156ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="156ae-132">OUTPUTS</span></span>

### <span data-ttu-id="156ae-133">IList를<ApiManagement> ServiceManagement. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="156ae-134">상속자</span><span class="sxs-lookup"><span data-stu-id="156ae-134">NOTES</span></span>

## <span data-ttu-id="156ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="156ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="156ae-136">새로운 AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="156ae-137">제거-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="156ae-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


