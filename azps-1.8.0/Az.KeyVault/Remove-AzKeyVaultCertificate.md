---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: 3e2da64d467d71721255afa12211530e7c0d9f08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867937"
---
# <span data-ttu-id="efd34-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="efd34-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="efd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd34-102">SYNOPSIS</span></span>
<span data-ttu-id="efd34-103">키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="efd34-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efd34-104">SYNTAX</span></span>

### <span data-ttu-id="efd34-105">ByVaultNameAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="efd34-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd34-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="efd34-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd34-107">설명은</span><span class="sxs-lookup"><span data-stu-id="efd34-107">DESCRIPTION</span></span>
<span data-ttu-id="efd34-108">**AzKeyVaultCertificate** cmdlet은 키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="efd34-109">예제의</span><span class="sxs-lookup"><span data-stu-id="efd34-109">EXAMPLES</span></span>

### <span data-ttu-id="efd34-110">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="efd34-110">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="efd34-111">이 명령은 ContosoKV01 이라는 키 자격 증명 모음에서 SelfSigned01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="efd34-112">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="efd34-113">따라서 cmdlet에서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="efd34-114">예제 2: 키 자격 증명 모음에서 삭제 된 인증서 영구 제거</span><span class="sxs-lookup"><span data-stu-id="efd34-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="efd34-115">이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 ' MyCert ' 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="efd34-116">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며,이는 이전에이 키 보관소의 사용자에 게 명시적으로 부여 된 것 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="efd34-117">변수</span><span class="sxs-lookup"><span data-stu-id="efd34-117">PARAMETERS</span></span>

### <span data-ttu-id="efd34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd34-118">-DefaultProfile</span></span>
<span data-ttu-id="efd34-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="efd34-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efd34-120">-Force</span><span class="sxs-lookup"><span data-stu-id="efd34-120">-Force</span></span>
<span data-ttu-id="efd34-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efd34-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efd34-122">-InputObject</span></span>
<span data-ttu-id="efd34-123">인증서 개체.</span><span class="sxs-lookup"><span data-stu-id="efd34-123">Certificate Object.</span></span>

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

### <span data-ttu-id="efd34-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="efd34-124">-InRemovedState</span></span>
<span data-ttu-id="efd34-125">있는 경우 이전에 삭제 된 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="efd34-126">-이름</span><span class="sxs-lookup"><span data-stu-id="efd34-126">-Name</span></span>
<span data-ttu-id="efd34-127">이 cmdlet이 키 자격 증명 모음에서 제거할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="efd34-128">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="efd34-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efd34-129">-PassThru</span></span>
<span data-ttu-id="efd34-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="efd34-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efd34-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="efd34-132">-VaultName</span></span>
<span data-ttu-id="efd34-133">이 cmdlet이 인증서를 제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="efd34-134">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="efd34-135">-확인</span><span class="sxs-lookup"><span data-stu-id="efd34-135">-Confirm</span></span>
<span data-ttu-id="efd34-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd34-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd34-137">-WhatIf</span></span>
<span data-ttu-id="efd34-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd34-139">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd34-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd34-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd34-141">CommonParameters</span></span>
<span data-ttu-id="efd34-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd34-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd34-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd34-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd34-144">입력</span><span class="sxs-lookup"><span data-stu-id="efd34-144">INPUTS</span></span>

### <span data-ttu-id="efd34-145">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="efd34-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="efd34-146">출력</span><span class="sxs-lookup"><span data-stu-id="efd34-146">OUTPUTS</span></span>

### <span data-ttu-id="efd34-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="efd34-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="efd34-148">상속자</span><span class="sxs-lookup"><span data-stu-id="efd34-148">NOTES</span></span>

## <span data-ttu-id="efd34-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efd34-149">RELATED LINKS</span></span>

[<span data-ttu-id="efd34-150">추가-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="efd34-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="efd34-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="efd34-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="efd34-152">가져오기-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="efd34-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="efd34-153">실행 취소-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="efd34-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
