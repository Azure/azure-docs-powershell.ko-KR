---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: fe4b965aa859388c2066dc759354a1651cb20123
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531833"
---
# <span data-ttu-id="44cc8-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="44cc8-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="44cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="44cc8-103">VM 크기 집합에 대해 디스크 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44cc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44cc8-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44cc8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="44cc8-106">**AzureRmVmssDiskEncryptionExtension** CMDLET은 VM 배율 집합에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="44cc8-107">이 cmdlet은 디스크 암호화 확장을 VM 크기 집합에 설치 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="44cc8-108">*Name* 매개 변수를 지정 하지 않으면 Windows 운영 체제를 실행 하는 가상 컴퓨터 또는 Linux 용 Azurediskencryption forlinux 가상 머신에 대 한 기본 이름 AzureDiskEncryption 확장자가 설치 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="44cc8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="44cc8-109">EXAMPLES</span></span>

### <span data-ttu-id="44cc8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="44cc8-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="44cc8-111">이 명령은 VM 크기 집합에 있는 모든 Vm의 모든 디스크에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="44cc8-112">변수</span><span class="sxs-lookup"><span data-stu-id="44cc8-112">PARAMETERS</span></span>

### <span data-ttu-id="44cc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cc8-113">-DefaultProfile</span></span>
<span data-ttu-id="44cc8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44cc8-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="44cc8-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="44cc8-116">부 버전의 자동 업그레이드 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="44cc8-116">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="44cc8-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="44cc8-118">생성 된 암호화 키가 놓일 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="44cc8-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="44cc8-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="44cc8-120">생성 된 암호화 키가 놓일 KeyVault의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="44cc8-121">-ExtensionName</span></span>
<span data-ttu-id="44cc8-122">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-122">The extension name.</span></span>
<span data-ttu-id="44cc8-123">이 매개 변수를 지정 하지 않으면 windows Vm 용 AzureDiskEncryption, Linux 용 Azurediskencryption linux 용으로 기본값 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="44cc8-124">-Force</span></span>
<span data-ttu-id="44cc8-125">가상 컴퓨터 크기 조정 집합에서 강제로 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="44cc8-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="44cc8-126">-ForceUpdate</span></span>
<span data-ttu-id="44cc8-127">강제 업데이트에 대 한 태그를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-127">Generate a tag for force update.</span></span>  <span data-ttu-id="44cc8-128">동일한 VM에서 반복 되는 암호화 작업을 수행 하도록 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-129">-Keya 알고리즘</span><span class="sxs-lookup"><span data-stu-id="44cc8-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="44cc8-130">볼륨 암호화 키를 암호화 하는 데 사용 되는 KeyEncryption 알고리즘</span><span class="sxs-lookup"><span data-stu-id="44cc8-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="44cc8-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="44cc8-132">디스크 암호화 키를 암호화 하는 데 사용 되는 KeyEncryptionKey의 버전이 지정 된 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="44cc8-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="44cc8-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="44cc8-134">디스크 암호화 키를 암호화 하는 데 사용 되는 KeyEncryptionKey를 포함 하는 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="44cc8-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-135">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="44cc8-135">-Passphrase</span></span>
<span data-ttu-id="44cc8-136">매개 변수에 지정 된 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="44cc8-137">이 매개 변수는 Linux VM에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-137">This parameter only works for Linux VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44cc8-138">-ResourceGroupName</span></span>
<span data-ttu-id="44cc8-139">VM 크기 설정이 속한 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="44cc8-139">The resource group name to which the VM Scale Set belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="44cc8-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="44cc8-141">형식 처리기 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-141">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="44cc8-142">-VMScaleSetName</span></span>
<span data-ttu-id="44cc8-143">가상 머신 크기 조정 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-143">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-144">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="44cc8-144">-VolumeType</span></span>
<span data-ttu-id="44cc8-145">암호화 작업을 수행할 볼륨 유형 (OS 또는 데이터)</span><span class="sxs-lookup"><span data-stu-id="44cc8-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44cc8-146">-확인</span><span class="sxs-lookup"><span data-stu-id="44cc8-146">-Confirm</span></span>
<span data-ttu-id="44cc8-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44cc8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44cc8-148">-WhatIf</span></span>
<span data-ttu-id="44cc8-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44cc8-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44cc8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cc8-151">CommonParameters</span></span>
<span data-ttu-id="44cc8-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cc8-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cc8-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cc8-154">입력</span><span class="sxs-lookup"><span data-stu-id="44cc8-154">INPUTS</span></span>

### <span data-ttu-id="44cc8-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44cc8-155">System.String</span></span>
<span data-ttu-id="44cc8-156">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="44cc8-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44cc8-157">출력</span><span class="sxs-lookup"><span data-stu-id="44cc8-157">OUTPUTS</span></span>

### <span data-ttu-id="44cc8-158">PSVirtualMachineScaleSetExtension를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cc8-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="44cc8-159">상속자</span><span class="sxs-lookup"><span data-stu-id="44cc8-159">NOTES</span></span>

## <span data-ttu-id="44cc8-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44cc8-160">RELATED LINKS</span></span>
