---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532247"
---
# <span data-ttu-id="7a885-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="7a885-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="7a885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a885-102">SYNOPSIS</span></span>
<span data-ttu-id="7a885-103">키 자격 증명 모음에서 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a885-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a885-104">SYNTAX</span></span>

### <span data-ttu-id="7a885-105">확장 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7a885-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a885-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="7a885-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a885-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7a885-107">DESCRIPTION</span></span>
<span data-ttu-id="7a885-108">Set-AzureKeyVaultCertificateIssuer cmdlet은 키 자격 증명 모음에 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="7a885-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7a885-109">EXAMPLES</span></span>

### <span data-ttu-id="7a885-110">예제 1: 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="7a885-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="7a885-111">이 명령은 인증서 발급자의 속성을 설정한 다음 $Issuer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="7a885-112">변수</span><span class="sxs-lookup"><span data-stu-id="7a885-112">PARAMETERS</span></span>

### <span data-ttu-id="7a885-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="7a885-113">-AccountId</span></span>
<span data-ttu-id="7a885-114">인증서 발급자의 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="7a885-115">-ApiKey</span></span>
<span data-ttu-id="7a885-116">인증서 발급자에 대 한 API 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-117">발급자</span><span class="sxs-lookup"><span data-stu-id="7a885-117">-Issuer</span></span>
<span data-ttu-id="7a885-118">업데이트할 인증서 발급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="7a885-119">-IssuerProvider</span></span>
<span data-ttu-id="7a885-120">인증서 발급자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7a885-121">-Name</span></span>
<span data-ttu-id="7a885-122">발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="7a885-123">-OrganizationDetails</span></span>
<span data-ttu-id="7a885-124">발급자와 함께 사용할 조직 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a885-125">-PassThru</span></span>
<span data-ttu-id="7a885-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a885-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7a885-128">-VaultName</span></span>
<span data-ttu-id="7a885-129">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-129">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a885-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7a885-130">-Confirm</span></span>
<span data-ttu-id="7a885-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a885-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a885-132">-WhatIf</span></span>
<span data-ttu-id="7a885-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a885-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a885-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a885-135">-DefaultProfile</span></span>
<span data-ttu-id="7a885-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a885-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a885-137">CommonParameters</span></span>
<span data-ttu-id="7a885-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a885-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a885-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a885-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a885-140">입력</span><span class="sxs-lookup"><span data-stu-id="7a885-140">INPUTS</span></span>

## <span data-ttu-id="7a885-141">출력</span><span class="sxs-lookup"><span data-stu-id="7a885-141">OUTPUTS</span></span>

### <span data-ttu-id="7a885-142">Microsoft. KeyVault. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="7a885-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="7a885-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7a885-143">NOTES</span></span>

## <span data-ttu-id="7a885-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a885-144">RELATED LINKS</span></span>

[<span data-ttu-id="7a885-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="7a885-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="7a885-146">제거-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="7a885-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

