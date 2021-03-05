---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 33c274154e122c0bb0925b8381d2dd51cad18264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960731"
---
# <span data-ttu-id="29cdb-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29cdb-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="29cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="29cdb-103">키 자격 증명 모음에서 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="29cdb-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="29cdb-104">구문</span><span class="sxs-lookup"><span data-stu-id="29cdb-104">SYNTAX</span></span>

### <span data-ttu-id="29cdb-105">확장(기본값)</span><span class="sxs-lookup"><span data-stu-id="29cdb-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29cdb-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="29cdb-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cdb-107">설명</span><span class="sxs-lookup"><span data-stu-id="29cdb-107">DESCRIPTION</span></span>
<span data-ttu-id="29cdb-108">Set-AzKeyVaultCertificateIssuer cmdlet은 키 자격 증명 모음에 인증서 발급자 를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="29cdb-109">예제</span><span class="sxs-lookup"><span data-stu-id="29cdb-109">EXAMPLES</span></span>

### <span data-ttu-id="29cdb-110">예제 1: 인증서 발급자 설정</span><span class="sxs-lookup"><span data-stu-id="29cdb-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="29cdb-111">이 명령은 인증서 발급자에 대한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="29cdb-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="29cdb-112">PARAMETERS</span></span>

### <span data-ttu-id="29cdb-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="29cdb-113">-AccountId</span></span>
<span data-ttu-id="29cdb-114">인증서 발급자에 대한 계정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="29cdb-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="29cdb-115">-ApiKey</span></span>
<span data-ttu-id="29cdb-116">인증서 발급자에 대한 API 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="29cdb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cdb-117">-DefaultProfile</span></span>
<span data-ttu-id="29cdb-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="29cdb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29cdb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29cdb-119">-InputObject</span></span>
<span data-ttu-id="29cdb-120">설정할 인증서 발급자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="29cdb-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="29cdb-121">-IssuerProvider</span></span>
<span data-ttu-id="29cdb-122">인증서 발급자 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="29cdb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="29cdb-123">-Name</span></span>
<span data-ttu-id="29cdb-124">발급자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="29cdb-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="29cdb-125">-OrganizationDetails</span></span>
<span data-ttu-id="29cdb-126">발급자에 사용할 조직 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="29cdb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29cdb-127">-PassThru</span></span>
<span data-ttu-id="29cdb-128">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29cdb-129">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29cdb-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="29cdb-130">-VaultName</span></span>
<span data-ttu-id="29cdb-131">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="29cdb-132">-확인</span><span class="sxs-lookup"><span data-stu-id="29cdb-132">-Confirm</span></span>
<span data-ttu-id="29cdb-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29cdb-134">-WhatIf</span></span>
<span data-ttu-id="29cdb-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cdb-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cdb-137">CommonParameters</span></span>
<span data-ttu-id="29cdb-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29cdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cdb-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29cdb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cdb-140">입력</span><span class="sxs-lookup"><span data-stu-id="29cdb-140">INPUTS</span></span>

### <span data-ttu-id="29cdb-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="29cdb-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="29cdb-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29cdb-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="29cdb-143">출력</span><span class="sxs-lookup"><span data-stu-id="29cdb-143">OUTPUTS</span></span>

### <span data-ttu-id="29cdb-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="29cdb-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="29cdb-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29cdb-145">NOTES</span></span>

## <span data-ttu-id="29cdb-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29cdb-146">RELATED LINKS</span></span>

[<span data-ttu-id="29cdb-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29cdb-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="29cdb-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="29cdb-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

