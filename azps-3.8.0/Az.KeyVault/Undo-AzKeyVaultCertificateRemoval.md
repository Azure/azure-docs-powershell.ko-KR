---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 7e9af7cd775726fc57b78f3fdead20f36dca13cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878282"
---
# <span data-ttu-id="3a9d0-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="3a9d0-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="3a9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9d0-103">키 자격 증명 모음에서 삭제 된 인증서를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="3a9d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a9d0-104">SYNTAX</span></span>

### <span data-ttu-id="3a9d0-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a9d0-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3a9d0-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3a9d0-107">DESCRIPTION</span></span>
<span data-ttu-id="3a9d0-108">AzKeyVaultCertificateRemoval cmdlet을 **실행** 하면 이전에 삭제 된 인증서가 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="3a9d0-109">복구 된 인증서는 활성화 되며 모든 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="3a9d0-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="3a9d0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3a9d0-111">EXAMPLES</span></span>

### <span data-ttu-id="3a9d0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a9d0-112">Example 1</span></span>
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

<span data-ttu-id="3a9d0-113">이 명령을 사용 하면 이전에 삭제 된 인증서 ' MyCertificate '을 활성 및 사용 가능한 상태로 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="3a9d0-114">변수</span><span class="sxs-lookup"><span data-stu-id="3a9d0-114">PARAMETERS</span></span>

### <span data-ttu-id="3a9d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9d0-115">-DefaultProfile</span></span>
<span data-ttu-id="3a9d0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a9d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a9d0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a9d0-117">-InputObject</span></span>
<span data-ttu-id="3a9d0-118">삭제 된 인증서 개체</span><span class="sxs-lookup"><span data-stu-id="3a9d0-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="3a9d0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3a9d0-119">-Name</span></span>
<span data-ttu-id="3a9d0-120">인증서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-120">Certificate name.</span></span>
<span data-ttu-id="3a9d0-121">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 인증서 이름 으로부터 인증서의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="3a9d0-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3a9d0-122">-VaultName</span></span>
<span data-ttu-id="3a9d0-123">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="3a9d0-123">Vault name.</span></span>
<span data-ttu-id="3a9d0-124">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3a9d0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="3a9d0-125">-Confirm</span></span>
<span data-ttu-id="3a9d0-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9d0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9d0-127">-WhatIf</span></span>
<span data-ttu-id="3a9d0-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9d0-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9d0-130">CommonParameters</span></span>
<span data-ttu-id="3a9d0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9d0-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a9d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9d0-133">입력</span><span class="sxs-lookup"><span data-stu-id="3a9d0-133">INPUTS</span></span>

### <span data-ttu-id="3a9d0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3a9d0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="3a9d0-135">출력</span><span class="sxs-lookup"><span data-stu-id="3a9d0-135">OUTPUTS</span></span>

### <span data-ttu-id="3a9d0-136">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3a9d0-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3a9d0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3a9d0-137">NOTES</span></span>

## <span data-ttu-id="3a9d0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a9d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="3a9d0-139">제거-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3a9d0-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="3a9d0-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3a9d0-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
