---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990444"
---
# <span data-ttu-id="a6653-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a6653-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="a6653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6653-102">SYNOPSIS</span></span>
<span data-ttu-id="a6653-103">가상 머신에 대한 운영 체제 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="a6653-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6653-104">SYNTAX</span></span>

### <span data-ttu-id="a6653-105">Windows(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6653-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6653-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="a6653-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6653-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="a6653-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6653-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="a6653-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6653-109">Linux</span><span class="sxs-lookup"><span data-stu-id="a6653-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6653-110">설명</span><span class="sxs-lookup"><span data-stu-id="a6653-110">DESCRIPTION</span></span>
<span data-ttu-id="a6653-111">**Set-AzVMOperatingSystem** cmdlet은 가상 머신에 대한 운영 체제 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="a6653-112">로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="a6653-113">예제</span><span class="sxs-lookup"><span data-stu-id="a6653-113">EXAMPLES</span></span>

### <span data-ttu-id="a6653-114">예제 1: 새 가상 머신에 대한 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="a6653-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="a6653-115">첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="a6653-116">자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="a6653-117">두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="a6653-118">자세한 내용은 `Get-Help New-Object` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="a6653-119">세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a6653-120">네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a6653-121">명령은 가상 머신에 이름과 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a6653-122">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a6653-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a6653-123">다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="a6653-124">**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="a6653-125">그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="a6653-126">최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a6653-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a6653-127">명령은 명령에 저장된 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="a6653-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="a6653-128">명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="a6653-129">예제 2: 핫 패치를 사용하도록 설정된 새 가상 머신에 대한 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="a6653-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="a6653-130">첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="a6653-131">자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="a6653-132">두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="a6653-133">자세한 내용은 `Get-Help New-Object` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="a6653-134">세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a6653-135">네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a6653-136">명령은 가상 머신에 이름과 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a6653-137">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a6653-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a6653-138">다음 네 개의 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="a6653-139">**Set-AzVMOperatingSystem** 명령에서 직접 이러한 문자열을 지정할 수 있기 때문에 이 방법은 가독성에만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="a6653-140">그러나 스크립트에서 이와 같은 방법을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="a6653-141">최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a6653-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a6653-142">명령은 명령에 저장된 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="a6653-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="a6653-143">명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="a6653-144">이 명령은 가상 머신에서 Hotpatching을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="a6653-145">예제 3: 새 Linux 가상 머신에 대한 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="a6653-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="a6653-146">첫 번째 명령은 암호를 보안 문자열로 변환한 다음, 암호 $SecurePassword 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="a6653-147">자세한 내용은 `Get-Help ConvertTo-SecureString` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="a6653-148">두 번째 명령은 사용자 FullerP 및 암호에 저장된 암호에 대한 자격 증명을 $SecurePassword 자격 증명을 $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="a6653-149">자세한 내용은 `Get-Help New-Object` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="a6653-150">세 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 얻은 다음 해당 개체를 $AvailabilitySet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a6653-151">네 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a6653-152">명령은 가상 머신에 이름과 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a6653-153">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a6653-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a6653-154">다음 두 명령은 다음 명령에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="a6653-155">최종 명령은 가상 머신에 저장된 가상 머신에 대한 운영 체제 속성을 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a6653-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a6653-156">명령은 명령에 저장된 자격 증명을 $Credential.</span><span class="sxs-lookup"><span data-stu-id="a6653-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="a6653-157">명령은 일부 매개 변수에 대해 이전 명령에 할당된 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="a6653-158">명령은 가상 머신의 패치 모드 값을 "AutomaticByPlatform"으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="a6653-159">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6653-159">PARAMETERS</span></span>

