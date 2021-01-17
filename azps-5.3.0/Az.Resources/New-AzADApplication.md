---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490435"
---
# <span data-ttu-id="be78e-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="be78e-101">New-AzADApplication</span></span>

## <span data-ttu-id="be78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be78e-102">SYNOPSIS</span></span>
<span data-ttu-id="be78e-103">새 Azure Active Directory 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="be78e-104">구문</span><span class="sxs-lookup"><span data-stu-id="be78e-104">SYNTAX</span></span>

### <span data-ttu-id="be78e-105">ApplicationWithoutCredentialParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="be78e-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be78e-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be78e-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be78e-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be78e-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be78e-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="be78e-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be78e-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="be78e-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be78e-110">설명</span><span class="sxs-lookup"><span data-stu-id="be78e-110">DESCRIPTION</span></span>
<span data-ttu-id="be78e-111">새 Azure Active Directory 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="be78e-112">다음은 애플리케이션을 만드는 데 필요한 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="be78e-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="be78e-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="be78e-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="be78e-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="be78e-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="be78e-115">Microsoft Graph</span></span>
  - <span data-ttu-id="be78e-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="be78e-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="be78e-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be78e-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="be78e-118">예제</span><span class="sxs-lookup"><span data-stu-id="be78e-118">EXAMPLES</span></span>

### <span data-ttu-id="be78e-119">예제 1: 새 AAD 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="be78e-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="be78e-120">자격 증명 없이 새 Azure Active Directory 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="be78e-121">예제 2: 암호로 새 AAD 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="be78e-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="be78e-122">새 Azure Active Directory 애플리케이션을 만들고 암호 자격 증명을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="be78e-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be78e-123">PARAMETERS</span></span>

### <span data-ttu-id="be78e-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="be78e-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="be78e-125">애플리케이션이 단일 테넌트인지 다중 테넌트인지를 지정하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="be78e-126">-CertValue</span></span>
<span data-ttu-id="be78e-127">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="be78e-128">기본 64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-128">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be78e-129">-DefaultProfile</span></span>
<span data-ttu-id="be78e-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be78e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be78e-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="be78e-131">-DisplayName</span></span>
<span data-ttu-id="be78e-132">새 애플리케이션의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="be78e-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="be78e-133">-EndDate</span></span>
<span data-ttu-id="be78e-134">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="be78e-135">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-135">The default end date value is one year from today.</span></span> <span data-ttu-id="be78e-136">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-137">-HomePage</span><span class="sxs-lookup"><span data-stu-id="be78e-137">-HomePage</span></span>
<span data-ttu-id="be78e-138">애플리케이션 홈페이지에 대한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="be78e-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="be78e-139">-IdentifierUris</span></span>
<span data-ttu-id="be78e-140">애플리케이션을 식별하는 UR입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-140">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="be78e-141">-KeyCredentials</span></span>
<span data-ttu-id="be78e-142">애플리케이션과 연결된 인증서 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-143">-Password</span><span class="sxs-lookup"><span data-stu-id="be78e-143">-Password</span></span>
<span data-ttu-id="be78e-144">애플리케이션과 연결될 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-144">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="be78e-145">-PasswordCredentials</span></span>
<span data-ttu-id="be78e-146">애플리케이션과 연결된 암호 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="be78e-147">-ReplyUrls</span></span>
<span data-ttu-id="be78e-148">애플리케이션 회신 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-148">The application reply urls.</span></span>

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

### <span data-ttu-id="be78e-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="be78e-149">-StartDate</span></span>
<span data-ttu-id="be78e-150">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="be78e-151">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-151">The default start date value is today.</span></span> <span data-ttu-id="be78e-152">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be78e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be78e-153">-Confirm</span></span>
<span data-ttu-id="be78e-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be78e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be78e-155">-WhatIf</span></span>
<span data-ttu-id="be78e-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="be78e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be78e-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be78e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be78e-158">CommonParameters</span></span>
<span data-ttu-id="be78e-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="be78e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be78e-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be78e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be78e-161">입력</span><span class="sxs-lookup"><span data-stu-id="be78e-161">INPUTS</span></span>

### <span data-ttu-id="be78e-162">System.String</span><span class="sxs-lookup"><span data-stu-id="be78e-162">System.String</span></span>

### <span data-ttu-id="be78e-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="be78e-163">System.String[]</span></span>

### <span data-ttu-id="be78e-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be78e-164">System.Boolean</span></span>

### <span data-ttu-id="be78e-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="be78e-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="be78e-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="be78e-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="be78e-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="be78e-167">System.Security.SecureString</span></span>

### <span data-ttu-id="be78e-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="be78e-168">System.DateTime</span></span>

## <span data-ttu-id="be78e-169">출력</span><span class="sxs-lookup"><span data-stu-id="be78e-169">OUTPUTS</span></span>

### <span data-ttu-id="be78e-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="be78e-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="be78e-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="be78e-171">NOTES</span></span>
<span data-ttu-id="be78e-172">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="be78e-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="be78e-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be78e-173">RELATED LINKS</span></span>

[<span data-ttu-id="be78e-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="be78e-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="be78e-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="be78e-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="be78e-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="be78e-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="be78e-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="be78e-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="be78e-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="be78e-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="be78e-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="be78e-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

