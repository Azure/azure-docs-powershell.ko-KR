---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531668"
---
# <span data-ttu-id="a8350-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8350-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="a8350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8350-102">SYNOPSIS</span></span>
<span data-ttu-id="a8350-103">기존 서비스 사용자에 게 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8350-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8350-104">SYNTAX</span></span>

### <span data-ttu-id="a8350-105">SpObjectIdWithPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8350-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8350-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8350-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8350-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8350-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8350-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8350-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8350-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a8350-109">DESCRIPTION</span></span>
<span data-ttu-id="a8350-110">New-AzureRmADSpCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 서비스 사용자를 위해 자격 증명을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="a8350-111">서비스 사용자는 개체 id 또는 서비스 사용자 이름 중 하나를 제공 하 여 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="a8350-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a8350-112">EXAMPLES</span></span>

### <span data-ttu-id="a8350-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a8350-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="a8350-114">새 암호 자격 증명이 기존 서비스 주체에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="a8350-115">이 예제에서는 제공 된 암호 값이 objectId를 사용 하 여 서비스 사용자에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="a8350-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="a8350-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="a8350-117">새 키 자격 증명이 기존 서비스 주체에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="a8350-118">이 예제에서는 제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")를 SPN을 사용 하 여 서비스 사용자에 게 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="a8350-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="a8350-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="a8350-120">변수</span><span class="sxs-lookup"><span data-stu-id="a8350-120">PARAMETERS</span></span>

### <span data-ttu-id="a8350-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a8350-121">-CertValue</span></span>
<span data-ttu-id="a8350-122">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a8350-123">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8350-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8350-124">-DefaultProfile</span></span>
<span data-ttu-id="a8350-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a8350-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8350-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a8350-126">-EndDate</span></span>
<span data-ttu-id="a8350-127">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a8350-128">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-128">The default end date value is one year from today.</span></span> <span data-ttu-id="a8350-129">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a8350-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a8350-130">-ObjectId</span></span>
<span data-ttu-id="a8350-131">자격 증명을 추가할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8350-132">-암호</span><span class="sxs-lookup"><span data-stu-id="a8350-132">-Password</span></span>
<span data-ttu-id="a8350-133">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8350-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8350-134">-ServicePrincipalName</span></span>
<span data-ttu-id="a8350-135">자격 증명을 추가할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8350-136">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="a8350-136">-StartDate</span></span>
<span data-ttu-id="a8350-137">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a8350-138">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-138">The default start date value is today.</span></span> <span data-ttu-id="a8350-139">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a8350-140">-확인</span><span class="sxs-lookup"><span data-stu-id="a8350-140">-Confirm</span></span>
<span data-ttu-id="a8350-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8350-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8350-142">-WhatIf</span></span>
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

### <span data-ttu-id="a8350-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8350-143">CommonParameters</span></span>
<span data-ttu-id="a8350-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8350-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8350-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8350-146">입력</span><span class="sxs-lookup"><span data-stu-id="a8350-146">INPUTS</span></span>

### <span data-ttu-id="a8350-147">않아야</span><span class="sxs-lookup"><span data-stu-id="a8350-147">None</span></span>
<span data-ttu-id="a8350-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8350-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8350-149">출력</span><span class="sxs-lookup"><span data-stu-id="a8350-149">OUTPUTS</span></span>

### <span data-ttu-id="a8350-150">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="a8350-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="a8350-151">상속자</span><span class="sxs-lookup"><span data-stu-id="a8350-151">NOTES</span></span>

## <span data-ttu-id="a8350-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8350-152">RELATED LINKS</span></span>

[<span data-ttu-id="a8350-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8350-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a8350-154">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8350-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="a8350-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a8350-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



