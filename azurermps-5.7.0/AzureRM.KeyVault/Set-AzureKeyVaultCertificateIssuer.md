---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536787"
---
# <span data-ttu-id="88653-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88653-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="88653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88653-102">SYNOPSIS</span></span>
<span data-ttu-id="88653-103">키 자격 증명 모음에서 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88653-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88653-104">SYNTAX</span></span>

### <span data-ttu-id="88653-105">확장 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="88653-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88653-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="88653-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88653-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88653-107">DESCRIPTION</span></span>
<span data-ttu-id="88653-108">Set-AzureKeyVaultCertificateIssuer cmdlet은 키 자격 증명 모음에 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="88653-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88653-109">EXAMPLES</span></span>

### <span data-ttu-id="88653-110">예제 1: 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="88653-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="88653-111">이 명령은 인증서 발급자의 속성을 설정한 다음 $Issuer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="88653-112">변수</span><span class="sxs-lookup"><span data-stu-id="88653-112">PARAMETERS</span></span>

### <span data-ttu-id="88653-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="88653-113">-AccountId</span></span>
<span data-ttu-id="88653-114">인증서 발급자의 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="88653-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="88653-115">-ApiKey</span></span>
<span data-ttu-id="88653-116">인증서 발급자에 대 한 API 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="88653-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88653-117">-DefaultProfile</span></span>
<span data-ttu-id="88653-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88653-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88653-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88653-119">-InputObject</span></span>
<span data-ttu-id="88653-120">설정할 인증서 발급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88653-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="88653-121">-IssuerProvider</span></span>
<span data-ttu-id="88653-122">인증서 발급자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="88653-123">-이름</span><span class="sxs-lookup"><span data-stu-id="88653-123">-Name</span></span>
<span data-ttu-id="88653-124">발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="88653-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="88653-125">-OrganizationDetails</span></span>
<span data-ttu-id="88653-126">발급자와 함께 사용할 조직 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="88653-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88653-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88653-127">-PassThru</span></span>
<span data-ttu-id="88653-128">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="88653-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88653-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="88653-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="88653-130">-VaultName</span></span>
<span data-ttu-id="88653-131">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="88653-132">-확인</span><span class="sxs-lookup"><span data-stu-id="88653-132">-Confirm</span></span>
<span data-ttu-id="88653-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88653-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88653-134">-WhatIf</span></span>
<span data-ttu-id="88653-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88653-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88653-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88653-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88653-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88653-137">CommonParameters</span></span>
<span data-ttu-id="88653-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88653-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88653-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88653-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88653-140">입력</span><span class="sxs-lookup"><span data-stu-id="88653-140">INPUTS</span></span>

### <span data-ttu-id="88653-141">않아야</span><span class="sxs-lookup"><span data-stu-id="88653-141">None</span></span>
<span data-ttu-id="88653-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88653-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88653-143">출력</span><span class="sxs-lookup"><span data-stu-id="88653-143">OUTPUTS</span></span>

### <span data-ttu-id="88653-144">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="88653-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="88653-145">상속자</span><span class="sxs-lookup"><span data-stu-id="88653-145">NOTES</span></span>

## <span data-ttu-id="88653-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88653-146">RELATED LINKS</span></span>

[<span data-ttu-id="88653-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88653-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="88653-148">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="88653-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

