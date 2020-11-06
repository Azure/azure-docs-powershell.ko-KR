---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532651"
---
# <span data-ttu-id="485b8-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="485b8-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="485b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485b8-102">SYNOPSIS</span></span>
<span data-ttu-id="485b8-103">새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="485b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="485b8-104">SYNTAX</span></span>

### <span data-ttu-id="485b8-105">ApplicationWithoutCredentialParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="485b8-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b8-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b8-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b8-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b8-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b8-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b8-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485b8-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="485b8-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="485b8-110">설명은</span><span class="sxs-lookup"><span data-stu-id="485b8-110">DESCRIPTION</span></span>
<span data-ttu-id="485b8-111">새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="485b8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="485b8-112">EXAMPLES</span></span>

### <span data-ttu-id="485b8-113">새 AAD 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="485b8-114">자격 증명 없이 새 azure active directory 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="485b8-115">비밀 번호를 사용 하 여 새 AAD 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="485b8-116">새 azure active directory 응용 프로그램을 만들고 암호 자격 증명을 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="485b8-117">변수</span><span class="sxs-lookup"><span data-stu-id="485b8-117">PARAMETERS</span></span>

### <span data-ttu-id="485b8-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="485b8-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="485b8-119">응용 프로그램이 단일 테 넌 트 인지 또는 다중 테 넌 트에서 지정 하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="485b8-120">-CertValue</span></span>
<span data-ttu-id="485b8-121">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="485b8-122">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485b8-123">-DefaultProfile</span></span>
<span data-ttu-id="485b8-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="485b8-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="485b8-125">-DisplayName</span></span>
<span data-ttu-id="485b8-126">새 응용 프로그램의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="485b8-127">-EndDate</span></span>
<span data-ttu-id="485b8-128">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="485b8-129">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-129">The default end date value is one year from today.</span></span> <span data-ttu-id="485b8-130">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-131">-홈페이지</span><span class="sxs-lookup"><span data-stu-id="485b8-131">-HomePage</span></span>
<span data-ttu-id="485b8-132">응용 프로그램 홈페이지에 대 한 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="485b8-133">-IdentifierUris</span></span>
<span data-ttu-id="485b8-134">응용 프로그램을 식별 하는 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="485b8-135">-KeyCredentials</span></span>
<span data-ttu-id="485b8-136">응용 프로그램과 연결 된 인증서 자격 증명의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-137">-암호</span><span class="sxs-lookup"><span data-stu-id="485b8-137">-Password</span></span>
<span data-ttu-id="485b8-138">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="485b8-139">-PasswordCredentials</span></span>
<span data-ttu-id="485b8-140">응용 프로그램과 연결 된 암호 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="485b8-141">-ReplyUrls</span></span>
<span data-ttu-id="485b8-142">응용 프로그램 회신 url입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-143">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="485b8-143">-StartDate</span></span>
<span data-ttu-id="485b8-144">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="485b8-145">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-145">The default start date value is today.</span></span> <span data-ttu-id="485b8-146">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-147">-확인</span><span class="sxs-lookup"><span data-stu-id="485b8-147">-Confirm</span></span>
<span data-ttu-id="485b8-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485b8-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="485b8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485b8-150">CommonParameters</span></span>
<span data-ttu-id="485b8-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485b8-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="485b8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485b8-153">입력</span><span class="sxs-lookup"><span data-stu-id="485b8-153">INPUTS</span></span>

### <span data-ttu-id="485b8-154">않아야</span><span class="sxs-lookup"><span data-stu-id="485b8-154">None</span></span>
<span data-ttu-id="485b8-155">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="485b8-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="485b8-156">출력</span><span class="sxs-lookup"><span data-stu-id="485b8-156">OUTPUTS</span></span>

### <span data-ttu-id="485b8-157">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="485b8-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="485b8-158">상속자</span><span class="sxs-lookup"><span data-stu-id="485b8-158">NOTES</span></span>
<span data-ttu-id="485b8-159">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="485b8-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="485b8-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="485b8-160">RELATED LINKS</span></span>

[<span data-ttu-id="485b8-161">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="485b8-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="485b8-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="485b8-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="485b8-163">새로운 AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="485b8-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="485b8-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="485b8-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="485b8-165">새로운 AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="485b8-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="485b8-166">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="485b8-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

