---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d0883edb698000ae0aaff957899a03e9936e4d93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531508"
---
# <span data-ttu-id="db8b5-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db8b5-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="db8b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="db8b5-103">새 Id 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db8b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db8b5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db8b5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="db8b5-105">DESCRIPTION</span></span>
<span data-ttu-id="db8b5-106">새 Id 공급자 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="db8b5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="db8b5-107">EXAMPLES</span></span>

### <span data-ttu-id="db8b5-108">예제 1: Facebook을 개발자 포털 로그인의 id 공급자로 구성</span><span class="sxs-lookup"><span data-stu-id="db8b5-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="db8b5-109">이 명령은 ApiManagement 서비스의 개발자 포털에서 Facebook Id를 허용 된 Id 공급자로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="db8b5-110">이는 Facebook 앱의 ClientId 및 ClientSecret을 입력 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="db8b5-111">변수</span><span class="sxs-lookup"><span data-stu-id="db8b5-111">PARAMETERS</span></span>

### <span data-ttu-id="db8b5-112">-AllowedTenants 넌 트</span><span class="sxs-lookup"><span data-stu-id="db8b5-112">-AllowedTenants</span></span>
<span data-ttu-id="db8b5-113">허용 되는 Azure Active Directory 테 넌 트 목록</span><span class="sxs-lookup"><span data-stu-id="db8b5-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db8b5-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="db8b5-114">-ClientId</span></span>
<span data-ttu-id="db8b5-115">외부 Id 공급자의 응용 프로그램에 대 한 클라이언트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="db8b5-116">Facebook 로그인의 앱 ID, Google 로그인의 클라이언트 ID, Microsoft의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="db8b5-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="db8b5-117">-ClientSecret</span></span>
<span data-ttu-id="db8b5-118">로그인 요청을 인증 하는 데 사용 되는 외부 Id 공급자에 해당 하는 응용 프로그램의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="db8b5-119">예를 들어 Facebook 로그인에 대 한 앱 비밀, Google 로그인의 API 키, Microsoft의 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="db8b5-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="db8b5-120">-Context</span></span>
<span data-ttu-id="db8b5-121">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db8b5-122">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-122">This parameter is required.</span></span>

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

### <span data-ttu-id="db8b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8b5-123">-DefaultProfile</span></span>
<span data-ttu-id="db8b5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db8b5-125">-Type</span><span class="sxs-lookup"><span data-stu-id="db8b5-125">-Type</span></span>
<span data-ttu-id="db8b5-126">Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="db8b5-127">지정 된 경우 식별자를 사용 하 여 id 공급자 구성을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="db8b5-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db8b5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="db8b5-129">-Confirm</span></span>
<span data-ttu-id="db8b5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8b5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db8b5-131">-WhatIf</span></span>
<span data-ttu-id="db8b5-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db8b5-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8b5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8b5-134">CommonParameters</span></span>
<span data-ttu-id="db8b5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db8b5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8b5-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db8b5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8b5-137">입력</span><span class="sxs-lookup"><span data-stu-id="db8b5-137">INPUTS</span></span>

### <span data-ttu-id="db8b5-138">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db8b5-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db8b5-139">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="db8b5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="db8b5-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="db8b5-140">System.String</span></span>

### <span data-ttu-id="db8b5-141">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="db8b5-141">System.String[]</span></span>

## <span data-ttu-id="db8b5-142">출력</span><span class="sxs-lookup"><span data-stu-id="db8b5-142">OUTPUTS</span></span>

### <span data-ttu-id="db8b5-143">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db8b5-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="db8b5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="db8b5-144">NOTES</span></span>

## <span data-ttu-id="db8b5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db8b5-145">RELATED LINKS</span></span>

[<span data-ttu-id="db8b5-146">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db8b5-146">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="db8b5-147">제거-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db8b5-147">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="db8b5-148">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="db8b5-148">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
