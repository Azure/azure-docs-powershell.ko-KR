---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876694"
---
# <span data-ttu-id="fa9b3-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fa9b3-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="fa9b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9b3-103">키 자격 증명 모음에서 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="fa9b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa9b3-104">SYNTAX</span></span>

### <span data-ttu-id="fa9b3-105">확장 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa9b3-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa9b3-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="fa9b3-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa9b3-107">DESCRIPTION</span></span>
<span data-ttu-id="fa9b3-108">Set-AzKeyVaultCertificateIssuer cmdlet은 키 자격 증명 모음에 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="fa9b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fa9b3-109">EXAMPLES</span></span>

### <span data-ttu-id="fa9b3-110">예제 1: 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="fa9b3-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="fa9b3-111">이 명령은 인증서 발급자의 속성을 설정한 다음 $Issuer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="fa9b3-112">변수</span><span class="sxs-lookup"><span data-stu-id="fa9b3-112">PARAMETERS</span></span>

### <span data-ttu-id="fa9b3-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="fa9b3-113">-AccountId</span></span>
<span data-ttu-id="fa9b3-114">인증서 발급자의 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="fa9b3-115">-ApiKey</span></span>
<span data-ttu-id="fa9b3-116">인증서 발급자에 대 한 API 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9b3-117">-DefaultProfile</span></span>
<span data-ttu-id="fa9b3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fa9b3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-119">발급자</span><span class="sxs-lookup"><span data-stu-id="fa9b3-119">-Issuer</span></span>
<span data-ttu-id="fa9b3-120">업데이트할 인증서 발급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="fa9b3-121">-IssuerProvider</span></span>
<span data-ttu-id="fa9b3-122">인증서 발급자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fa9b3-123">-Name</span></span>
<span data-ttu-id="fa9b3-124">발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="fa9b3-125">-OrganizationDetails</span></span>
<span data-ttu-id="fa9b3-126">발급자와 함께 사용할 조직 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa9b3-127">-PassThru</span></span>
<span data-ttu-id="fa9b3-128">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa9b3-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fa9b3-130">-VaultName</span></span>
<span data-ttu-id="fa9b3-131">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-131">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa9b3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="fa9b3-132">-Confirm</span></span>
<span data-ttu-id="fa9b3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9b3-134">-WhatIf</span></span>
<span data-ttu-id="fa9b3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9b3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9b3-137">CommonParameters</span></span>
<span data-ttu-id="fa9b3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9b3-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9b3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9b3-140">입력</span><span class="sxs-lookup"><span data-stu-id="fa9b3-140">INPUTS</span></span>

### <span data-ttu-id="fa9b3-141">않아야</span><span class="sxs-lookup"><span data-stu-id="fa9b3-141">None</span></span>
<span data-ttu-id="fa9b3-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa9b3-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa9b3-143">출력</span><span class="sxs-lookup"><span data-stu-id="fa9b3-143">OUTPUTS</span></span>

### <span data-ttu-id="fa9b3-144">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="fa9b3-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="fa9b3-145">상속자</span><span class="sxs-lookup"><span data-stu-id="fa9b3-145">NOTES</span></span>

## <span data-ttu-id="fa9b3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa9b3-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa9b3-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fa9b3-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="fa9b3-148">제거-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="fa9b3-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

