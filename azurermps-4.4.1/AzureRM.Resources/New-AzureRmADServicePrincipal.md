---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711502"
---
# <span data-ttu-id="3995d-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3995d-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="3995d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3995d-102">SYNOPSIS</span></span>
<span data-ttu-id="3995d-103">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3995d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3995d-104">SYNTAX</span></span>

### <span data-ttu-id="3995d-105">ApplicationWithoutCredentialParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3995d-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3995d-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="3995d-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3995d-115">설명은</span><span class="sxs-lookup"><span data-stu-id="3995d-115">DESCRIPTION</span></span>
<span data-ttu-id="3995d-116">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="3995d-117">참고: 또한 cmdlet은 응용 프로그램을 암시적으로 만들고 해당 속성 (ApplicationId이 제공 되지 않은 경우)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="3995d-118">응용 프로그램별 매개 변수를 업데이트 하려면 Set-AzureRmADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="3995d-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="3995d-119">예제의</span><span class="sxs-lookup"><span data-stu-id="3995d-119">EXAMPLES</span></span>

### <span data-ttu-id="3995d-120">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3995d-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="3995d-121">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="3995d-122">DisplayName 형식 ObjectId</span><span class="sxs-lookup"><span data-stu-id="3995d-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="3995d-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="3995d-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="3995d-124">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3995d-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="3995d-125">새 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-125">Creates a new service principal.</span></span>
<span data-ttu-id="3995d-126">또한 cmdlet은 응용 프로그램을 암시적으로 만들기 때문에이는 제공 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="3995d-127">DisplayName 형식 ObjectId</span><span class="sxs-lookup"><span data-stu-id="3995d-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="3995d-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="3995d-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="3995d-129">변수</span><span class="sxs-lookup"><span data-stu-id="3995d-129">PARAMETERS</span></span>

### <span data-ttu-id="3995d-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3995d-130">-ApplicationId</span></span>
<span data-ttu-id="3995d-131">테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="3995d-132">만든 후에는이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="3995d-133">응용 프로그램 id가 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="3995d-134">-CertValue</span></span>
<span data-ttu-id="3995d-135">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="3995d-136">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3995d-137">-DisplayName</span></span>
<span data-ttu-id="3995d-138">서비스 사용자의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-139">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3995d-139">-EndDate</span></span>
<span data-ttu-id="3995d-140">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="3995d-141">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-141">The default end date value is one year from today.</span></span> <span data-ttu-id="3995d-142">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-143">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="3995d-143">-KeyCredentials</span></span>
<span data-ttu-id="3995d-144">서비스 사용자와 연결 된 인증서 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-145">-암호</span><span class="sxs-lookup"><span data-stu-id="3995d-145">-Password</span></span>
<span data-ttu-id="3995d-146">서비스 사용자와 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="3995d-147">-PasswordCredentials</span></span>
<span data-ttu-id="3995d-148">서비스 사용자와 연결 된 암호 자격 증명 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-149">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="3995d-149">-StartDate</span></span>
<span data-ttu-id="3995d-150">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="3995d-151">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-151">The default start date value is today.</span></span> <span data-ttu-id="3995d-152">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3995d-153">-확인</span><span class="sxs-lookup"><span data-stu-id="3995d-153">-Confirm</span></span>
<span data-ttu-id="3995d-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3995d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3995d-155">-WhatIf</span></span>
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

### <span data-ttu-id="3995d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3995d-156">-DefaultProfile</span></span>
<span data-ttu-id="3995d-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3995d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3995d-158">CommonParameters</span></span>
<span data-ttu-id="3995d-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3995d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3995d-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3995d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3995d-161">입력</span><span class="sxs-lookup"><span data-stu-id="3995d-161">INPUTS</span></span>

## <span data-ttu-id="3995d-162">출력</span><span class="sxs-lookup"><span data-stu-id="3995d-162">OUTPUTS</span></span>

### <span data-ttu-id="3995d-163">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal</span><span class="sxs-lookup"><span data-stu-id="3995d-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3995d-164">상속자</span><span class="sxs-lookup"><span data-stu-id="3995d-164">NOTES</span></span>
<span data-ttu-id="3995d-165">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="3995d-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3995d-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3995d-166">RELATED LINKS</span></span>

[<span data-ttu-id="3995d-167">제거-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3995d-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3995d-168">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3995d-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3995d-169">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3995d-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="3995d-170">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3995d-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="3995d-171">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3995d-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="3995d-172">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3995d-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="3995d-173">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3995d-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

