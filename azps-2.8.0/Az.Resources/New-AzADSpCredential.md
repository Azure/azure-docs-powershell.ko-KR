---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: af2eb05e627af1b88948b2c1be0229eb6680254c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871814"
---
# <span data-ttu-id="13015-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13015-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="13015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13015-102">SYNOPSIS</span></span>
<span data-ttu-id="13015-103">기존 서비스 사용자에 게 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="13015-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="13015-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13015-104">SYNTAX</span></span>

### <span data-ttu-id="13015-105">SpObjectIdWithPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="13015-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13015-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="13015-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13015-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="13015-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13015-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="13015-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13015-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="13015-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13015-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="13015-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13015-111">설명은</span><span class="sxs-lookup"><span data-stu-id="13015-111">DESCRIPTION</span></span>
<span data-ttu-id="13015-112">New-AzADSpCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 서비스 사용자를 위해 자격 증명을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13015-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="13015-113">서비스 사용자는 개체 id 또는 서비스 사용자 이름 중 하나를 제공 하 여 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13015-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="13015-114">예제의</span><span class="sxs-lookup"><span data-stu-id="13015-114">EXAMPLES</span></span>

### <span data-ttu-id="13015-115">예제 1-생성 된 암호를 사용 하 여 새 서비스 사용자 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="13015-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="13015-116">새 암호 자격 증명이 개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 기존 서비스 계정에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13015-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="13015-117">예제 2-인증서를 사용 하 여 새 서비스 사용자 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="13015-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="13015-118">제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")는 해당 SPN을 사용 하 여 기존 서비스 주체에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13015-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="13015-119">예제 3-파이핑을 사용 하 여 새 서비스 사용자 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="13015-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="13015-120">개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 서비스 사용자를 가져오고 생성 된 암호를 사용 하 여 해당 서비스 사용자에 대 한 새 서비스 사용자 자격 증명을 만들기 위해 New-AzADSpCredential에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13015-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="13015-121">변수</span><span class="sxs-lookup"><span data-stu-id="13015-121">PARAMETERS</span></span>

### <span data-ttu-id="13015-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="13015-122">-CertValue</span></span>
<span data-ttu-id="13015-123">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="13015-124">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13015-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="13015-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13015-125">-DefaultProfile</span></span>
<span data-ttu-id="13015-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="13015-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13015-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="13015-127">-EndDate</span></span>
<span data-ttu-id="13015-128">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="13015-129">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="13015-130">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13015-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="13015-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="13015-131">-ObjectId</span></span>
<span data-ttu-id="13015-132">자격 증명을 추가할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="13015-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="13015-133">-ServicePrincipalName</span></span>
<span data-ttu-id="13015-134">자격 증명을 추가할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="13015-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="13015-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="13015-136">자격 증명을 추가할 서비스 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="13015-137">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="13015-137">-StartDate</span></span>
<span data-ttu-id="13015-138">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="13015-139">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="13015-139">The default start date value is today.</span></span>
<span data-ttu-id="13015-140">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13015-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="13015-141">-확인</span><span class="sxs-lookup"><span data-stu-id="13015-141">-Confirm</span></span>
<span data-ttu-id="13015-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13015-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13015-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13015-143">-WhatIf</span></span>
<span data-ttu-id="13015-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13015-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13015-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13015-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13015-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13015-146">CommonParameters</span></span>
<span data-ttu-id="13015-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13015-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13015-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13015-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13015-149">입력</span><span class="sxs-lookup"><span data-stu-id="13015-149">INPUTS</span></span>

### <span data-ttu-id="13015-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13015-150">System.String</span></span>

### <span data-ttu-id="13015-151">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="13015-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="13015-152">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="13015-152">System.DateTime</span></span>

## <span data-ttu-id="13015-153">출력</span><span class="sxs-lookup"><span data-stu-id="13015-153">OUTPUTS</span></span>

### <span data-ttu-id="13015-154">ActiveDirectory Adcredential 자격 증명</span><span class="sxs-lookup"><span data-stu-id="13015-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="13015-155">Microsoft. a. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="13015-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="13015-156">상속자</span><span class="sxs-lookup"><span data-stu-id="13015-156">NOTES</span></span>

## <span data-ttu-id="13015-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13015-157">RELATED LINKS</span></span>

[<span data-ttu-id="13015-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13015-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="13015-159">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13015-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="13015-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="13015-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



