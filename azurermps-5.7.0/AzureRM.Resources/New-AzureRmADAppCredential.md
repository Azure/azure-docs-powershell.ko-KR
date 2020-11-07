---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703228"
---
# <span data-ttu-id="46b46-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46b46-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="46b46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b46-102">SYNOPSIS</span></span>
<span data-ttu-id="46b46-103">기존 응용 프로그램에 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46b46-104">SYNTAX</span></span>

### <span data-ttu-id="46b46-105">ApplicationObjectIdWithPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="46b46-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b46-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b46-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b46-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b46-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b46-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b46-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b46-109">설명은</span><span class="sxs-lookup"><span data-stu-id="46b46-109">DESCRIPTION</span></span>
<span data-ttu-id="46b46-110">New-AzureRmADAppCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 응용 프로그램에 대 한 자격 증명을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="46b46-111">응용 프로그램은 응용 프로그램 개체 id 또는 응용 프로그램 Id 중 하나를 제공 하 여 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="46b46-112">예제의</span><span class="sxs-lookup"><span data-stu-id="46b46-112">EXAMPLES</span></span>

### <span data-ttu-id="46b46-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="46b46-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="46b46-114">새 암호 자격 증명이 기존 응용 프로그램에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="46b46-115">이 예제에서는 제공 된 암호 값이 응용 프로그램 개체 id를 사용 하 여 응용 프로그램에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="46b46-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="46b46-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="46b46-117">기존 응용 프로그램에 새 키 자격 증명이 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="46b46-118">이 예제에서는 제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")가 applicationId를 사용 하 여 응용 프로그램에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="46b46-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="46b46-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="46b46-120">변수</span><span class="sxs-lookup"><span data-stu-id="46b46-120">PARAMETERS</span></span>

### <span data-ttu-id="46b46-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="46b46-121">-ApplicationId</span></span>
<span data-ttu-id="46b46-122">자격 증명을 추가할 응용 프로그램의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="46b46-123">-CertValue</span></span>
<span data-ttu-id="46b46-124">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="46b46-125">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b46-126">-DefaultProfile</span></span>
<span data-ttu-id="46b46-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46b46-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46b46-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="46b46-128">-EndDate</span></span>
<span data-ttu-id="46b46-129">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="46b46-130">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-130">The default end date value is one year from today.</span></span> <span data-ttu-id="46b46-131">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="46b46-132">-ObjectId</span></span>
<span data-ttu-id="46b46-133">자격 증명을 추가할 응용 프로그램의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-134">-암호</span><span class="sxs-lookup"><span data-stu-id="46b46-134">-Password</span></span>
<span data-ttu-id="46b46-135">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-136">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="46b46-136">-StartDate</span></span>
<span data-ttu-id="46b46-137">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="46b46-138">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-138">The default start date value is today.</span></span>
<span data-ttu-id="46b46-139">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46b46-140">-확인</span><span class="sxs-lookup"><span data-stu-id="46b46-140">-Confirm</span></span>
<span data-ttu-id="46b46-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b46-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b46-142">-WhatIf</span></span>
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

### <span data-ttu-id="46b46-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b46-143">CommonParameters</span></span>
<span data-ttu-id="46b46-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b46-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b46-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b46-146">입력</span><span class="sxs-lookup"><span data-stu-id="46b46-146">INPUTS</span></span>

### <span data-ttu-id="46b46-147">않아야</span><span class="sxs-lookup"><span data-stu-id="46b46-147">None</span></span>
<span data-ttu-id="46b46-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46b46-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46b46-149">출력</span><span class="sxs-lookup"><span data-stu-id="46b46-149">OUTPUTS</span></span>

### <span data-ttu-id="46b46-150">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="46b46-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="46b46-151">상속자</span><span class="sxs-lookup"><span data-stu-id="46b46-151">NOTES</span></span>

## <span data-ttu-id="46b46-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46b46-152">RELATED LINKS</span></span>

[<span data-ttu-id="46b46-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46b46-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="46b46-154">제거-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="46b46-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="46b46-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="46b46-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

