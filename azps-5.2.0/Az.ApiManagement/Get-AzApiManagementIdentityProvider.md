---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322601"
---
# <span data-ttu-id="b76a8-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b76a8-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b76a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b76a8-103">ID 공급자 구성 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="b76a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="b76a8-104">SYNTAX</span></span>

### <span data-ttu-id="b76a8-105">AllIdentityProviders(기본값)</span><span class="sxs-lookup"><span data-stu-id="b76a8-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b76a8-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="b76a8-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b76a8-107">설명</span><span class="sxs-lookup"><span data-stu-id="b76a8-107">DESCRIPTION</span></span>
<span data-ttu-id="b76a8-108">ID 공급자 구성 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="b76a8-109">ClientSecret은 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="b76a8-110">클라이언트 비밀을 얻습니다. **Get-AzApiManagementIdentityProviderClientSecret을 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="b76a8-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="b76a8-111">예제</span><span class="sxs-lookup"><span data-stu-id="b76a8-111">EXAMPLES</span></span>

### <span data-ttu-id="b76a8-112">예제 1: 모든 ID 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="b76a8-113">서비스에 대한 모든 ID 공급자 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="b76a8-114">예제 2: AAD 형식 ID 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="b76a8-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="b76a8-115">Azure Active Directory의 ID 공급자 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="b76a8-116">예제 3: AAD B2C 형식 ID 공급자를 얻게</span><span class="sxs-lookup"><span data-stu-id="b76a8-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="b76a8-117">Azure Active Directory의 ID 공급자 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="b76a8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76a8-118">PARAMETERS</span></span>

### <span data-ttu-id="b76a8-119">-Context</span><span class="sxs-lookup"><span data-stu-id="b76a8-119">-Context</span></span>
<span data-ttu-id="b76a8-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b76a8-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b76a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76a8-122">-DefaultProfile</span></span>
<span data-ttu-id="b76a8-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76a8-124">-Type</span><span class="sxs-lookup"><span data-stu-id="b76a8-124">-Type</span></span>
<span data-ttu-id="b76a8-125">ID 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="b76a8-126">지정된 경우 식별자에 의해 ID 공급자 구성을 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="b76a8-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b76a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76a8-128">CommonParameters</span></span>
<span data-ttu-id="b76a8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b76a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76a8-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b76a8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76a8-131">입력</span><span class="sxs-lookup"><span data-stu-id="b76a8-131">INPUTS</span></span>

### <span data-ttu-id="b76a8-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b76a8-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b76a8-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="b76a8-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="b76a8-134">출력</span><span class="sxs-lookup"><span data-stu-id="b76a8-134">OUTPUTS</span></span>

### <span data-ttu-id="b76a8-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="b76a8-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="b76a8-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b76a8-136">NOTES</span></span>

## <span data-ttu-id="b76a8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b76a8-137">RELATED LINKS</span></span>
