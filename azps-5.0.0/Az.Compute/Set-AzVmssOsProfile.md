---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304223"
---
# <span data-ttu-id="268ae-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="268ae-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="268ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268ae-102">SYNOPSIS</span></span>
<span data-ttu-id="268ae-103">VMSS 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="268ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="268ae-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="268ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="268ae-105">DESCRIPTION</span></span>
<span data-ttu-id="268ae-106">**AzVmssOsProfile** Cmdlet은 가상 컴퓨터 크기 집합 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="268ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="268ae-107">EXAMPLES</span></span>

### <span data-ttu-id="268ae-108">예제 1: VMSS에 대 한 운영 체제 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="268ae-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="268ae-109">이 명령은 ContosoVMSS 이라는 VMSS에 속한 가상 컴퓨터의 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="268ae-110">이 명령은 VMSS에서 테스트 하 고 관리자 사용자 이름 및 암호를 제공 하는 모든 가상 컴퓨터 인스턴스의 컴퓨터 이름 접두사를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="268ae-111">변수</span><span class="sxs-lookup"><span data-stu-id="268ae-111">PARAMETERS</span></span>

### <span data-ttu-id="268ae-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="268ae-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="268ae-113">무인 콘텐츠 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="268ae-114">Add-AzVMAdditionalUnattendContent를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="268ae-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="268ae-115">-AdminPassword</span></span>
<span data-ttu-id="268ae-116">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="268ae-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="268ae-117">-AdminUsername</span></span>
<span data-ttu-id="268ae-118">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="268ae-119">**Windows 전용 제한:** 으로 끝날 수 없습니다 \" .\"</span><span class="sxs-lookup"><span data-stu-id="268ae-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="268ae-120">**허용 되지 않는 값:** \" 관리자 \" , \" 관리자 \" , \" 사용자 \" , \" user1 \" , \" 테스트 \" ,로, \" \" \" test1 \" , \" user3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser \" , \" adm \" , \" admin2 \" , \" aspnet \" , \" backup \" , \" console \" , \" david \" , \" 게스트 \" , \" john \" , \" owner \" , \" root \" , \" server \" , \" sql \" , \" support \" , \" support_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" user4 \" , \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="268ae-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="268ae-121">**최소 길이 (Linux):** 1 문자</span><span class="sxs-lookup"><span data-stu-id="268ae-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="268ae-122">**최대 길이 (Linux):** 64 문자</span><span class="sxs-lookup"><span data-stu-id="268ae-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="268ae-123">**최대 길이 (Windows):** 20 자</span><span class="sxs-lookup"><span data-stu-id="268ae-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="268ae-124">Linux VM에 대 한 루트 액세스의 경우 [Azure의 linux 가상 머신에 대 한 루트 권한 사용](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="268ae-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="268ae-125">이 필드에 사용할 수 없는 Linux의 기본 제공 시스템 사용자 목록은 [Azure에서 Linux의 사용자 이름 선택을](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="268ae-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="268ae-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="268ae-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="268ae-127">VMSS의 모든 가상 컴퓨터 인스턴스에 대 한 컴퓨터 이름 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="268ae-128">컴퓨터 이름은 1 ~ 15 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="268ae-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="268ae-129">-CustomData</span></span>
<span data-ttu-id="268ae-130">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="268ae-131">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="268ae-132">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="268ae-133">VM에 대 한 클라우드 초기화를 사용 [하려면 클라우드 초기화를 사용 하 여 LINUX VM을 만드는 동안 사용자 지정](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="268ae-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="268ae-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268ae-134">-DefaultProfile</span></span>
<span data-ttu-id="268ae-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268ae-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="268ae-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="268ae-137">이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="268ae-138">-수신기</span><span class="sxs-lookup"><span data-stu-id="268ae-138">-Listener</span></span>
<span data-ttu-id="268ae-139">WinRM (Windows Remote Management) 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="268ae-140">이렇게 하면 원격 Windows PowerShell이 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="268ae-141">Add-AzVmssWinRMListener cmdlet을 사용 하 여 수신기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="268ae-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="268ae-142">-PublicKey</span></span>
<span data-ttu-id="268ae-143">보안 셸 (SSH) 공개 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="268ae-144">Add-AzVMSshPublicKey cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="268ae-145">-비밀</span><span class="sxs-lookup"><span data-stu-id="268ae-145">-Secret</span></span>
<span data-ttu-id="268ae-146">가상 컴퓨터에 배치할 인증서 참조를 포함 하는 비밀 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="268ae-147">Add-AzVmssSecret cmdlet을 사용 하 여 비밀 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="268ae-148">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="268ae-148">-TimeZone</span></span>
<span data-ttu-id="268ae-149">가상 컴퓨터의 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="268ae-150">예: \" 태평양 표준시 시간 \" .</span><span class="sxs-lookup"><span data-stu-id="268ae-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="268ae-151">가능한 값은 [TimeZoneInfo Systemtimezones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)에서 반환 된 표준 시간대의 [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 값이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="268ae-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="268ae-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="268ae-153">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="268ae-154">New-AzVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="268ae-155">-Windowsconfigurationenable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="268ae-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="268ae-156">VMSS의 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="268ae-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="268ae-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="268ae-158">VMSS의 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="268ae-159">-확인</span><span class="sxs-lookup"><span data-stu-id="268ae-159">-Confirm</span></span>
<span data-ttu-id="268ae-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="268ae-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="268ae-161">-WhatIf</span></span>
<span data-ttu-id="268ae-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="268ae-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="268ae-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268ae-164">CommonParameters</span></span>
<span data-ttu-id="268ae-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="268ae-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268ae-166">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="268ae-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268ae-167">입력</span><span class="sxs-lookup"><span data-stu-id="268ae-167">INPUTS</span></span>

### <span data-ttu-id="268ae-168">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="268ae-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="268ae-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="268ae-169">System.String</span></span>

### <span data-ttu-id="268ae-170">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="268ae-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="268ae-171">Microsoft AdditionalUnattendContent []을 (를)</span><span class="sxs-lookup"><span data-stu-id="268ae-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="268ae-172">Microsoft. 관리. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="268ae-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="268ae-173">Microsoft SshPublicKey []을 (를)</span><span class="sxs-lookup"><span data-stu-id="268ae-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="268ae-174">Microsoft VaultSecretGroup []을 (를)</span><span class="sxs-lookup"><span data-stu-id="268ae-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="268ae-175">출력</span><span class="sxs-lookup"><span data-stu-id="268ae-175">OUTPUTS</span></span>

### <span data-ttu-id="268ae-176">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="268ae-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="268ae-177">상속자</span><span class="sxs-lookup"><span data-stu-id="268ae-177">NOTES</span></span>

## <span data-ttu-id="268ae-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="268ae-178">RELATED LINKS</span></span>

[<span data-ttu-id="268ae-179">추가-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="268ae-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="268ae-180">추가-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="268ae-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="268ae-181">추가-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="268ae-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="268ae-182">추가-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="268ae-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="268ae-183">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="268ae-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


