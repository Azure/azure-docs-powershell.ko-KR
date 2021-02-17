---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204712"
---
# <span data-ttu-id="186c9-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="186c9-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="186c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="186c9-102">SYNOPSIS</span></span>
<span data-ttu-id="186c9-103">가상 머신에 대한 운영 체제 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="186c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="186c9-104">SYNTAX</span></span>

### <span data-ttu-id="186c9-105">Windows(기본값)</span><span class="sxs-lookup"><span data-stu-id="186c9-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="186c9-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="186c9-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="186c9-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="186c9-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="186c9-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="186c9-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="186c9-109">Linux</span><span class="sxs-lookup"><span data-stu-id="186c9-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="186c9-110">설명</span><span class="sxs-lookup"><span data-stu-id="186c9-110">DESCRIPTION</span></span>
<span data-ttu-id="186c9-111">**Set-AzVMOperatingSystem** cmdlet은 가상 머신에 대한 운영 체제 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="186c9-112">로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="186c9-113">예제</span><span class="sxs-lookup"><span data-stu-id="186c9-113">EXAMPLES</span></span>

### <span data-ttu-id="186c9-114">예제 1: 새 가상 머신에 대한 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="186c9-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="186c9-115">첫 번째 명령은 암호를 보안 문자열로 변환한 다음 $SecurePassword 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="186c9-116">자세한 내용은 `Get-Help ConvertTo-SecureString` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="186c9-117">두 번째 명령은 FullerP 사용자에 대한 자격 증명과 사용자에 저장된 암호를 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="186c9-118">자세한 내용은 `Get-Help New-Object` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="186c9-119">세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="186c9-120">네 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="186c9-121">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="186c9-122">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="186c9-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="186c9-123">다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="186c9-124">**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="186c9-125">그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="186c9-126">마지막 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="186c9-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="186c9-127">이 명령은 명령에 저장된 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="186c9-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="186c9-128">이 명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="186c9-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="186c9-129">PARAMETERS</span></span>

### <span data-ttu-id="186c9-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="186c9-130">-ComputerName</span></span>
<span data-ttu-id="186c9-131">컴퓨터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="186c9-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="186c9-132">-Credential</span></span>
<span data-ttu-id="186c9-133">가상 머신의 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="186c9-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="186c9-134">자격 증명을 얻습니다. Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="186c9-135">자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="186c9-136">-CustomData</span></span>
<span data-ttu-id="186c9-137">사용자 지정 데이터의 base-64로 인코딩된 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="186c9-138">가상 머신에 파일로 저장된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="186c9-139">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="186c9-140">**참고: customData 속성에 비밀 또는 암호를 전달하지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="186c9-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="186c9-141">VM을 만든 후 이 속성을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="186c9-142">customData가 파일로 저장될 VM에 전달됩니다. 자세한 내용은 Azure VM의 사용자 지정 데이터를 [참조하세요.](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="186c9-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="186c9-143">Linux VM에 cloud-init를 사용하는 경우 [cloud-init를](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) 사용하여 생성 중에 Linux VM 사용자 지정을 참조</span><span class="sxs-lookup"><span data-stu-id="186c9-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

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

### <span data-ttu-id="186c9-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="186c9-144">-DefaultProfile</span></span>
<span data-ttu-id="186c9-145">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="186c9-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="186c9-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="186c9-147">이 cmdlet이 암호 인증을 사용하지 않도록 설정하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="186c9-148">-DisableVMAgent</span></span>
<span data-ttu-id="186c9-149">VM 에이전트 프로비전을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="186c9-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="186c9-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="186c9-151">이 cmdlet을 통해 자동 업데이트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="186c9-152">-Linux</span></span>
<span data-ttu-id="186c9-153">운영 체제 유형이 Linux인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="186c9-154">-PatchMode</span></span>
<span data-ttu-id="186c9-155">IaaS 가상 머신에 대한 게스트 내 패치 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="186c9-156">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="186c9-156">Possible values are:</span></span><br>
<span data-ttu-id="186c9-157">**수동** - 가상 머신에 대한 패치의 애플리케이션을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="186c9-158">VM 내에서 패치를 수동으로 적용하여 이 작업을 수행하세요.</span><span class="sxs-lookup"><span data-stu-id="186c9-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="186c9-159">이 모드에서는 자동 업데이트가 비활성화됩니다. WindowsConfiguration.enableAutomaticUpdates 속성은 false가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="186c9-160">**AutomaticByOS** - 가상 머신은 OS에 의해 자동으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="186c9-161">WindowsConfiguration.enableAutomaticUpdates 속성은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="186c9-162">**AutomaticByPlatform** - 가상 머신이 OS에 의해 자동으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="186c9-163">properties provisionVMAgent 및 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="186c9-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="186c9-165">가상 머신에 가상 머신 에이전트를 설치해야 하는 설정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="186c9-166">-TimeZone</span></span>
<span data-ttu-id="186c9-167">가상 머신의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="186c9-168">예: \" 태평양 표준시 \"</span><span class="sxs-lookup"><span data-stu-id="186c9-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="186c9-169">가능한 값은 [TimeZoneInfo.getSystemTimeZones에서](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones) [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) 표준 시간대의 값을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-170">-VM</span><span class="sxs-lookup"><span data-stu-id="186c9-170">-VM</span></span>
<span data-ttu-id="186c9-171">운영 체제 속성을 설정할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="186c9-172">가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="186c9-173">New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="186c9-174">-Windows</span></span>
<span data-ttu-id="186c9-175">운영 체제의 유형이 Windows인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="186c9-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="186c9-177">WinRM 인증서의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="186c9-178">Key Vault에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="186c9-179">-WinRMHttp</span></span>
<span data-ttu-id="186c9-180">이 운영 체제가 HTTP WinRM을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="186c9-181">-WinRMHttps</span></span>
<span data-ttu-id="186c9-182">이 운영 체제가 HTTPS WinRM을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="186c9-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="186c9-183">CommonParameters</span></span>
<span data-ttu-id="186c9-184">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="186c9-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="186c9-185">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="186c9-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="186c9-186">입력</span><span class="sxs-lookup"><span data-stu-id="186c9-186">INPUTS</span></span>

### <span data-ttu-id="186c9-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="186c9-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="186c9-188">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="186c9-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="186c9-189">System.String</span><span class="sxs-lookup"><span data-stu-id="186c9-189">System.String</span></span>

### <span data-ttu-id="186c9-190">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="186c9-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="186c9-191">System.Uri</span><span class="sxs-lookup"><span data-stu-id="186c9-191">System.Uri</span></span>

## <span data-ttu-id="186c9-192">출력</span><span class="sxs-lookup"><span data-stu-id="186c9-192">OUTPUTS</span></span>

### <span data-ttu-id="186c9-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="186c9-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="186c9-194">참고 사항</span><span class="sxs-lookup"><span data-stu-id="186c9-194">NOTES</span></span>

## <span data-ttu-id="186c9-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="186c9-195">RELATED LINKS</span></span>

[<span data-ttu-id="186c9-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="186c9-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="186c9-197">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="186c9-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


