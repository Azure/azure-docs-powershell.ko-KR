---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 3d3fdb53bf6dd0338f89bd03f11786bc9942acaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044610"
---
# <span data-ttu-id="da7a6-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="da7a6-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="da7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="da7a6-103">VMSS 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="da7a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da7a6-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="da7a6-106">**AzVmssOsProfile** Cmdlet은 가상 컴퓨터 크기 집합 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="da7a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="da7a6-107">EXAMPLES</span></span>

### <span data-ttu-id="da7a6-108">예제 1: VMSS에 대 한 운영 체제 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="da7a6-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="da7a6-109">이 명령은 ContosoVMSS 이라는 VMSS에 속한 가상 컴퓨터의 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="da7a6-110">이 명령은 VMSS에서 테스트 하 고 관리자 사용자 이름 및 암호를 제공 하는 모든 가상 컴퓨터 인스턴스의 컴퓨터 이름 접두사를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="da7a6-111">변수</span><span class="sxs-lookup"><span data-stu-id="da7a6-111">PARAMETERS</span></span>

### <span data-ttu-id="da7a6-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="da7a6-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="da7a6-113">무인 콘텐츠 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="da7a6-114">Add-AzVMAdditionalUnattendContent를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="da7a6-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="da7a6-115">-AdminPassword</span></span>
<span data-ttu-id="da7a6-116">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="da7a6-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="da7a6-117">-AdminUsername</span></span>
<span data-ttu-id="da7a6-118">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="da7a6-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="da7a6-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="da7a6-120">VMSS의 모든 가상 컴퓨터 인스턴스에 대 한 컴퓨터 이름 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="da7a6-121">컴퓨터 이름은 1 ~ 15 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="da7a6-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="da7a6-122">-CustomData</span></span>
<span data-ttu-id="da7a6-123">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="da7a6-124">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="da7a6-125">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="da7a6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7a6-126">-DefaultProfile</span></span>
<span data-ttu-id="da7a6-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da7a6-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="da7a6-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="da7a6-129">이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="da7a6-130">-수신기</span><span class="sxs-lookup"><span data-stu-id="da7a6-130">-Listener</span></span>
<span data-ttu-id="da7a6-131">WinRM (Windows Remote Management) 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="da7a6-132">이렇게 하면 원격 Windows PowerShell이 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="da7a6-133">Add-AzVmssWinRMListener cmdlet을 사용 하 여 수신기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="da7a6-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="da7a6-134">-PublicKey</span></span>
<span data-ttu-id="da7a6-135">보안 셸 (SSH) 공개 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="da7a6-136">Add-AzVMSshPublicKey cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="da7a6-137">-비밀</span><span class="sxs-lookup"><span data-stu-id="da7a6-137">-Secret</span></span>
<span data-ttu-id="da7a6-138">가상 컴퓨터에 배치할 인증서 참조를 포함 하는 비밀 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="da7a6-139">Add-AzVmssSecret cmdlet을 사용 하 여 비밀 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="da7a6-140">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="da7a6-140">-TimeZone</span></span>
<span data-ttu-id="da7a6-141">가상 컴퓨터에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="da7a6-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="da7a6-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="da7a6-143">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="da7a6-144">New-AzVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="da7a6-145">-Windowsconfigurationenable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="da7a6-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="da7a6-146">VMSS의 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="da7a6-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="da7a6-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="da7a6-148">VMSS의 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="da7a6-149">-확인</span><span class="sxs-lookup"><span data-stu-id="da7a6-149">-Confirm</span></span>
<span data-ttu-id="da7a6-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7a6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7a6-151">-WhatIf</span></span>
<span data-ttu-id="da7a6-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da7a6-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7a6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7a6-154">CommonParameters</span></span>
<span data-ttu-id="da7a6-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7a6-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da7a6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7a6-157">입력</span><span class="sxs-lookup"><span data-stu-id="da7a6-157">INPUTS</span></span>

### <span data-ttu-id="da7a6-158">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="da7a6-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="da7a6-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da7a6-159">System.String</span></span>

### <span data-ttu-id="da7a6-160">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="da7a6-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="da7a6-161">Microsoft AdditionalUnattendContent []을 (를)</span><span class="sxs-lookup"><span data-stu-id="da7a6-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="da7a6-162">Microsoft. 관리. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="da7a6-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="da7a6-163">Microsoft SshPublicKey []을 (를)</span><span class="sxs-lookup"><span data-stu-id="da7a6-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="da7a6-164">Microsoft VaultSecretGroup []을 (를)</span><span class="sxs-lookup"><span data-stu-id="da7a6-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="da7a6-165">출력</span><span class="sxs-lookup"><span data-stu-id="da7a6-165">OUTPUTS</span></span>

### <span data-ttu-id="da7a6-166">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="da7a6-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="da7a6-167">상속자</span><span class="sxs-lookup"><span data-stu-id="da7a6-167">NOTES</span></span>

## <span data-ttu-id="da7a6-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da7a6-168">RELATED LINKS</span></span>

[<span data-ttu-id="da7a6-169">추가-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="da7a6-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="da7a6-170">추가-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="da7a6-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="da7a6-171">추가-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="da7a6-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="da7a6-172">추가-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="da7a6-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="da7a6-173">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="da7a6-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


