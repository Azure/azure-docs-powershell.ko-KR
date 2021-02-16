---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199993"
---
# <span data-ttu-id="e4603-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e4603-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e4603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4603-102">SYNOPSIS</span></span>
<span data-ttu-id="e4603-103">키 자격 증명 모음에서 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="e4603-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4603-104">SYNTAX</span></span>

### <span data-ttu-id="e4603-105">ByVaultNameAndName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e4603-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4603-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e4603-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4603-107">설명</span><span class="sxs-lookup"><span data-stu-id="e4603-107">DESCRIPTION</span></span>
<span data-ttu-id="e4603-108">**Remove-AzKeyVaultCertificate** cmdlet은 키 자격 증명 모음에서 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="e4603-109">예제</span><span class="sxs-lookup"><span data-stu-id="e4603-109">EXAMPLES</span></span>

### <span data-ttu-id="e4603-110">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="e4603-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="e4603-111">이 명령은 ContosoKV01이라는 키 자격 증명 모음에서 SelfSigned01이라는 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="e4603-112">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="e4603-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e4603-113">따라서 cmdlet은 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e4603-114">예제 2: Key Vault에서 삭제된 인증서를 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="e4603-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="e4603-115">이 명령은 'Contoso'라는 키 자격 증명 모음에서 'MyCert'라는 인증서를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="e4603-116">이 cmdlet을 실행하려면 이전에 이 키 자격 증명 모음의 사용자에게 명시적으로 부여된 '제거' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="e4603-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4603-117">PARAMETERS</span></span>

### <span data-ttu-id="e4603-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4603-118">-DefaultProfile</span></span>
<span data-ttu-id="e4603-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4603-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4603-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e4603-120">-Force</span></span>
<span data-ttu-id="e4603-121">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4603-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4603-122">-InputObject</span></span>
<span data-ttu-id="e4603-123">인증서 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4603-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="e4603-124">-InRemovedState</span></span>
<span data-ttu-id="e4603-125">있는 경우 이전에 삭제된 인증서를 영구적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="e4603-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e4603-126">-Name</span></span>
<span data-ttu-id="e4603-127">이 cmdlet이 키 자격 증명 모음에서 제거하는 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="e4603-128">이 cmdlet은 이 매개 변수가 지정하는 이름, 키 자격 증명 모음의 이름 및 현재 환경에 따라 인증서의 FQDN(정식 도메인 이름)을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4603-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4603-129">-PassThru</span></span>
<span data-ttu-id="e4603-130">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4603-131">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4603-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e4603-132">-VaultName</span></span>
<span data-ttu-id="e4603-133">이 cmdlet이 인증서를 제거하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="e4603-134">이 cmdlet은 이 매개 변수가 지정하는 이름 및 현재 환경에 따라 키 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4603-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4603-135">-Confirm</span></span>
<span data-ttu-id="e4603-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4603-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4603-137">-WhatIf</span></span>
<span data-ttu-id="e4603-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e4603-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4603-139">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e4603-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4603-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4603-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4603-141">CommonParameters</span></span>
<span data-ttu-id="e4603-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4603-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4603-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4603-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4603-144">입력</span><span class="sxs-lookup"><span data-stu-id="e4603-144">INPUTS</span></span>

### <span data-ttu-id="e4603-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e4603-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="e4603-146">출력</span><span class="sxs-lookup"><span data-stu-id="e4603-146">OUTPUTS</span></span>

### <span data-ttu-id="e4603-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e4603-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="e4603-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4603-148">NOTES</span></span>

## <span data-ttu-id="e4603-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4603-149">RELATED LINKS</span></span>

[<span data-ttu-id="e4603-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e4603-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="e4603-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e4603-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="e4603-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e4603-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="e4603-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="e4603-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
