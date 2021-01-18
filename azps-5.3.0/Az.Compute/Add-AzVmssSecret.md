---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496115"
---
# <span data-ttu-id="36d6f-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="36d6f-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="36d6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="36d6f-103">VMSS에 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="36d6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="36d6f-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36d6f-105">설명</span><span class="sxs-lookup"><span data-stu-id="36d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="36d6f-106">**Add-AzVmssSecret** cmdlet은 VMSS(Virtual Machine Scale Set)에 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="36d6f-107">비밀은 Azure Key Vault에 저장되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="36d6f-108">Key Vault와 관련된 자세한 내용은 [Azure Key Vault란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="36d6f-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="36d6f-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="36d6f-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="36d6f-110">cmdlet에 대한 자세한 내용은 [Azure Key Vault Cmdlet 또는](/powershell/module/az.keyvault) [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36d6f-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="36d6f-111">예제</span><span class="sxs-lookup"><span data-stu-id="36d6f-111">EXAMPLES</span></span>

### <span data-ttu-id="36d6f-112">예제 1: VMSS에 비밀 추가</span><span class="sxs-lookup"><span data-stu-id="36d6f-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="36d6f-113">이 예제에서는 VMSS에 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="36d6f-114">첫 번째 명령은 Get-AzKeyVault cmdlet을 사용하여 ContosoVault라는 자격 증명 모음에서 자격 증명 모음 비밀을 구하고 결과를 $Vault.</span><span class="sxs-lookup"><span data-stu-id="36d6f-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="36d6f-115">두 번째 명령은 **New-AzVmssVaultCertificateConfig** cmdlet을 사용하여 인증서라는 인증서 저장소에서 지정된 인증서 URL을 사용하여 Key Vault 인증서 구성을 만들고 결과를 $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="36d6f-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="36d6f-116">세 번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 VMSS라는 이름의 변수에 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="36d6f-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="36d6f-117">네 번째 명령은 키 리소스 ID 및 자격 증명 모음 및 자격 증명 모음 변수에 저장된 자격 증명 모음 인증서를 사용하여 자격 증명 모음 비밀을 사용하여 VMSS에 $Vault $CertConfig 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="36d6f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36d6f-118">PARAMETERS</span></span>

### <span data-ttu-id="36d6f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d6f-119">-DefaultProfile</span></span>
<span data-ttu-id="36d6f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d6f-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="36d6f-121">-SourceVaultId</span></span>
<span data-ttu-id="36d6f-122">가상 머신에 추가할 수 있는 인증서를 포함하는 Key Vault의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="36d6f-123">또한 이 값은 여러 인증서를 추가하기 위한 키 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="36d6f-124">즉, 동일한 Key Vault에서 여러 인증서를 추가할 때 *SourceVaultId* 매개 변수에 동일한 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d6f-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="36d6f-125">-VaultCertificate</span></span>
<span data-ttu-id="36d6f-126">인증서 URL 및 인증서 이름을 포함하는 **자격** 증명 모음 인증서 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="36d6f-127">[New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet을 사용하여 이 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d6f-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36d6f-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="36d6f-129">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="36d6f-130">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 이 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d6f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d6f-131">-Confirm</span></span>
<span data-ttu-id="36d6f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d6f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d6f-133">-WhatIf</span></span>
<span data-ttu-id="36d6f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36d6f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d6f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d6f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d6f-136">CommonParameters</span></span>
<span data-ttu-id="36d6f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36d6f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d6f-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36d6f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d6f-139">입력</span><span class="sxs-lookup"><span data-stu-id="36d6f-139">INPUTS</span></span>

### <span data-ttu-id="36d6f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36d6f-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="36d6f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="36d6f-141">System.String</span></span>

### <span data-ttu-id="36d6f-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="36d6f-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="36d6f-143">출력</span><span class="sxs-lookup"><span data-stu-id="36d6f-143">OUTPUTS</span></span>

### <span data-ttu-id="36d6f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36d6f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36d6f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36d6f-145">NOTES</span></span>

## <span data-ttu-id="36d6f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36d6f-146">RELATED LINKS</span></span>

[<span data-ttu-id="36d6f-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="36d6f-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="36d6f-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="36d6f-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
