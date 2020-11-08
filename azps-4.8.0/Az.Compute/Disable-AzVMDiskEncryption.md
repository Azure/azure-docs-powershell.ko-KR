---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212571"
---
# <span data-ttu-id="5b507-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="5b507-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="5b507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b507-102">SYNOPSIS</span></span>
<span data-ttu-id="5b507-103">IaaS 가상 머신에서 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="5b507-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b507-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b507-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b507-105">DESCRIPTION</span></span>
<span data-ttu-id="5b507-106">**AzVMDiskEncryption** Cmdlet은 IaaS (인프라 as services) 가상 컴퓨터로 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="5b507-107">이 cmdlet은 Windows 가상 컴퓨터와 Linux 가상 컴퓨터 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="5b507-108">이 cmdlet은 암호화를 사용 하지 않도록 가상 컴퓨터에 확장을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="5b507-109">*Name* 매개 변수를 지정 하지 않으면 기본 이름인 "AzureDiskEncryption 암호화 Windows vm"이 있는 확장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="5b507-110">주의:이 cmdlet은 가상 컴퓨터를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="5b507-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5b507-111">EXAMPLES</span></span>

### <span data-ttu-id="5b507-112">예제 1: Windows 가상 컴퓨터의 모든 볼륨에 대해 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="5b507-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="5b507-113">이 명령은 Group001 이라는 리소스 그룹에 속하는 가상 컴퓨터 VM002의 모두 유형의 볼륨에 대해 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="5b507-114">지 수 *etype* 매개 변수를 지정 하지 않았으므로 cmdlet은 값을 All로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="5b507-115">예제 2: Windows 가상 컴퓨터에서 데이터 볼륨에 대 한 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="5b507-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="5b507-116">이 명령은 Group002 이라는 리소스 그룹에 속하는 가상 컴퓨터 VM004의 형식 데이터 볼륨에 대 한 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="5b507-117">변수</span><span class="sxs-lookup"><span data-stu-id="5b507-117">PARAMETERS</span></span>

### <span data-ttu-id="5b507-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b507-118">-DefaultProfile</span></span>
<span data-ttu-id="5b507-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b507-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5b507-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5b507-121">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="5b507-122">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="5b507-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="5b507-123">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-123">The extension publisher name.</span></span> <span data-ttu-id="5b507-124">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="5b507-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="5b507-125">-ExtensionType</span></span>
<span data-ttu-id="5b507-126">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-126">The extension type.</span></span> <span data-ttu-id="5b507-127">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="5b507-128">-Force</span><span class="sxs-lookup"><span data-stu-id="5b507-128">-Force</span></span>
<span data-ttu-id="5b507-129">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b507-130">-이름</span><span class="sxs-lookup"><span data-stu-id="5b507-130">-Name</span></span>
<span data-ttu-id="5b507-131">확장명을 나타내는 ARM (Azure Resource Manager) 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="5b507-132">이 매개 변수를 지정 하지 않으면이 cmdlet은 "Windows Vm 용 AzureDiskEncryption"을 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="5b507-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b507-133">-ResourceGroupName</span></span>
<span data-ttu-id="5b507-134">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="5b507-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5b507-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="5b507-136">암호화 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="5b507-137">이 매개 변수에 대 한 값을 지정 하지 않으면 최신 버전의 확장을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="5b507-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b507-138">-VMName</span></span>
<span data-ttu-id="5b507-139">이 cmdlet이 암호화를 사용 하지 않도록 설정 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="5b507-140">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="5b507-140">-VolumeType</span></span>
<span data-ttu-id="5b507-141">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="5b507-142">Windows 가상 컴퓨터의 경우 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="5b507-143">모든</span><span class="sxs-lookup"><span data-stu-id="5b507-143">All</span></span>
- <span data-ttu-id="5b507-144">변경할</span><span class="sxs-lookup"><span data-stu-id="5b507-144">OS</span></span>
- <span data-ttu-id="5b507-145">데이터.</span><span class="sxs-lookup"><span data-stu-id="5b507-145">Data.</span></span>
<span data-ttu-id="5b507-146">이 매개 변수에 대 한 값을 지정 하지 않으면 기본적으로 모두 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="5b507-147">현재 Linux에 대해 암호화 사용 안 함이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="5b507-148">-확인</span><span class="sxs-lookup"><span data-stu-id="5b507-148">-Confirm</span></span>
<span data-ttu-id="5b507-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b507-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b507-150">-WhatIf</span></span>
<span data-ttu-id="5b507-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b507-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b507-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b507-153">CommonParameters</span></span>
<span data-ttu-id="5b507-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b507-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5b507-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b507-156">입력</span><span class="sxs-lookup"><span data-stu-id="5b507-156">INPUTS</span></span>

### <span data-ttu-id="5b507-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b507-157">System.String</span></span>

### <span data-ttu-id="5b507-158">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b507-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b507-159">출력</span><span class="sxs-lookup"><span data-stu-id="5b507-159">OUTPUTS</span></span>

### <span data-ttu-id="5b507-160">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="5b507-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5b507-161">상속자</span><span class="sxs-lookup"><span data-stu-id="5b507-161">NOTES</span></span>

## <span data-ttu-id="5b507-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b507-162">RELATED LINKS</span></span>

[<span data-ttu-id="5b507-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="5b507-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="5b507-164">제거-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5b507-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="5b507-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5b507-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


