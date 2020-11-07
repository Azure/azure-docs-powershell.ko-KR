---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: 814da56d9b925e19deac81dad886604d562e05e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711500"
---
# <span data-ttu-id="84bc0-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84bc0-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="84bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="84bc0-103">기존 서비스 사용자에 게 자격 증명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84bc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84bc0-104">SYNTAX</span></span>

### <span data-ttu-id="84bc0-105">SpObjectIdWithPasswordParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="84bc0-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84bc0-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="84bc0-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84bc0-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="84bc0-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84bc0-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="84bc0-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84bc0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="84bc0-109">DESCRIPTION</span></span>
<span data-ttu-id="84bc0-110">New-AzureRmADSpCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 서비스 사용자를 위해 자격 증명을 롤백할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="84bc0-111">서비스 사용자는 개체 id 또는 서비스 사용자 이름 중 하나를 제공 하 여 식별 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="84bc0-112">예제의</span><span class="sxs-lookup"><span data-stu-id="84bc0-112">EXAMPLES</span></span>

### <span data-ttu-id="84bc0-113">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="84bc0-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password "P@ssw0rd!"
```

<span data-ttu-id="84bc0-114">새 암호 자격 증명이 기존 서비스 주체에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="84bc0-115">이 예제에서는 제공 된 암호 값이 objectId를 사용 하 여 서비스 사용자에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="84bc0-116">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="84bc0-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="84bc0-117">새 키 자격 증명이 기존 서비스 주체에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="84bc0-118">이 예제에서는 제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")를 SPN을 사용 하 여 서비스 사용자에 게 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="84bc0-119">--------------------------예제 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="84bc0-119">--------------------------  Example 3  --------------------------</span></span>
<span data-ttu-id="84bc0-120">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="84bc0-120">@{paragraph=PS C:\\\>}</span></span>







```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="84bc0-121">변수</span><span class="sxs-lookup"><span data-stu-id="84bc0-121">PARAMETERS</span></span>

### <span data-ttu-id="84bc0-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="84bc0-122">-CertValue</span></span>
<span data-ttu-id="84bc0-123">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="84bc0-124">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="84bc0-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="84bc0-125">-EndDate</span></span>
<span data-ttu-id="84bc0-126">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="84bc0-127">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-127">The default end date value is one year from today.</span></span> <span data-ttu-id="84bc0-128">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="84bc0-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="84bc0-129">-ObjectId</span></span>
<span data-ttu-id="84bc0-130">자격 증명을 추가할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-130">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="84bc0-131">-암호</span><span class="sxs-lookup"><span data-stu-id="84bc0-131">-Password</span></span>
<span data-ttu-id="84bc0-132">응용 프로그램과 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-132">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bc0-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="84bc0-133">-ServicePrincipalName</span></span>
<span data-ttu-id="84bc0-134">자격 증명을 추가할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="84bc0-135">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="84bc0-135">-StartDate</span></span>
<span data-ttu-id="84bc0-136">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-136">The effective start date of the credential usage.</span></span>
<span data-ttu-id="84bc0-137">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-137">The default start date value is today.</span></span> <span data-ttu-id="84bc0-138">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-138">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="84bc0-139">-확인</span><span class="sxs-lookup"><span data-stu-id="84bc0-139">-Confirm</span></span>
<span data-ttu-id="84bc0-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84bc0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84bc0-141">-WhatIf</span></span>
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

### <span data-ttu-id="84bc0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bc0-142">-DefaultProfile</span></span>
<span data-ttu-id="84bc0-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84bc0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bc0-144">CommonParameters</span></span>
<span data-ttu-id="84bc0-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84bc0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bc0-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bc0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bc0-147">입력</span><span class="sxs-lookup"><span data-stu-id="84bc0-147">INPUTS</span></span>

## <span data-ttu-id="84bc0-148">출력</span><span class="sxs-lookup"><span data-stu-id="84bc0-148">OUTPUTS</span></span>

### <span data-ttu-id="84bc0-149">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adcredential</span><span class="sxs-lookup"><span data-stu-id="84bc0-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="84bc0-150">상속자</span><span class="sxs-lookup"><span data-stu-id="84bc0-150">NOTES</span></span>

## <span data-ttu-id="84bc0-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84bc0-151">RELATED LINKS</span></span>

[<span data-ttu-id="84bc0-152">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84bc0-152">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="84bc0-153">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="84bc0-153">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="84bc0-154">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="84bc0-154">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



