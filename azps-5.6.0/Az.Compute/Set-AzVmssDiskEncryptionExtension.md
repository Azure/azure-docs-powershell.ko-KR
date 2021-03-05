---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 7f163a80efe4e10f0107298351c59a72bfaaceb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001680"
---
# <span data-ttu-id="abf8c-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="abf8c-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="abf8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="abf8c-103">VM 확장 집합에서 디스크 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="abf8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="abf8c-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abf8c-105">설명</span><span class="sxs-lookup"><span data-stu-id="abf8c-105">DESCRIPTION</span></span>
<span data-ttu-id="abf8c-106">**Set-AzVmssDiskEncryptionExtension** cmdlet을 사용하면 VM 확장 집합에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="abf8c-107">이 cmdlet은 VM 확장 집합에 디스크 암호화 확장을 설치하여 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="abf8c-108">Linux 가상 머신의 경우 *VolumeType* 매개 변수가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="abf8c-109">예제</span><span class="sxs-lookup"><span data-stu-id="abf8c-109">EXAMPLES</span></span>

### <span data-ttu-id="abf8c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="abf8c-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="abf8c-111">이 명령은 VM 확장 집합의 모든 Windows VM의 모든 디스크에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="abf8c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="abf8c-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="abf8c-113">이 명령을 사용하면 VM 확장 집합의 모든 Linux VM의 데이터 디스크에서 암호화할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="abf8c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="abf8c-114">PARAMETERS</span></span>

### <span data-ttu-id="abf8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf8c-115">-DefaultProfile</span></span>
<span data-ttu-id="abf8c-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abf8c-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="abf8c-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="abf8c-118">부 버전 자동 업그레이드 사용 안</span><span class="sxs-lookup"><span data-stu-id="abf8c-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="abf8c-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="abf8c-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="abf8c-120">생성된 암호화 키가 배치되는 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="abf8c-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="abf8c-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="abf8c-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="abf8c-122">생성된 암호화 키가 배치되는 KeyVault의 URL</span><span class="sxs-lookup"><span data-stu-id="abf8c-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="abf8c-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="abf8c-123">-ExtensionName</span></span>
<span data-ttu-id="abf8c-124">확장 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-124">The extension name.</span></span>
<span data-ttu-id="abf8c-125">이 매개 변수를 지정하지 않으면 Windows VM용 AzureDiskEncryption 및 Linux VM용 AzureDiskEncryptionForLinux가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="abf8c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="abf8c-126">-Force</span></span>
<span data-ttu-id="abf8c-127">가상 머신 확장 집합에서 암호화를 강제로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="abf8c-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="abf8c-128">-ForceUpdate</span></span>
<span data-ttu-id="abf8c-129">강제 업데이트에 대한 태그를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-129">Generate a tag for force update.</span></span>  <span data-ttu-id="abf8c-130">동일한 VM에서 반복 암호화 작업을 수행하기 위해 이 작업을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="abf8c-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="abf8c-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="abf8c-132">볼륨 암호화 키를 암호화하는 데 사용되는 KeyEncryption 알고리즘</span><span class="sxs-lookup"><span data-stu-id="abf8c-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="abf8c-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="abf8c-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="abf8c-134">디스크 암호화 키를 암호화하는 데 사용되는 KeyEncryptionKey의 버전이 지정된 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="abf8c-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="abf8c-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="abf8c-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="abf8c-136">디스크 암호화 키를 암호화하는 데 사용되는 KeyEncryptionKey를 포함하는 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="abf8c-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="abf8c-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="abf8c-137">-Passphrase</span></span>
<span data-ttu-id="abf8c-138">매개 변수에 지정된 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="abf8c-139">이 매개 변수는 Linux VM에만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="abf8c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf8c-140">-ResourceGroupName</span></span>
<span data-ttu-id="abf8c-141">VM 확장 집합이 속한 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="abf8c-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="abf8c-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="abf8c-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="abf8c-143">형식 처리기 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-143">The type handler version.</span></span>

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

### <span data-ttu-id="abf8c-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="abf8c-144">-VMScaleSetName</span></span>
<span data-ttu-id="abf8c-145">가상 머신 확장 집합의 이름</span><span class="sxs-lookup"><span data-stu-id="abf8c-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="abf8c-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="abf8c-146">-VolumeType</span></span>
<span data-ttu-id="abf8c-147">암호화 작업을 수행할 가상 머신 볼륨 유형(OS, 데이터 또는 모두)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="abf8c-148">Linux: **VolumeType** 매개 변수가 있어야 합니다. 데이터로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="abf8c-149">Windows: **VolumeType** 매개 변수가 있는 경우 전체 또는 OS로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="abf8c-150">**VolumeType** 매개 변수가 생략된 경우 기본값은 "모두"입니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="abf8c-151">-확인</span><span class="sxs-lookup"><span data-stu-id="abf8c-151">-Confirm</span></span>
<span data-ttu-id="abf8c-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf8c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf8c-153">-WhatIf</span></span>
<span data-ttu-id="abf8c-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf8c-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf8c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf8c-156">CommonParameters</span></span>
<span data-ttu-id="abf8c-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="abf8c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf8c-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abf8c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf8c-159">입력</span><span class="sxs-lookup"><span data-stu-id="abf8c-159">INPUTS</span></span>

### <span data-ttu-id="abf8c-160">System.String</span><span class="sxs-lookup"><span data-stu-id="abf8c-160">System.String</span></span>

### <span data-ttu-id="abf8c-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="abf8c-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="abf8c-162">출력</span><span class="sxs-lookup"><span data-stu-id="abf8c-162">OUTPUTS</span></span>

### <span data-ttu-id="abf8c-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="abf8c-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="abf8c-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="abf8c-164">NOTES</span></span>

## <span data-ttu-id="abf8c-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abf8c-165">RELATED LINKS</span></span>
