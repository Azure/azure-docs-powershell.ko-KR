---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
ms.openlocfilehash: 0eea5d3a4f379b61e5d66e04b66e7812abaf75f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882649"
---
# <span data-ttu-id="64332-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="64332-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="64332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64332-102">SYNOPSIS</span></span>
<span data-ttu-id="64332-103">가상 컴퓨터에 대 한 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64332-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64332-104">SYNTAX</span></span>

### <span data-ttu-id="64332-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="64332-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64332-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="64332-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64332-107">Linux</span><span class="sxs-lookup"><span data-stu-id="64332-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64332-108">설명은</span><span class="sxs-lookup"><span data-stu-id="64332-108">DESCRIPTION</span></span>
<span data-ttu-id="64332-109">**AzureRmVMOperatingSystem** cmdlet은 가상 컴퓨터의 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="64332-110">로그온 자격 증명, 컴퓨터 이름 및 운영 체제 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64332-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="64332-111">예제의</span><span class="sxs-lookup"><span data-stu-id="64332-111">EXAMPLES</span></span>

### <span data-ttu-id="64332-112">예제 1: 새 가상 컴퓨터의 운영 체제 속성 설정</span><span class="sxs-lookup"><span data-stu-id="64332-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="64332-113">첫 번째 명령은 암호를 안전한 문자열로 변환한 다음 $SecurePassword 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="64332-114">자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="64332-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="64332-115">두 번째 명령은 사용자의 자격 증명을 만들고 $SecurePassword에 저장 된 암호를 만든 다음 $Credential 변수에 자격 증명을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="64332-116">자세한 내용은을 입력 `Get-Help New-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="64332-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="64332-117">세 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="64332-118">네 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="64332-119">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="64332-120">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="64332-121">다음 네 개의 명령은 다음 명령에 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="64332-122">이러한 문자열은 **Set-AzureRmVMOperatingSystem** 명령에서 직접 지정할 수 있으므로이 접근 방식은 가독성을 위해 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="64332-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="64332-123">그러나이 방법을 스크립트에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64332-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="64332-124">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터의 운영 체제 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="64332-125">이 명령은 $Credential에 저장 된 자격 증명을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="64332-126">명령에서는 일부 매개 변수에 대해 이전 명령에서 할당 된 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="64332-127">변수</span><span class="sxs-lookup"><span data-stu-id="64332-127">PARAMETERS</span></span>

### <span data-ttu-id="64332-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="64332-128">-ComputerName</span></span>
<span data-ttu-id="64332-129">컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="64332-130">-Credential</span></span>
<span data-ttu-id="64332-131">가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="64332-132">자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="64332-133">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="64332-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="64332-134">-CustomData</span></span>
<span data-ttu-id="64332-135">사용자 지정 데이터의 base-64 인코딩된 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="64332-136">이는 가상 컴퓨터에 파일로 저장 된 이진 배열로 디코딩됩니다.</span><span class="sxs-lookup"><span data-stu-id="64332-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="64332-137">이진 배열의 최대 길이는 65535 바이트입니다.</span><span class="sxs-lookup"><span data-stu-id="64332-137">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="64332-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64332-138">-DefaultProfile</span></span>
<span data-ttu-id="64332-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64332-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64332-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="64332-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="64332-141">이 cmdlet이 암호 인증을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-141">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-142">-EnableAutoUpdate 업데이트</span><span class="sxs-lookup"><span data-stu-id="64332-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="64332-143">이 cmdlet이 자동 업데이트를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="64332-144">-Linux</span></span>
<span data-ttu-id="64332-145">운영 체제 유형이 Linux 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-145">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="64332-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="64332-147">설정에 따라 가상 컴퓨터에 가상 컴퓨터 에이전트가 설치 되어 있어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-148">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="64332-148">-TimeZone</span></span>
<span data-ttu-id="64332-149">가상 컴퓨터에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-150">-VM</span><span class="sxs-lookup"><span data-stu-id="64332-150">-VM</span></span>
<span data-ttu-id="64332-151">운영 체제 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="64332-152">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="64332-153">New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64332-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="64332-154">-Windows</span></span>
<span data-ttu-id="64332-155">운영 체제 유형이 Windows 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="64332-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="64332-157">WinRM 인증서의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="64332-158">이를 키 보관소에 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="64332-159">-WinRMHttp</span></span>
<span data-ttu-id="64332-160">이 운영 체제에서 HTTP WinRM을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="64332-161">-WinRMHttps</span></span>
<span data-ttu-id="64332-162">이 운영 체제에서 HTTPS WinRM을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64332-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64332-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64332-163">CommonParameters</span></span>
<span data-ttu-id="64332-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64332-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64332-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64332-166">입력</span><span class="sxs-lookup"><span data-stu-id="64332-166">INPUTS</span></span>

### <span data-ttu-id="64332-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64332-167">PSVirtualMachine</span></span>
<span data-ttu-id="64332-168">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="64332-169">출력</span><span class="sxs-lookup"><span data-stu-id="64332-169">OUTPUTS</span></span>

### <span data-ttu-id="64332-170">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="64332-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="64332-171">상속자</span><span class="sxs-lookup"><span data-stu-id="64332-171">NOTES</span></span>

## <span data-ttu-id="64332-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64332-172">RELATED LINKS</span></span>

[<span data-ttu-id="64332-173">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="64332-173">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="64332-174">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="64332-174">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


