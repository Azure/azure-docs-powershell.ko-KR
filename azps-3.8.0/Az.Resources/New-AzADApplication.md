---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: a60e2b873803c8ad3acfdc08c645cf419cf8689f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044460"
---
# <span data-ttu-id="8e1fc-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e1fc-101">New-AzADApplication</span></span>

## <span data-ttu-id="8e1fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1fc-103">새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="8e1fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e1fc-104">SYNTAX</span></span>

### <span data-ttu-id="8e1fc-105">ApplicationWithoutCredentialParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e1fc-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1fc-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e1fc-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1fc-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e1fc-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1fc-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e1fc-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1fc-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e1fc-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e1fc-110">설명은</span><span class="sxs-lookup"><span data-stu-id="8e1fc-110">DESCRIPTION</span></span>
<span data-ttu-id="8e1fc-111">새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="8e1fc-112">다음은 응용 프로그램을 만드는 데 필요한 사용 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="8e1fc-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="8e1fc-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="8e1fc-114">Application. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="8e1fc-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="8e1fc-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8e1fc-115">Microsoft Graph</span></span>
  - <span data-ttu-id="8e1fc-116">Directory. AccessAsUser. 모든</span><span class="sxs-lookup"><span data-stu-id="8e1fc-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="8e1fc-117">Directory. a $ $</span><span class="sxs-lookup"><span data-stu-id="8e1fc-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="8e1fc-118">예제의</span><span class="sxs-lookup"><span data-stu-id="8e1fc-118">EXAMPLES</span></span>

### <span data-ttu-id="8e1fc-119">예제 1-새 AAD 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="8e1fc-119">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="8e1fc-120">자격 증명 없이 새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="8e1fc-121">예제 2-암호를 사용 하 여 새 AAD 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="8e1fc-121">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="8e1fc-122">새 azure active directory 응용 프로그램을 만들고 암호 자격 증명을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="8e1fc-123">변수</span><span class="sxs-lookup"><span data-stu-id="8e1fc-123">PARAMETERS</span></span>

### <span data-ttu-id="8e1fc-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="8e1fc-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="8e1fc-125">응용 프로그램이 단일 테 넌 트 인지 또는 다중 테 넌 트에서 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="8e1fc-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8e1fc-126">-CertValue</span></span>
<span data-ttu-id="8e1fc-127">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="8e1fc-128">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="8e1fc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1fc-129">-DefaultProfile</span></span>
<span data-ttu-id="8e1fc-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e1fc-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e1fc-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e1fc-131">-DisplayName</span></span>
<span data-ttu-id="8e1fc-132">새 응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="8e1fc-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8e1fc-133">-EndDate</span></span>
<span data-ttu-id="8e1fc-134">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="8e1fc-135">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-135">The default end date value is one year from today.</span></span> <span data-ttu-id="8e1fc-136">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="8e1fc-137">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="8e1fc-137">-HomePage</span></span>
<span data-ttu-id="8e1fc-138">응용 프로그램 홈페이지에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="8e1fc-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="8e1fc-139">-IdentifierUris</span></span>
<span data-ttu-id="8e1fc-140">응용 프로그램을 식별 하는 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="8e1fc-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="8e1fc-141">-KeyCredentials</span></span>
<span data-ttu-id="8e1fc-142">응용 프로그램과 연결 된 인증서 자격 증명의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="8e1fc-143">-암호</span><span class="sxs-lookup"><span data-stu-id="8e1fc-143">-Password</span></span>
<span data-ttu-id="8e1fc-144">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="8e1fc-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="8e1fc-145">-PasswordCredentials</span></span>
<span data-ttu-id="8e1fc-146">응용 프로그램과 연결 된 암호 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="8e1fc-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="8e1fc-147">-ReplyUrls</span></span>
<span data-ttu-id="8e1fc-148">응용 프로그램 회신 url입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-148">The application reply urls.</span></span>

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

### <span data-ttu-id="8e1fc-149">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="8e1fc-149">-StartDate</span></span>
<span data-ttu-id="8e1fc-150">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="8e1fc-151">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-151">The default start date value is today.</span></span> <span data-ttu-id="8e1fc-152">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="8e1fc-153">-확인</span><span class="sxs-lookup"><span data-stu-id="8e1fc-153">-Confirm</span></span>
<span data-ttu-id="8e1fc-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1fc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1fc-155">-WhatIf</span></span>
<span data-ttu-id="8e1fc-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e1fc-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e1fc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1fc-158">CommonParameters</span></span>
<span data-ttu-id="8e1fc-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1fc-160">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e1fc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1fc-161">입력</span><span class="sxs-lookup"><span data-stu-id="8e1fc-161">INPUTS</span></span>

### <span data-ttu-id="8e1fc-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e1fc-162">System.String</span></span>

### <span data-ttu-id="8e1fc-163">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="8e1fc-163">System.String[]</span></span>

### <span data-ttu-id="8e1fc-164">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8e1fc-164">System.Boolean</span></span>

### <span data-ttu-id="8e1fc-165">ActiveDirectory PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="8e1fc-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="8e1fc-166">ActiveDirectory PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="8e1fc-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="8e1fc-167">System.webserver</span><span class="sxs-lookup"><span data-stu-id="8e1fc-167">System.Security.SecureString</span></span>

### <span data-ttu-id="8e1fc-168">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="8e1fc-168">System.DateTime</span></span>

## <span data-ttu-id="8e1fc-169">출력</span><span class="sxs-lookup"><span data-stu-id="8e1fc-169">OUTPUTS</span></span>

### <span data-ttu-id="8e1fc-170">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="8e1fc-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8e1fc-171">상속자</span><span class="sxs-lookup"><span data-stu-id="8e1fc-171">NOTES</span></span>
<span data-ttu-id="8e1fc-172">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="8e1fc-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8e1fc-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e1fc-173">RELATED LINKS</span></span>

[<span data-ttu-id="8e1fc-174">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e1fc-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8e1fc-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e1fc-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="8e1fc-176">새로운 AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8e1fc-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="8e1fc-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e1fc-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8e1fc-178">새로운 AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e1fc-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8e1fc-179">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e1fc-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

