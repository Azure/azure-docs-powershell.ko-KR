---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: e514ded413eaca5ae5992e452a6b35f78ab6532b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991083"
---
# <span data-ttu-id="d3989-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d3989-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="d3989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3989-102">SYNOPSIS</span></span>
<span data-ttu-id="d3989-103">키 자격 증명 모음에서 삭제된 인증서를 활성 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="d3989-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3989-104">SYNTAX</span></span>

### <span data-ttu-id="d3989-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3989-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3989-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d3989-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3989-107">설명</span><span class="sxs-lookup"><span data-stu-id="d3989-107">DESCRIPTION</span></span>
<span data-ttu-id="d3989-108">**Undo-AzKeyVaultCertificateRemoval** cmdlet은 이전에 삭제된 인증서를 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="d3989-109">복구된 인증서는 활성으로 모든 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="d3989-110">호출자에 이 작업을 수행하려면 '복구' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d3989-111">예제</span><span class="sxs-lookup"><span data-stu-id="d3989-111">EXAMPLES</span></span>

### <span data-ttu-id="d3989-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3989-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="d3989-113">이 명령은 이전에 삭제된 'MyCertificate' 인증서를 활성 상태 및 사용 가능한 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d3989-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3989-114">PARAMETERS</span></span>

### <span data-ttu-id="d3989-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3989-115">-DefaultProfile</span></span>
<span data-ttu-id="d3989-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d3989-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3989-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3989-117">-InputObject</span></span>
<span data-ttu-id="d3989-118">삭제된 인증서 개체</span><span class="sxs-lookup"><span data-stu-id="d3989-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3989-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d3989-119">-Name</span></span>
<span data-ttu-id="d3989-120">인증서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-120">Certificate name.</span></span>
<span data-ttu-id="d3989-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 인증서 이름에서 인증서의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3989-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d3989-122">-VaultName</span></span>
<span data-ttu-id="d3989-123">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-123">Vault name.</span></span>
<span data-ttu-id="d3989-124">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3989-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d3989-125">-Confirm</span></span>
<span data-ttu-id="d3989-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3989-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3989-127">-WhatIf</span></span>
<span data-ttu-id="d3989-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3989-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3989-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3989-130">CommonParameters</span></span>
<span data-ttu-id="d3989-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3989-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3989-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3989-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3989-133">입력</span><span class="sxs-lookup"><span data-stu-id="d3989-133">INPUTS</span></span>

### <span data-ttu-id="d3989-134">Microsoft.Azure.Commands.KeyVault.Models.PSDKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d3989-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="d3989-135">출력</span><span class="sxs-lookup"><span data-stu-id="d3989-135">OUTPUTS</span></span>

### <span data-ttu-id="d3989-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3989-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="d3989-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3989-137">NOTES</span></span>

## <span data-ttu-id="d3989-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3989-138">RELATED LINKS</span></span>

[<span data-ttu-id="d3989-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3989-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d3989-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d3989-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
