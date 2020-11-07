---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: d2e05ca2d2d7b3e1839cd4b2cd1ae870faff77d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868878"
---
# <span data-ttu-id="69c5a-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="69c5a-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="69c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="69c5a-103">가상 컴퓨터에 대 한 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="69c5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69c5a-104">SYNTAX</span></span>

### <span data-ttu-id="69c5a-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="69c5a-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c5a-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="69c5a-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c5a-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="69c5a-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c5a-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="69c5a-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69c5a-109">Linux</span><span class="sxs-lookup"><span data-stu-id="69c5a-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69c5a-110">설명은</span><span class="sxs-lookup"><span data-stu-id="69c5a-110">DESCRIPTION</span></span>
<span data-ttu-id="69c5a-111">**AzVMOperatingSystem** cmdlet은 가상 컴퓨터의 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="69c5a-112">로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="69c5a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="69c5a-113">EXAMPLES</span></span>

### <span data-ttu-id="69c5a-114">예제 1: 새 가상 컴퓨터의 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="69c5a-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="69c5a-115">첫 번째 명령은 암호를 안전한 문자열로 변환한 다음 $SecurePassword 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="69c5a-116">자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="69c5a-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="69c5a-117">두 번째 명령은 사용자의 자격 증명을 만들고 $SecurePassword에 저장 된 암호를 만든 다음 $Credential 변수에 자격 증명을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="69c5a-118">자세한 내용은을 입력 `Get-Help New-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="69c5a-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="69c5a-119">세 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-119">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="69c5a-120">네 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="69c5a-121">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="69c5a-122">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="69c5a-123">다음 네 개의 명령은 다음 명령에 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="69c5a-124">이러한 문자열은 **Set-AzVMOperatingSystem** 명령에서 직접 지정할 수 있으므로이 접근 방식은 가독성을 위해 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="69c5a-125">그러나이 방법을 스크립트에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="69c5a-126">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터의 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="69c5a-127">이 명령은 $Credential에 저장 된 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="69c5a-128">명령에서는 일부 매개 변수에 대해 이전 명령에서 할당 된 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="69c5a-129">변수</span><span class="sxs-lookup"><span data-stu-id="69c5a-129">PARAMETERS</span></span>

### <span data-ttu-id="69c5a-130">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="69c5a-130">-ComputerName</span></span>
<span data-ttu-id="69c5a-131">컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="69c5a-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="69c5a-132">-Credential</span></span>
<span data-ttu-id="69c5a-133">가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="69c5a-134">자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="69c5a-135">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="69c5a-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="69c5a-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="69c5a-136">-CustomData</span></span>
<span data-ttu-id="69c5a-137">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="69c5a-138">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="69c5a-139">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="69c5a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c5a-140">-DefaultProfile</span></span>
<span data-ttu-id="69c5a-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c5a-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="69c5a-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="69c5a-143">이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="69c5a-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="69c5a-144">-DisableVMAgent</span></span>
<span data-ttu-id="69c5a-145">VM 에이전트 프로 비전을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="69c5a-146">-EnableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="69c5a-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="69c5a-147">이 cmdlet이 자동 업데이트를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="69c5a-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="69c5a-148">-Linux</span></span>
<span data-ttu-id="69c5a-149">운영 체제 유형이 Linux 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="69c5a-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="69c5a-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="69c5a-151">설정에 따라 가상 컴퓨터에 가상 컴퓨터 에이전트가 설치 되어 있어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="69c5a-152">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="69c5a-152">-TimeZone</span></span>
<span data-ttu-id="69c5a-153">가상 컴퓨터에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="69c5a-154">-VM</span><span class="sxs-lookup"><span data-stu-id="69c5a-154">-VM</span></span>
<span data-ttu-id="69c5a-155">운영 체제 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="69c5a-156">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-156">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="69c5a-157">New-AzVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-157">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="69c5a-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="69c5a-158">-Windows</span></span>
<span data-ttu-id="69c5a-159">운영 체제 유형이 Windows 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="69c5a-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="69c5a-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="69c5a-161">WinRM 인증서의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="69c5a-162">이를 키 보관소에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="69c5a-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="69c5a-163">-WinRMHttp</span></span>
<span data-ttu-id="69c5a-164">이 운영 체제에서 HTTP WinRM을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="69c5a-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="69c5a-165">-WinRMHttps</span></span>
<span data-ttu-id="69c5a-166">이 운영 체제에서 HTTPS WinRM을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="69c5a-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c5a-167">CommonParameters</span></span>
<span data-ttu-id="69c5a-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c5a-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c5a-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c5a-170">입력</span><span class="sxs-lookup"><span data-stu-id="69c5a-170">INPUTS</span></span>

### <span data-ttu-id="69c5a-171">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="69c5a-172">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="69c5a-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="69c5a-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69c5a-173">System.String</span></span>

### <span data-ttu-id="69c5a-174">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="69c5a-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="69c5a-175">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="69c5a-175">System.Uri</span></span>

## <span data-ttu-id="69c5a-176">출력</span><span class="sxs-lookup"><span data-stu-id="69c5a-176">OUTPUTS</span></span>

### <span data-ttu-id="69c5a-177">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="69c5a-178">상속자</span><span class="sxs-lookup"><span data-stu-id="69c5a-178">NOTES</span></span>

## <span data-ttu-id="69c5a-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69c5a-179">RELATED LINKS</span></span>

[<span data-ttu-id="69c5a-180">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="69c5a-180">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="69c5a-181">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="69c5a-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


