---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304226"
---
# <span data-ttu-id="0887f-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0887f-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="0887f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0887f-102">SYNOPSIS</span></span>
<span data-ttu-id="0887f-103">VM 크기 집합에 대해 디스크 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="0887f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0887f-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0887f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0887f-105">DESCRIPTION</span></span>
<span data-ttu-id="0887f-106">**AzVmssDiskEncryptionExtension** CMDLET은 VM 배율 집합에서 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="0887f-107">이 cmdlet은 디스크 암호화 확장을 VM 크기 집합에 설치 하 여 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="0887f-108">Linux 가상 머신의 경우,는 데 필요한 *etype* 매개 변수가 있어야 하 고 "Data"로 설정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="0887f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0887f-109">EXAMPLES</span></span>

### <span data-ttu-id="0887f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0887f-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="0887f-111">이 명령을 사용 하면 VM 배율 집합에 있는 모든 Windows Vm의 모든 디스크에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="0887f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="0887f-112">Example 2</span></span>
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

<span data-ttu-id="0887f-113">이 명령을 사용 하면 VM 배율 집합에 있는 모든 Linux Vm의 데이터 디스크에 대 한 암호화가 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="0887f-114">변수</span><span class="sxs-lookup"><span data-stu-id="0887f-114">PARAMETERS</span></span>

### <span data-ttu-id="0887f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0887f-115">-DefaultProfile</span></span>
<span data-ttu-id="0887f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0887f-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0887f-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="0887f-118">부 버전의 자동 업그레이드 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="0887f-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="0887f-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0887f-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="0887f-120">생성 된 암호화 키가 놓일 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="0887f-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="0887f-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0887f-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="0887f-122">생성 된 암호화 키가 놓일 KeyVault의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="0887f-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0887f-123">-ExtensionName</span></span>
<span data-ttu-id="0887f-124">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-124">The extension name.</span></span>
<span data-ttu-id="0887f-125">이 매개 변수를 지정 하지 않으면 windows Vm 용 AzureDiskEncryption, Linux 용 Azurediskencryption linux 용으로 기본값 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="0887f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="0887f-126">-Force</span></span>
<span data-ttu-id="0887f-127">가상 컴퓨터 크기 조정 집합에서 강제로 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="0887f-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="0887f-128">-ForceUpdate</span></span>
<span data-ttu-id="0887f-129">강제 업데이트에 대 한 태그를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-129">Generate a tag for force update.</span></span>  <span data-ttu-id="0887f-130">동일한 VM에서 반복 되는 암호화 작업을 수행 하도록 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="0887f-131">-Keya 알고리즘</span><span class="sxs-lookup"><span data-stu-id="0887f-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="0887f-132">볼륨 암호화 키를 암호화 하는 데 사용 되는 KeyEncryption 알고리즘</span><span class="sxs-lookup"><span data-stu-id="0887f-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="0887f-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="0887f-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="0887f-134">디스크 암호화 키를 암호화 하는 데 사용 되는 KeyEncryptionKey의 버전이 지정 된 KeyVault URL</span><span class="sxs-lookup"><span data-stu-id="0887f-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="0887f-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0887f-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="0887f-136">디스크 암호화 키를 암호화 하는 데 사용 되는 KeyEncryptionKey를 포함 하는 KeyVault의 ResourceID</span><span class="sxs-lookup"><span data-stu-id="0887f-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="0887f-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="0887f-137">-Passphrase</span></span>
<span data-ttu-id="0887f-138">매개 변수에 지정 된 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="0887f-139">이 매개 변수는 Linux VM에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="0887f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0887f-140">-ResourceGroupName</span></span>
<span data-ttu-id="0887f-141">VM 크기 설정이 속한 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0887f-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="0887f-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="0887f-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="0887f-143">형식 처리기 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-143">The type handler version.</span></span>

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

### <span data-ttu-id="0887f-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0887f-144">-VMScaleSetName</span></span>
<span data-ttu-id="0887f-145">가상 머신 크기 조정 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="0887f-146">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="0887f-146">-VolumeType</span></span>
<span data-ttu-id="0887f-147">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형 (OS, 데이터 또는 모두)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="0887f-148">Linux:가 중 **etype** 매개 변수는 반드시 있어야 하며 Data로 설정 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="0887f-149">Windows:이 (가) 모든 또는 OS로 설정 되어 **있어야 합니다.**</span><span class="sxs-lookup"><span data-stu-id="0887f-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="0887f-150">지 수 **etype** 매개 변수를 생략 하면 기본값으로 "All"이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="0887f-151">-확인</span><span class="sxs-lookup"><span data-stu-id="0887f-151">-Confirm</span></span>
<span data-ttu-id="0887f-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0887f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0887f-153">-WhatIf</span></span>
<span data-ttu-id="0887f-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0887f-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0887f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0887f-156">CommonParameters</span></span>
<span data-ttu-id="0887f-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0887f-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0887f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0887f-159">입력</span><span class="sxs-lookup"><span data-stu-id="0887f-159">INPUTS</span></span>

### <span data-ttu-id="0887f-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0887f-160">System.String</span></span>

### <span data-ttu-id="0887f-161">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0887f-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0887f-162">출력</span><span class="sxs-lookup"><span data-stu-id="0887f-162">OUTPUTS</span></span>

### <span data-ttu-id="0887f-163">PSVirtualMachineScaleSetExtension를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="0887f-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="0887f-164">상속자</span><span class="sxs-lookup"><span data-stu-id="0887f-164">NOTES</span></span>

## <span data-ttu-id="0887f-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0887f-165">RELATED LINKS</span></span>
