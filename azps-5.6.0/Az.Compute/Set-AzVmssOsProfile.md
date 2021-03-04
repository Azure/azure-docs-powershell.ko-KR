---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958891"
---
# <span data-ttu-id="ca4a9-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ca4a9-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="ca4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4a9-103">VMSS 운영 체제 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="ca4a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca4a9-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca4a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca4a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca4a9-106">**Set-AzVmssOsProfile** cmdlet은 Virtual Machine Scale Set 운영 체제 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="ca4a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca4a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca4a9-108">예제 1: VMSS에 대한 운영 체제 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="ca4a9-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="ca4a9-109">이 명령은 ContosoVMSS라는 VMSS에 속하는 가상 머신에 대한 운영 체제 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="ca4a9-110">명령은 VMSS의 모든 가상 머신 인스턴스에 대한 컴퓨터 이름 연결부를 테스트하도록 설정하고 관리자 사용자 이름 및 암호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="ca4a9-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca4a9-111">PARAMETERS</span></span>

### <span data-ttu-id="ca4a9-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ca4a9-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="ca4a9-113">무인 콘텐츠 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="ca4a9-114">개체를 만드는 데 Add-AzVMAdditionalUnattendContent 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="ca4a9-115">-AdminPassword</span></span>
<span data-ttu-id="ca4a9-116">VMSS의 모든 가상 머신 인스턴스에 사용할 관리자 암호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="ca4a9-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="ca4a9-117">-AdminUsername</span></span>
<span data-ttu-id="ca4a9-118">VMSS의 모든 가상 머신 인스턴스에 사용할 관리자 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="ca4a9-119">**Windows 전용 제한:** 에서 종료할 수 \" 없습니다.\"</span><span class="sxs-lookup"><span data-stu-id="ca4a9-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="ca4a9-120">**수 없습니다.** \" 관리자 , 관리자 , 사용자 \" \" , \" \" \" \" user1 , test , \" \" \" user2 , test1 , \" \" \" \" \" user3 \" , \" admin1 \" , \" 1 , 123 , a , actuser , adm , admin2 , aspnet \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" \" , Backup , Console , david , guest , john , owner , root , server , sql , support , support_388945a0 , sys , test2 , test3 , user4 , user5 .</span><span class="sxs-lookup"><span data-stu-id="ca4a9-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="ca4a9-121">**최소 길이(Linux):** 1자</span><span class="sxs-lookup"><span data-stu-id="ca4a9-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="ca4a9-122">**최대 길이(Linux):** 64자</span><span class="sxs-lookup"><span data-stu-id="ca4a9-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="ca4a9-123">**최대 길이(Windows):** 20자</span><span class="sxs-lookup"><span data-stu-id="ca4a9-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="ca4a9-124">Linux VM에 대한 루트 액세스는 Azure의 Linux 가상 머신에서 루트 권한 [사용을 참조하세요.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="ca4a9-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="ca4a9-125">이 필드에서 사용할 수 없는 Linux의 기본 제공 시스템 사용자 목록은 [Azure에서 Linux용 사용자](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)이름 선택을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="ca4a9-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ca4a9-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="ca4a9-127">VMSS의 모든 가상 머신 인스턴스에 대한 컴퓨터 이름 연결부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="ca4a9-128">컴퓨터 이름은 1~15자입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="ca4a9-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ca4a9-129">-CustomData</span></span>
<span data-ttu-id="ca4a9-130">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ca4a9-131">가상 머신의 파일로 저장되는 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ca4a9-132">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="ca4a9-133">VM에 클라우드-init를 사용하는 경우 만들기 중에 [Cloud-init를 사용하여 Linux VM을 사용자 지정하는 방법을 참조합니다.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="ca4a9-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4a9-134">-DefaultProfile</span></span>
<span data-ttu-id="ca4a9-135">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca4a9-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ca4a9-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="ca4a9-137">이 cmdlet이 암호 인증을 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="ca4a9-138">-Listener</span></span>
<span data-ttu-id="ca4a9-139">WinRM(Windows 원격 관리) 수신기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="ca4a9-140">이렇게 하면 원격 Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="ca4a9-141">수신기 Add-AzVmssWinRMListener cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="ca4a9-142">-PublicKey</span></span>
<span data-ttu-id="ca4a9-143">SSH(보안 셸) 공개 키 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="ca4a9-144">Add-AzVMSshPublicKey cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="ca4a9-145">-Secret</span></span>
<span data-ttu-id="ca4a9-146">가상 머신에 두는 인증서 참조를 포함하는 비밀 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="ca4a9-147">Add-AzVmssSecret cmdlet을 사용하여 비밀 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ca4a9-148">-TimeZone</span></span>
<span data-ttu-id="ca4a9-149">가상 머신의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="ca4a9-150">예: \" 태평양 표준시 \" 입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="ca4a9-151">가능한 값은 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) [TimeZoneInfo.GetSystemTimeZones에서](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)TimeZoneInfo.Id 표준 시간대에서 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ca4a9-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ca4a9-153">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="ca4a9-154">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ca4a9-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ca4a9-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="ca4a9-156">VMSS의 가상 머신이 자동 업데이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ca4a9-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="ca4a9-158">VMSS의 가상 머신에서 가상 머신 에이전트를 프로비전해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4a9-159">-확인</span><span class="sxs-lookup"><span data-stu-id="ca4a9-159">-Confirm</span></span>
<span data-ttu-id="ca4a9-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4a9-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4a9-161">-WhatIf</span></span>
<span data-ttu-id="ca4a9-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca4a9-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4a9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4a9-164">CommonParameters</span></span>
<span data-ttu-id="ca4a9-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4a9-166">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca4a9-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4a9-167">입력</span><span class="sxs-lookup"><span data-stu-id="ca4a9-167">INPUTS</span></span>

### <span data-ttu-id="ca4a9-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ca4a9-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ca4a9-169">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4a9-169">System.String</span></span>

### <span data-ttu-id="ca4a9-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca4a9-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ca4a9-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="ca4a9-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="ca4a9-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="ca4a9-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="ca4a9-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="ca4a9-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="ca4a9-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="ca4a9-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="ca4a9-175">출력</span><span class="sxs-lookup"><span data-stu-id="ca4a9-175">OUTPUTS</span></span>

### <span data-ttu-id="ca4a9-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ca4a9-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ca4a9-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca4a9-177">NOTES</span></span>

## <span data-ttu-id="ca4a9-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca4a9-178">RELATED LINKS</span></span>

[<span data-ttu-id="ca4a9-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ca4a9-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="ca4a9-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="ca4a9-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="ca4a9-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ca4a9-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="ca4a9-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ca4a9-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="ca4a9-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ca4a9-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


