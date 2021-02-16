---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195068"
---
# <span data-ttu-id="42d6d-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="42d6d-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="42d6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="42d6d-103">IaaS 가상 머신에서 암호화를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="42d6d-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="42d6d-104">구문</span><span class="sxs-lookup"><span data-stu-id="42d6d-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d6d-105">설명</span><span class="sxs-lookup"><span data-stu-id="42d6d-105">DESCRIPTION</span></span>
<span data-ttu-id="42d6d-106">**Disable-AzVMDiskEncryption** cmdlet은 IaaS(Infrastructure as a Service) 가상 머신에서 암호화를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="42d6d-107">이 cmdlet은 Linux 가상 머신이 아닌 Windows 가상 머신에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="42d6d-108">이 cmdlet은 암호화를 사용하지 않도록 가상 머신에 확장을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="42d6d-109">*Name* 매개 변수를 지정하지 않으면 기본 이름이 "Windows VM용 AzureDiskEncryption"인 확장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="42d6d-110">주의: 이 cmdlet은 가상 머신을 다시부팅합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="42d6d-111">예제</span><span class="sxs-lookup"><span data-stu-id="42d6d-111">EXAMPLES</span></span>

### <span data-ttu-id="42d6d-112">예제 1: Windows 가상 머신의 모든 볼륨에 대해 암호화 사용 안</span><span class="sxs-lookup"><span data-stu-id="42d6d-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="42d6d-113">이 명령은 Group001이라는 리소스 그룹에 속하는 VM002라는 가상 머신에 대한 모든 유형의 볼륨에 대한 암호화를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="42d6d-114">*VolumeType* 매개 변수가 지정되지 않은 경우 cmdlet은 값을 All로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="42d6d-115">예제 2: Windows 가상 머신에서 데이터 볼륨에 대한 암호화 사용 안</span><span class="sxs-lookup"><span data-stu-id="42d6d-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="42d6d-116">이 명령은 Group002 리소스 그룹에 속하는 VM004라는 가상 머신에 대한 형식 데이터 볼륨에 대한 암호화를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="42d6d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42d6d-117">PARAMETERS</span></span>

### <span data-ttu-id="42d6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d6d-118">-DefaultProfile</span></span>
<span data-ttu-id="42d6d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d6d-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="42d6d-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="42d6d-121">이 cmdlet이 부 버전의 확장 자동 업그레이드를 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="42d6d-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="42d6d-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="42d6d-123">확장 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-123">The extension publisher name.</span></span> <span data-ttu-id="42d6d-124">이 매개 변수를 지정하여 기본값인 "Microsoft.Azure.Security"를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="42d6d-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="42d6d-125">-ExtensionType</span></span>
<span data-ttu-id="42d6d-126">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-126">The extension type.</span></span> <span data-ttu-id="42d6d-127">이 매개 변수를 지정하여 Windows VM의 기본값인 "AzureDiskEncryption"을, Linux VM의 경우 "AzureDiskEncryptionForLinux"를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="42d6d-128">-Force</span><span class="sxs-lookup"><span data-stu-id="42d6d-128">-Force</span></span>
<span data-ttu-id="42d6d-129">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="42d6d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="42d6d-130">-Name</span></span>
<span data-ttu-id="42d6d-131">확장을 나타내는 Azure Resource Manager(ARM) 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="42d6d-132">이 매개 변수를 지정하지 않으면 이 cmdlet은 기본적으로 "Windows VM용 AzureDiskEncryption"으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d6d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d6d-133">-ResourceGroupName</span></span>
<span data-ttu-id="42d6d-134">가상 머신의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="42d6d-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="42d6d-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="42d6d-136">암호화 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="42d6d-137">이 매개 변수에 대한 값을 지정하지 않으면 최신 버전의 확장이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d6d-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="42d6d-138">-VMName</span></span>
<span data-ttu-id="42d6d-139">이 cmdlet에서 암호화를 사용하지 않도록 설정하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d6d-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="42d6d-140">-VolumeType</span></span>
<span data-ttu-id="42d6d-141">암호화 작업을 수행할 가상 머신 볼륨의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="42d6d-142">Windows 가상 머신의 경우 유효한 값은</span><span class="sxs-lookup"><span data-stu-id="42d6d-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="42d6d-143">모두</span><span class="sxs-lookup"><span data-stu-id="42d6d-143">All</span></span>
- <span data-ttu-id="42d6d-144">OS</span><span class="sxs-lookup"><span data-stu-id="42d6d-144">OS</span></span>
- <span data-ttu-id="42d6d-145">데이터.</span><span class="sxs-lookup"><span data-stu-id="42d6d-145">Data.</span></span>
<span data-ttu-id="42d6d-146">이 매개 변수에 대한 값을 지정하지 않으면 기본값은 모두입니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="42d6d-147">암호화 사용 안 은 현재 Linux에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d6d-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42d6d-148">-Confirm</span></span>
<span data-ttu-id="42d6d-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d6d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d6d-150">-WhatIf</span></span>
<span data-ttu-id="42d6d-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42d6d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d6d-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d6d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d6d-153">CommonParameters</span></span>
<span data-ttu-id="42d6d-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42d6d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d6d-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42d6d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d6d-156">입력</span><span class="sxs-lookup"><span data-stu-id="42d6d-156">INPUTS</span></span>

### <span data-ttu-id="42d6d-157">System.String</span><span class="sxs-lookup"><span data-stu-id="42d6d-157">System.String</span></span>

### <span data-ttu-id="42d6d-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42d6d-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42d6d-159">출력</span><span class="sxs-lookup"><span data-stu-id="42d6d-159">OUTPUTS</span></span>

### <span data-ttu-id="42d6d-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="42d6d-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="42d6d-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42d6d-161">NOTES</span></span>

## <span data-ttu-id="42d6d-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42d6d-162">RELATED LINKS</span></span>

[<span data-ttu-id="42d6d-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="42d6d-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="42d6d-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="42d6d-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="42d6d-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="42d6d-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


