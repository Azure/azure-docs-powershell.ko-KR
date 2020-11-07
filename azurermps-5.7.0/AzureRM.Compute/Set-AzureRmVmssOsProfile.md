---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711185"
---
# <span data-ttu-id="f2929-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f2929-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="f2929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2929-102">SYNOPSIS</span></span>
<span data-ttu-id="f2929-103">VMSS 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2929-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2929-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2929-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2929-105">DESCRIPTION</span></span>
<span data-ttu-id="f2929-106">**AzureRmVmssOsProfile** Cmdlet은 가상 컴퓨터 크기 집합 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="f2929-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2929-107">EXAMPLES</span></span>

### <span data-ttu-id="f2929-108">예제 1: VMSS에 대 한 운영 체제 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="f2929-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="f2929-109">이 명령은 ContosoVMSS 이라는 VMSS에 속한 가상 컴퓨터의 운영 체제 프로필 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="f2929-110">이 명령은 VMSS에서 테스트 하 고 관리자 사용자 이름 및 암호를 제공 하는 모든 가상 컴퓨터 인스턴스의 컴퓨터 이름 접두사를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="f2929-111">변수</span><span class="sxs-lookup"><span data-stu-id="f2929-111">PARAMETERS</span></span>

### <span data-ttu-id="f2929-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f2929-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="f2929-113">무인 콘텐츠 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="f2929-114">Add-AzureRmVMAdditionalUnattendContent를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="f2929-115">-AdminPassword</span></span>
<span data-ttu-id="f2929-116">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="f2929-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="f2929-117">-AdminUsername</span></span>
<span data-ttu-id="f2929-118">VMSS의 모든 가상 컴퓨터 인스턴스에 사용할 관리자 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="f2929-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f2929-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="f2929-120">VMSS의 모든 가상 컴퓨터 인스턴스에 대 한 컴퓨터 이름 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="f2929-121">컴퓨터 이름은 1 ~ 15 자 길이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="f2929-122">-CustomData</span></span>
<span data-ttu-id="f2929-123">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="f2929-124">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="f2929-125">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="f2929-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="f2929-127">이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-127">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-128">-수신기</span><span class="sxs-lookup"><span data-stu-id="f2929-128">-Listener</span></span>
<span data-ttu-id="f2929-129">WinRM (Windows Remote Management) 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="f2929-130">이렇게 하면 원격 Windows PowerShell이 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="f2929-131">Add-AzureRmVmssWinRMListener cmdlet을 사용 하 여 수신기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="f2929-132">-PublicKey</span></span>
<span data-ttu-id="f2929-133">보안 셸 (SSH) 공개 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="f2929-134">Add-AzureRmVMSshPublicKey cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-135">-비밀</span><span class="sxs-lookup"><span data-stu-id="f2929-135">-Secret</span></span>
<span data-ttu-id="f2929-136">가상 컴퓨터에 배치할 인증서 참조를 포함 하는 비밀 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="f2929-137">Add-AzureRmVmssSecret cmdlet을 사용 하 여 비밀 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-138">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="f2929-138">-TimeZone</span></span>
<span data-ttu-id="f2929-139">가상 컴퓨터에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-139">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f2929-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f2929-141">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="f2929-142">New-AzureRmVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-143">-Windowsconfigurationenable자동 업데이트</span><span class="sxs-lookup"><span data-stu-id="f2929-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="f2929-144">VMSS의 가상 컴퓨터를 자동 업데이트에 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="f2929-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="f2929-146">VMSS의 가상 컴퓨터에서 가상 컴퓨터 에이전트를 프로 비전 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-147">-확인</span><span class="sxs-lookup"><span data-stu-id="f2929-147">-Confirm</span></span>
<span data-ttu-id="f2929-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2929-149">-WhatIf</span></span>
<span data-ttu-id="f2929-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2929-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2929-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2929-152">CommonParameters</span></span>
<span data-ttu-id="f2929-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2929-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2929-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2929-155">입력</span><span class="sxs-lookup"><span data-stu-id="f2929-155">INPUTS</span></span>

### <span data-ttu-id="f2929-156">않아야</span><span class="sxs-lookup"><span data-stu-id="f2929-156">None</span></span>
<span data-ttu-id="f2929-157">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2929-158">출력</span><span class="sxs-lookup"><span data-stu-id="f2929-158">OUTPUTS</span></span>

### <span data-ttu-id="f2929-159">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2929-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f2929-160">상속자</span><span class="sxs-lookup"><span data-stu-id="f2929-160">NOTES</span></span>

## <span data-ttu-id="f2929-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2929-161">RELATED LINKS</span></span>

[<span data-ttu-id="f2929-162">추가-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f2929-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="f2929-163">추가-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="f2929-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="f2929-164">추가-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f2929-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="f2929-165">추가-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f2929-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="f2929-166">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f2929-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