### <span data-ttu-id="a6653-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="a6653-160">-ComputerName</span></span>
<span data-ttu-id="a6653-161">컴퓨터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-161">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="a6653-162">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="a6653-162">-Credential</span></span>
<span data-ttu-id="a6653-163">가상 머신에 대한 사용자 이름 및 암호를 **PSCredential 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a6653-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="a6653-164">자격 증명을 얻은 경우 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a6653-165">자세한 내용은 `Get-Help Get-Credential` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-165">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="a6653-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="a6653-166">-CustomData</span></span>
<span data-ttu-id="a6653-167">가상 머신에 전달할 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="a6653-168">자세한 내용은 [Azure VM의 사용자 지정 데이터를 참조하세요.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)</span><span class="sxs-lookup"><span data-stu-id="a6653-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="a6653-169">**참고: 사용자 지정 데이터에 중요한 정보를 저장하는 것은 권장되지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="a6653-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="a6653-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6653-170">-DefaultProfile</span></span>
<span data-ttu-id="a6653-171">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6653-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="a6653-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="a6653-173">이 cmdlet이 암호 인증을 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-173">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="a6653-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="a6653-174">-DisableVMAgent</span></span>
<span data-ttu-id="a6653-175">프로비전 VM 에이전트를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-175">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="a6653-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="a6653-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="a6653-177">이 cmdlet에서 자동 업데이트를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-177">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="a6653-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="a6653-178">-EnableHotpatching</span></span>
<span data-ttu-id="a6653-179">고객이 다시 부팅하지 않고도 Azure VM을 패치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="a6653-180">enableHotpatching의 경우 'provisionVMAgent'를 true로 설정하고 'patchMode'를 'AutomaticByPlatform'으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6653-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="a6653-181">-Linux</span></span>
<span data-ttu-id="a6653-182">운영 체제 유형이 Linux인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-182">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="a6653-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="a6653-183">-PatchMode</span></span>
<span data-ttu-id="a6653-184">IaaS 가상 머신에 게스트 내 패치 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="a6653-185">가능한 값은:</span><span class="sxs-lookup"><span data-stu-id="a6653-185">Possible values are:</span></span><br>
<span data-ttu-id="a6653-186">**수동** - 가상 머신에 패치 적용을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="a6653-187">이 작업을 수행하려면 VM 내부에 수동으로 패치를 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="a6653-188">이 모드에서는 자동 업데이트를 사용할 수 없습니다. 속성 WindowsConfiguration.enableAutomaticUpdates는 false가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="a6653-189">**자동ByOS** - 가상 머신은 OS에 의해 자동으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="a6653-190">속성 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="a6653-191">**AutomaticByPlatform** - 가상 머신이 OS에 의해 자동으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="a6653-192">속성 프로비전VMAgent 및 WindowsConfiguration.enableAutomaticUpdates는 true가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="a6653-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="a6653-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="a6653-194">설정에서 가상 머신 에이전트를 가상 머신에 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="a6653-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a6653-195">-TimeZone</span></span>
<span data-ttu-id="a6653-196">가상 머신의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="a6653-197">예: \" 태평양 표준시 \" 입니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="a6653-198">가능한 값은 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) [TimeZoneInfo.GetSystemTimeZones에서](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)TimeZoneInfo.Id 표준 시간대에서 값으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="a6653-199">-VM</span><span class="sxs-lookup"><span data-stu-id="a6653-199">-VM</span></span>
<span data-ttu-id="a6653-200">운영 체제 속성을 설정할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="a6653-201">가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="a6653-202">New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="a6653-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="a6653-203">-Windows</span></span>
<span data-ttu-id="a6653-204">운영 체제 유형이 Windows인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-204">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="a6653-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a6653-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="a6653-206">WinRM 인증서의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="a6653-207">이 파일은 Key Vault에 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-207">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="a6653-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="a6653-208">-WinRMHttp</span></span>
<span data-ttu-id="a6653-209">이 운영 체제에서 HTTP WinRM을 사용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-209">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="a6653-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="a6653-210">-WinRMHttps</span></span>
<span data-ttu-id="a6653-211">이 운영 체제에서 HTTPS WinRM을 사용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="a6653-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6653-212">CommonParameters</span></span>
<span data-ttu-id="a6653-213">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6653-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6653-214">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6653-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6653-215">입력</span><span class="sxs-lookup"><span data-stu-id="a6653-215">INPUTS</span></span>

### <span data-ttu-id="a6653-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6653-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a6653-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a6653-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a6653-218">System.String</span><span class="sxs-lookup"><span data-stu-id="a6653-218">System.String</span></span>

### <span data-ttu-id="a6653-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="a6653-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="a6653-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="a6653-220">System.Uri</span></span>

## <span data-ttu-id="a6653-221">출력</span><span class="sxs-lookup"><span data-stu-id="a6653-221">OUTPUTS</span></span>

### <span data-ttu-id="a6653-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a6653-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a6653-223">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6653-223">NOTES</span></span>

## <span data-ttu-id="a6653-224">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6653-224">RELATED LINKS</span></span>

[<span data-ttu-id="a6653-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a6653-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a6653-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a6653-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


