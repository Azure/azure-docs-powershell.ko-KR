---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 281b74aa14431a0bcfe0d138a78db73e28bcfeb4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877134"
---
# <span data-ttu-id="d907a-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="d907a-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="d907a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d907a-102">SYNOPSIS</span></span>
<span data-ttu-id="d907a-103">가상 컴퓨터에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="d907a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d907a-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d907a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d907a-105">DESCRIPTION</span></span>
<span data-ttu-id="d907a-106">**추가-AzVMSecret** cmdlet은 가상 컴퓨터에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="d907a-107">이 값을 사용 하 여 가상 컴퓨터에 인증서를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="d907a-108">비밀은 키 보관소에 저장 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="d907a-109">키 자격 증명 모음에 대 한 자세한 내용은 [Azure 키 보관소 란?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d907a-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="d907a-110">Cmdlet에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리 또는 [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) Cmdlet의 [Azure 키 자격 증명 모음 cmdlet](https://msdn.microsoft.com/library/azure/dn868052.aspx) 을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d907a-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="d907a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d907a-111">EXAMPLES</span></span>

### <span data-ttu-id="d907a-112">예제 1: 가상 컴퓨터에 비밀 추가</span><span class="sxs-lookup"><span data-stu-id="d907a-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="d907a-113">첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d907a-114">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d907a-115">두 번째 명령은 Get-Credential cmdlet을 사용 하 여 credential 개체를 만든 다음 그 결과를 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="d907a-116">명령이 사용자 이름 및 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="d907a-117">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="d907a-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="d907a-118">세 번째 명령은 **AzVMOperatingSystem** cmdlet을 사용 하 여 $VirtualMachine에 저장 된 가상 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="d907a-119">네 번째 명령은 나중에 사용할 수 있도록 $SourceVaultId 변수에 원본 자격 증명 모음 ID를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="d907a-120">명령에서는 $SubscriptionId 변수에 적절 한 값이 있다고 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="d907a-121">다섯 번째 명령은 나중에 사용할 수 있도록 $CertificateStore 01 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="d907a-122">여섯 번째 명령은 인증서 저장소에 대 한 URL을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="d907a-123">일곱째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 비밀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d907a-124">SourceVaultId 매개 변수는 키 보관소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="d907a-125">명령은 인증서 저장소의 이름과 인증서의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="d907a-126">**추가-AzVMSecret** 를 반복적으로 실행 하 여 다른 인증서에 대 한 비밀을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="d907a-127">변수</span><span class="sxs-lookup"><span data-stu-id="d907a-127">PARAMETERS</span></span>

### <span data-ttu-id="d907a-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="d907a-128">-CertificateStore</span></span>
<span data-ttu-id="d907a-129">Windows 운영 체제를 실행 하는 가상 컴퓨터의 인증서 저장소 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="d907a-130">이 cmdlet은이 매개 변수에서 지정 하는 저장소에 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="d907a-131">Windows 운영 체제를 실행 하는 가상 컴퓨터에 대해서만이 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d907a-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="d907a-132">-CertificateUrl</span></span>
<span data-ttu-id="d907a-133">인증서를 포함 하는 키 보관소 비밀을 가리키는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="d907a-134">인증서는 u t f-8로 인코딩된 다음의 JSON (JavaScript Object Notation) 개체에 대 한 Base64 인코딩입니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="d907a-135">{"data": " \< Base 64 인코딩 파일 \> "," dataType ":" \< 파일 형식 \> "," 암호 ":" \< pfx-file-password \> "}</span><span class="sxs-lookup"><span data-stu-id="d907a-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="d907a-136">현재 데이터 형식은 .pfx 파일만 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d907a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d907a-137">-DefaultProfile</span></span>
<span data-ttu-id="d907a-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d907a-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d907a-139">-SourceVaultId</span></span>
<span data-ttu-id="d907a-140">가상 컴퓨터에 추가할 수 있는 인증서를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="d907a-141">이 값은 또한 여러 인증서를 추가 하는 키 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="d907a-142">즉, 동일한 키 보관소에서 여러 개의 인증서를 추가 하는 경우 *SourceVaultId* 에 동일한 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d907a-143">-VM</span><span class="sxs-lookup"><span data-stu-id="d907a-143">-VM</span></span>
<span data-ttu-id="d907a-144">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d907a-145">가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-145">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d907a-146">[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-146">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d907a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d907a-147">CommonParameters</span></span>
<span data-ttu-id="d907a-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d907a-149">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d907a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d907a-150">입력</span><span class="sxs-lookup"><span data-stu-id="d907a-150">INPUTS</span></span>

### <span data-ttu-id="d907a-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d907a-151">PSVirtualMachine</span></span>
<span data-ttu-id="d907a-152">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d907a-153">출력</span><span class="sxs-lookup"><span data-stu-id="d907a-153">OUTPUTS</span></span>

### <span data-ttu-id="d907a-154">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d907a-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d907a-155">상속자</span><span class="sxs-lookup"><span data-stu-id="d907a-155">NOTES</span></span>

## <span data-ttu-id="d907a-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d907a-156">RELATED LINKS</span></span>

[<span data-ttu-id="d907a-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d907a-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d907a-158">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d907a-158">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="d907a-159">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d907a-159">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
