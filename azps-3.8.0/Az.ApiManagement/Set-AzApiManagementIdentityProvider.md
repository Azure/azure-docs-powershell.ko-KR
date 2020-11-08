---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: a110e950bff46bba7d3c7b5033c01b95ac2397f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043855"
---
# <span data-ttu-id="af8ef-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="af8ef-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="af8ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="af8ef-103">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="af8ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af8ef-104">SYNTAX</span></span>

### <span data-ttu-id="af8ef-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="af8ef-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SignInTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af8ef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af8ef-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SignInTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af8ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="af8ef-107">DESCRIPTION</span></span>
<span data-ttu-id="af8ef-108">기존 Id 공급자의 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="af8ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="af8ef-109">EXAMPLES</span></span>

### <span data-ttu-id="af8ef-110">예제 1: facebook Id 공급자 업데이트</span><span class="sxs-lookup"><span data-stu-id="af8ef-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="af8ef-111">Cmdlet은 Facebook Id 공급자의 클라이언트 비밀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="af8ef-112">변수</span><span class="sxs-lookup"><span data-stu-id="af8ef-112">PARAMETERS</span></span>

### <span data-ttu-id="af8ef-113">-AllowedTenants 넌 트</span><span class="sxs-lookup"><span data-stu-id="af8ef-113">-AllowedTenants</span></span>
<span data-ttu-id="af8ef-114">허용 되는 Azure Active Directory 테 넌 트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="af8ef-115">-기관</span><span class="sxs-lookup"><span data-stu-id="af8ef-115">-Authority</span></span>
<span data-ttu-id="af8ef-116">AAD 또는 AAD B2C에 대 한 OpenID Connect 검색 끝점 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="af8ef-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="af8ef-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="af8ef-118">-ClientId</span></span>
<span data-ttu-id="af8ef-119">외부 Id 공급자의 응용 프로그램에 대 한 클라이언트 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="af8ef-120">Facebook 로그인의 앱 ID, Google 로그인의 클라이언트 ID, Microsoft의 앱 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="af8ef-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="af8ef-121">-ClientSecret</span></span>
<span data-ttu-id="af8ef-122">로그인 요청을 인증 하는 데 사용 되는 외부 Id 공급자에 해당 하는 응용 프로그램의 클라이언트 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="af8ef-123">예를 들어 Facebook 로그인에 대 한 앱 비밀, Google 로그인의 API 키, Microsoft의 공개 키입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="af8ef-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="af8ef-124">-Context</span></span>
<span data-ttu-id="af8ef-125">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="af8ef-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ef-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af8ef-127">-DefaultProfile</span></span>
<span data-ttu-id="af8ef-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af8ef-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af8ef-129">-InputObject</span></span>
<span data-ttu-id="af8ef-130">PsApiManagementIdentityProvider의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="af8ef-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ef-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af8ef-132">-PassThru</span></span>
<span data-ttu-id="af8ef-133">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementIdentityProvider** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ef-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="af8ef-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="af8ef-135">암호 재설정 정책 이름.</span><span class="sxs-lookup"><span data-stu-id="af8ef-135">Password Reset Policy Name.</span></span> <span data-ttu-id="af8ef-136">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="af8ef-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="af8ef-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="af8ef-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="af8ef-139">프로필 편집 정책 이름</span><span class="sxs-lookup"><span data-stu-id="af8ef-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="af8ef-140">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="af8ef-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="af8ef-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="af8ef-142">-SigninPolicyName</span></span>
<span data-ttu-id="af8ef-143">로그인 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-143">Signin Policy Name.</span></span> <span data-ttu-id="af8ef-144">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="af8ef-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="af8ef-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="af8ef-146">-SignupPolicyName</span></span>
<span data-ttu-id="af8ef-147">등록 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-147">Signup Policy Name.</span></span> <span data-ttu-id="af8ef-148">AAD B2C Id 공급자에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="af8ef-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="af8ef-150">-Type</span><span class="sxs-lookup"><span data-stu-id="af8ef-150">-Type</span></span>
<span data-ttu-id="af8ef-151">기존 Id 공급자의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="af8ef-152">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af8ef-153">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="af8ef-153">-SigninTenant</span></span>
<span data-ttu-id="af8ef-154">테 넌 트가 아닌 AAD B2C에서 재정의 하도록 로그인 테 넌 트 `common`</span><span class="sxs-lookup"><span data-stu-id="af8ef-154">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="af8ef-155">-확인</span><span class="sxs-lookup"><span data-stu-id="af8ef-155">-Confirm</span></span>
<span data-ttu-id="af8ef-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af8ef-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af8ef-157">-WhatIf</span></span>
<span data-ttu-id="af8ef-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af8ef-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af8ef-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af8ef-160">CommonParameters</span></span>
<span data-ttu-id="af8ef-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af8ef-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af8ef-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af8ef-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af8ef-163">입력</span><span class="sxs-lookup"><span data-stu-id="af8ef-163">INPUTS</span></span>

### <span data-ttu-id="af8ef-164">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="af8ef-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="af8ef-165">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="af8ef-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="af8ef-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="af8ef-166">System.String</span></span>

### <span data-ttu-id="af8ef-167">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="af8ef-167">System.String[]</span></span>

### <span data-ttu-id="af8ef-168">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="af8ef-168">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af8ef-169">출력</span><span class="sxs-lookup"><span data-stu-id="af8ef-169">OUTPUTS</span></span>

### <span data-ttu-id="af8ef-170">ApiManagement. ServiceManagement. \ PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="af8ef-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="af8ef-171">상속자</span><span class="sxs-lookup"><span data-stu-id="af8ef-171">NOTES</span></span>

## <span data-ttu-id="af8ef-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af8ef-172">RELATED LINKS</span></span>

[<span data-ttu-id="af8ef-173">새로운 AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="af8ef-173">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="af8ef-174">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="af8ef-174">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="af8ef-175">제거-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="af8ef-175">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)