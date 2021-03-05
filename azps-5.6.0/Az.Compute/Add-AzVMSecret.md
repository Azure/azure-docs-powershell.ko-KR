---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: c4eef22d2bf188d56c0d7af66fb42ad3bce7b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962464"
---
# <span data-ttu-id="41c14-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="41c14-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="41c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41c14-102">SYNOPSIS</span></span>
<span data-ttu-id="41c14-103">가상 머신에 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="41c14-104">구문</span><span class="sxs-lookup"><span data-stu-id="41c14-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41c14-105">설명</span><span class="sxs-lookup"><span data-stu-id="41c14-105">DESCRIPTION</span></span>
<span data-ttu-id="41c14-106">**Add-AzVMSecret cmdlet은** 가상 머신에 비밀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="41c14-107">이 값을 사용하면 가상 머신에 인증서를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="41c14-108">비밀은 Key Vault에 저장되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="41c14-109">Key Vault에 대한 자세한 내용은 [Azure Key Vault란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="41c14-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="41c14-110">cmdlet에 대한 자세한 내용은 [Azure Key Vault Cmdlet](/powershell/module/az.keyvault) 또는 [Set-AzKeyVaultSecret cmdlet을](/powershell/module/az.keyvault/set-azkeyvaultsecret) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="41c14-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="41c14-111">예제</span><span class="sxs-lookup"><span data-stu-id="41c14-111">EXAMPLES</span></span>

### <span data-ttu-id="41c14-112">예제 1: 가상 머신에 비밀 추가</span><span class="sxs-lookup"><span data-stu-id="41c14-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="41c14-113">첫 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="41c14-114">명령은 가상 머신에 이름과 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="41c14-115">두 번째 명령은 Get-Credential cmdlet을 사용하여 자격 증명 개체를 만든 다음 결과를 $Credential 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="41c14-116">명령은 사용자 이름 및 암호를 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="41c14-117">자세한 내용은 `Get-Help Get-Credential` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="41c14-118">세 번째 명령은 **Set-AzVMOperatingSystem** cmdlet을 사용하여 에 저장된 가상 머신을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="41c14-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="41c14-119">네 번째 명령은 나중에 사용할 $SourceVaultId 변수에 원본 자격 증명 모음 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="41c14-120">명령은 $SubscriptionId 변수가 적절한 값을 가졌다고 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="41c14-121">다섯 번째 명령은 나중에 사용하기 위해 $CertificateStore 01 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="41c14-122">여섯 번째 명령은 인증서 저장소에 대한 URL을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="41c14-123">일곱 번째 명령은 에 저장된 가상 머신에 비밀을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="41c14-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="41c14-124">SourceVaultId 매개 변수는 Key Vault를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="41c14-125">명령은 인증서 저장소의 이름과 인증서의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="41c14-126">**Add-AzVMSecret을** 반복해서 실행하여 다른 인증서에 대한 비밀을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="41c14-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="41c14-127">PARAMETERS</span></span>

### <span data-ttu-id="41c14-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="41c14-128">-CertificateStore</span></span>
<span data-ttu-id="41c14-129">Windows 운영 체제를 실행하는 가상 머신의 인증서 저장소 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="41c14-130">이 cmdlet은 이 매개 변수가 지정하는 저장소에 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="41c14-131">Windows 운영 체제를 실행하는 가상 머신에만 이 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c14-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="41c14-132">-CertificateUrl</span></span>
<span data-ttu-id="41c14-133">인증서가 포함된 Key Vault 비밀을 지정하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="41c14-134">인증서는 다음 JavaScript 개체 표기법(JSON) 개체의 Base64 인코딩입니다. UTF-8: {"data": \<Base64-encoded-file\> ", "dataType": \<file-format\> ", "password": \<pfx-file-password\> "} 현재 dataType은 .pfx 파일만 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c14-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c14-135">-DefaultProfile</span></span>
<span data-ttu-id="41c14-136">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41c14-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="41c14-137">-SourceVaultId</span></span>
<span data-ttu-id="41c14-138">가상 머신에 추가할 수 있는 인증서를 포함하는 Key Vault의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="41c14-139">또한 이 값은 여러 인증서를 추가하기 위한 키 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="41c14-140">즉, 동일한 Key Vault에서 여러 인증서를 추가할 때 *SourceVaultId에* 동일한 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41c14-141">-VM</span><span class="sxs-lookup"><span data-stu-id="41c14-141">-VM</span></span>
<span data-ttu-id="41c14-142">이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="41c14-143">가상 머신 개체를 얻은 경우 [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="41c14-144">[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41c14-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c14-145">CommonParameters</span></span>
<span data-ttu-id="41c14-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41c14-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c14-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41c14-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c14-148">입력</span><span class="sxs-lookup"><span data-stu-id="41c14-148">INPUTS</span></span>

### <span data-ttu-id="41c14-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="41c14-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="41c14-150">System.String</span><span class="sxs-lookup"><span data-stu-id="41c14-150">System.String</span></span>

## <span data-ttu-id="41c14-151">출력</span><span class="sxs-lookup"><span data-stu-id="41c14-151">OUTPUTS</span></span>

### <span data-ttu-id="41c14-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="41c14-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="41c14-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41c14-153">NOTES</span></span>

## <span data-ttu-id="41c14-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41c14-154">RELATED LINKS</span></span>

[<span data-ttu-id="41c14-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="41c14-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="41c14-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="41c14-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="41c14-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="41c14-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
