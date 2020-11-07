---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 423cb695e4dedb978c3902e9c2f2c891a977464c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701984"
---
# <span data-ttu-id="ad39c-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ad39c-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="ad39c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad39c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad39c-103">VMSS에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad39c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad39c-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad39c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad39c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad39c-106">**AzureRmVmssSecret** Cmdlet은 가상 컴퓨터 크기 조정 집합 (vmss)에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ad39c-107">비밀은 Azure Key Vault에 저장 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="ad39c-108">키 볼트에 대 한 자세한 내용은 [Azure 키 보관소 란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad39c-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="ad39c-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="ad39c-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="ad39c-110">Cmdlet에 대 한 자세한 내용은 [Azure 키 자격 증명 모음 cmdlet](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) Microsoft 개발자 네트워크 라이브러리 또는 [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad39c-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="ad39c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ad39c-111">EXAMPLES</span></span>

### <span data-ttu-id="ad39c-112">예제 1: VMSS에 비밀 추가</span><span class="sxs-lookup"><span data-stu-id="ad39c-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="ad39c-113">이 예제에서는 VMSS에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="ad39c-114">첫 번째 명령은 Get-AzureRmKeyVault cmdlet을 사용 하 여 ContosoVault 이라는 자격 증명 모음에서 자격 증명 모음 비밀을 가져오고 그 결과를 $Vault 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="ad39c-115">두 번째 명령은 **AzureRmVmssVaultCertificateConfig** cmdlet을 사용 하 여 인증서 저장소에서 지정 된 인증서 URL을 사용 하 여 키 보관소 인증서 구성을 만든 다음 해당 결과를 $CertConfig 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="ad39c-116">세 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="ad39c-117">네 번째 명령은 $Vault 및 $CertConfig 변수에 저장 된 키 리소스 ID 및 자격 증명 모음 인증서를 사용 하 여 VMSS에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="ad39c-118">변수</span><span class="sxs-lookup"><span data-stu-id="ad39c-118">PARAMETERS</span></span>

### <span data-ttu-id="ad39c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad39c-119">-DefaultProfile</span></span>
<span data-ttu-id="ad39c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad39c-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ad39c-121">-SourceVaultId</span></span>
<span data-ttu-id="ad39c-122">가상 컴퓨터에 추가할 수 있는 인증서를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="ad39c-123">이 값은 또한 여러 인증서를 추가 하는 키 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="ad39c-124">즉, 동일한 키 보관소에서 여러 개의 인증서를 추가 하는 경우 *SourceVaultId* 매개 변수에 대해 동일한 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="ad39c-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="ad39c-125">-VaultCertificate</span></span>
<span data-ttu-id="ad39c-126">인증서 URL 및 인증서 이름을 포함 하는 자격 증명 모음 **인증서** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="ad39c-127">[새 AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet을 사용 하 여이 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="ad39c-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ad39c-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ad39c-129">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="ad39c-130">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여이 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="ad39c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ad39c-131">-Confirm</span></span>
<span data-ttu-id="ad39c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad39c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad39c-133">-WhatIf</span></span>
<span data-ttu-id="ad39c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad39c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad39c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad39c-136">CommonParameters</span></span>
<span data-ttu-id="ad39c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad39c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad39c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad39c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad39c-139">입력</span><span class="sxs-lookup"><span data-stu-id="ad39c-139">INPUTS</span></span>

### <span data-ttu-id="ad39c-140">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ad39c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ad39c-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad39c-141">System.String</span></span>

### <span data-ttu-id="ad39c-142">Microsoft VaultCertificate []을 (를)</span><span class="sxs-lookup"><span data-stu-id="ad39c-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="ad39c-143">출력</span><span class="sxs-lookup"><span data-stu-id="ad39c-143">OUTPUTS</span></span>

### <span data-ttu-id="ad39c-144">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ad39c-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ad39c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="ad39c-145">NOTES</span></span>

## <span data-ttu-id="ad39c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad39c-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad39c-147">새로운 AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="ad39c-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="ad39c-148">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ad39c-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
