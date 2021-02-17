---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208480"
---
# <span data-ttu-id="30198-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="30198-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="30198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30198-102">SYNOPSIS</span></span>
<span data-ttu-id="30198-103">기존 서비스 주체에 자격 증명을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="30198-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="30198-104">구문</span><span class="sxs-lookup"><span data-stu-id="30198-104">SYNTAX</span></span>

### <span data-ttu-id="30198-105">SpObjectIdWithPasswordParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="30198-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30198-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="30198-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30198-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="30198-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30198-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="30198-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30198-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="30198-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30198-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="30198-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30198-111">설명</span><span class="sxs-lookup"><span data-stu-id="30198-111">DESCRIPTION</span></span>
<span data-ttu-id="30198-112">이 New-AzADSpCredential cmdlet을 사용하여 새 자격 증명을 추가하거나 서비스 주체에 대한 자격 증명을 롤링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30198-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="30198-113">서비스 주체는 개체 ID 또는 서비스 주체 이름을 입력하여 식별됩니다.</span><span class="sxs-lookup"><span data-stu-id="30198-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="30198-114">예제</span><span class="sxs-lookup"><span data-stu-id="30198-114">EXAMPLES</span></span>

### <span data-ttu-id="30198-115">예제 1: 생성된 암호를 사용하여 새 서비스 주체 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="30198-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="30198-116">개체 ID가 '1f99cf81-0146-4f4e-beae-2007d0668476'인 기존 서비스 주체에 새 암호 자격 증명이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="30198-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="30198-117">예제 2: 인증서를 사용하여 새 서비스 주체 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="30198-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="30198-118">제공된 base64로 인코딩된 공용 X509 인증서("myapp.cer")는 SPN을 사용하여 기존 서비스 주체에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="30198-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="30198-119">예제 3: 파이핑을 사용하여 새 서비스 주체 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="30198-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="30198-120">개체 ID가 '1f99cf81-0146-4f4e-beae-2007d0668476'인 서비스 주체를 New-AzADSpCredential 생성된 암호로 해당 서비스 주체에 대한 새 서비스 주체 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30198-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="30198-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30198-121">PARAMETERS</span></span>

### <span data-ttu-id="30198-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="30198-122">-CertValue</span></span>
<span data-ttu-id="30198-123">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="30198-124">기본 64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="30198-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30198-125">-DefaultProfile</span></span>
<span data-ttu-id="30198-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30198-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30198-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="30198-127">-EndDate</span></span>
<span data-ttu-id="30198-128">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="30198-129">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="30198-130">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30198-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30198-131">-ObjectId</span></span>
<span data-ttu-id="30198-132">자격 증명을 추가할 서비스 주체의 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="30198-133">-ServicePrincipalName</span></span>
<span data-ttu-id="30198-134">자격 증명을 추가할 서비스 주체의 SPN(이름)</span><span class="sxs-lookup"><span data-stu-id="30198-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="30198-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="30198-136">자격 증명을 추가할 서비스 주체 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="30198-137">-StartDate</span></span>
<span data-ttu-id="30198-138">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="30198-139">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="30198-139">The default start date value is today.</span></span>
<span data-ttu-id="30198-140">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30198-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30198-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30198-141">-Confirm</span></span>
<span data-ttu-id="30198-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30198-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30198-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30198-143">-WhatIf</span></span>
<span data-ttu-id="30198-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="30198-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30198-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30198-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30198-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30198-146">CommonParameters</span></span>
<span data-ttu-id="30198-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30198-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30198-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30198-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30198-149">입력</span><span class="sxs-lookup"><span data-stu-id="30198-149">INPUTS</span></span>

### <span data-ttu-id="30198-150">System.String</span><span class="sxs-lookup"><span data-stu-id="30198-150">System.String</span></span>

### <span data-ttu-id="30198-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30198-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="30198-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="30198-152">System.DateTime</span></span>

## <span data-ttu-id="30198-153">출력</span><span class="sxs-lookup"><span data-stu-id="30198-153">OUTPUTS</span></span>

### <span data-ttu-id="30198-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="30198-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="30198-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="30198-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="30198-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30198-156">NOTES</span></span>

## <span data-ttu-id="30198-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30198-157">RELATED LINKS</span></span>

[<span data-ttu-id="30198-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="30198-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="30198-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="30198-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="30198-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30198-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



