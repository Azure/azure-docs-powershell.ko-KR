---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: fdb90d670034e87c4a08c316b73d4bd15614d872
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689612"
---
# <span data-ttu-id="06c7a-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="06c7a-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="06c7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="06c7a-103">키 자격 증명 모음에서 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="06c7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06c7a-104">SYNTAX</span></span>

### <span data-ttu-id="06c7a-105">확장 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="06c7a-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06c7a-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="06c7a-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06c7a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06c7a-107">DESCRIPTION</span></span>
<span data-ttu-id="06c7a-108">Set-AzKeyVaultCertificateIssuer cmdlet은 키 자격 증명 모음에 인증서 발급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="06c7a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06c7a-109">EXAMPLES</span></span>

### <span data-ttu-id="06c7a-110">예제 1: 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="06c7a-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="06c7a-111">이 명령은 인증서 발급자에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="06c7a-112">변수</span><span class="sxs-lookup"><span data-stu-id="06c7a-112">PARAMETERS</span></span>

### <span data-ttu-id="06c7a-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="06c7a-113">-AccountId</span></span>
<span data-ttu-id="06c7a-114">인증서 발급자의 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="06c7a-115">-ApiKey</span></span>
<span data-ttu-id="06c7a-116">인증서 발급자에 대 한 API 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c7a-117">-DefaultProfile</span></span>
<span data-ttu-id="06c7a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06c7a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06c7a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06c7a-119">-InputObject</span></span>
<span data-ttu-id="06c7a-120">설정할 인증서 발급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="06c7a-121">-IssuerProvider</span></span>
<span data-ttu-id="06c7a-122">인증서 발급자 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="06c7a-123">-Name</span></span>
<span data-ttu-id="06c7a-124">발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="06c7a-125">-OrganizationDetails</span></span>
<span data-ttu-id="06c7a-126">발급자와 함께 사용할 조직 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06c7a-127">-PassThru</span></span>
<span data-ttu-id="06c7a-128">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06c7a-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06c7a-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="06c7a-130">-VaultName</span></span>
<span data-ttu-id="06c7a-131">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06c7a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="06c7a-132">-Confirm</span></span>
<span data-ttu-id="06c7a-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06c7a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06c7a-134">-WhatIf</span></span>
<span data-ttu-id="06c7a-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06c7a-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06c7a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c7a-137">CommonParameters</span></span>
<span data-ttu-id="06c7a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06c7a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c7a-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c7a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c7a-140">입력</span><span class="sxs-lookup"><span data-stu-id="06c7a-140">INPUTS</span></span>

### <span data-ttu-id="06c7a-141">Microsoft. KeyVault. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="06c7a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="06c7a-142">Microsoft. KeyVault. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="06c7a-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="06c7a-143">출력</span><span class="sxs-lookup"><span data-stu-id="06c7a-143">OUTPUTS</span></span>

### <span data-ttu-id="06c7a-144">Microsoft. KeyVault. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="06c7a-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="06c7a-145">상속자</span><span class="sxs-lookup"><span data-stu-id="06c7a-145">NOTES</span></span>

## <span data-ttu-id="06c7a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06c7a-146">RELATED LINKS</span></span>

[<span data-ttu-id="06c7a-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="06c7a-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="06c7a-148">제거-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="06c7a-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)
