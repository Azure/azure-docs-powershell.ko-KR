---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041933"
---
# <span data-ttu-id="f1c5a-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f1c5a-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f1c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c5a-103">Id 공급자 구성 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f1c5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1c5a-104">SYNTAX</span></span>

### <span data-ttu-id="f1c5a-105">AllIdentityProviders (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1c5a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c5a-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="f1c5a-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c5a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f1c5a-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c5a-108">Id 공급자 구성 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="f1c5a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f1c5a-109">EXAMPLES</span></span>

### <span data-ttu-id="f1c5a-110">예제 1: 모든 Id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="f1c5a-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="f1c5a-111">서비스에서 모든 id 공급자 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="f1c5a-112">예제 2: AAD 형식 Id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="f1c5a-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f1c5a-113">Azure Active Directory의 Id 공급자 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="f1c5a-114">예제 3: AAD B2C 형식 Id 공급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="f1c5a-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="f1c5a-115">Azure Active Directory의 Id 공급자 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="f1c5a-116">변수</span><span class="sxs-lookup"><span data-stu-id="f1c5a-116">PARAMETERS</span></span>

### <span data-ttu-id="f1c5a-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f1c5a-117">-Context</span></span>
<span data-ttu-id="f1c5a-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f1c5a-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f1c5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c5a-120">-DefaultProfile</span></span>
<span data-ttu-id="f1c5a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c5a-122">-Type</span><span class="sxs-lookup"><span data-stu-id="f1c5a-122">-Type</span></span>
<span data-ttu-id="f1c5a-123">Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f1c5a-124">지정 된 경우 식별자를 사용 하 여 id 공급자 구성을 찾으려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f1c5a-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c5a-126">CommonParameters</span></span>
<span data-ttu-id="f1c5a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c5a-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1c5a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c5a-129">입력</span><span class="sxs-lookup"><span data-stu-id="f1c5a-129">INPUTS</span></span>

### <span data-ttu-id="f1c5a-130">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1c5a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1c5a-131">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f1c5a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="f1c5a-132">출력</span><span class="sxs-lookup"><span data-stu-id="f1c5a-132">OUTPUTS</span></span>

### <span data-ttu-id="f1c5a-133">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f1c5a-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f1c5a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f1c5a-134">NOTES</span></span>

## <span data-ttu-id="f1c5a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1c5a-135">RELATED LINKS</span></span>
