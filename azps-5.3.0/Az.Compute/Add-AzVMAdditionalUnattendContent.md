---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493925"
---
# <span data-ttu-id="82c6c-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="82c6c-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="82c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="82c6c-103">무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="82c6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="82c6c-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c6c-105">설명</span><span class="sxs-lookup"><span data-stu-id="82c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="82c6c-106">**Add-AzVMAdditionalUnattendContent** cmdlet은 무인 Windows 설치 응답 파일에 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="82c6c-107">이 cmdlet이 unattend.xml 추가하는 기본 64로 인코딩된 .xml 형식의 정보를 unattend.xml 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="82c6c-108">예제</span><span class="sxs-lookup"><span data-stu-id="82c6c-108">EXAMPLES</span></span>

### <span data-ttu-id="82c6c-109">예제 1: 콘텐츠 추가 unattend.xml</span><span class="sxs-lookup"><span data-stu-id="82c6c-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="82c6c-110">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹에서 AvailabilitySet03이라는 가용성 집합을 끈 다음 해당 개체를 $AvailabilitySet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="82c6c-111">두 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="82c6c-112">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="82c6c-113">가상 머신은 가상 머신에 저장된 가용성 집합에 $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="82c6c-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="82c6c-114">세 번째 명령은 Get-Credential cmdlet을 사용하여 자격 증명 개체를 만든 다음, $Credential 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="82c6c-115">이 명령은 사용자 이름 및 암호를 묻는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="82c6c-116">자세한 내용은 `Get-Help Get-Credential` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="82c6c-117">네 번째 명령은 **Set-AzVMOperatingSystem** cmdlet을 사용하여 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="82c6c-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="82c6c-118">다섯 번째 명령은 $AucContent 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="82c6c-119">콘텐츠에는 암호가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-119">The content includes a password.</span></span>
<span data-ttu-id="82c6c-120">마지막 명령은 $AucContent 저장된 콘텐츠를 unattend.xml 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="82c6c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82c6c-121">PARAMETERS</span></span>

### <span data-ttu-id="82c6c-122">-Content</span><span class="sxs-lookup"><span data-stu-id="82c6c-122">-Content</span></span>
<span data-ttu-id="82c6c-123">기본 64로 인코딩된 XML 형식의 콘텐츠를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="82c6c-124">이 cmdlet은 콘텐츠가 unattend.xml 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="82c6c-125">XML 콘텐츠는 4KB 미만이 되어야 합니다. 이 cmdlet이 삽입하는 설정 또는 기능에 대한 루트 요소를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="82c6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c6c-126">-DefaultProfile</span></span>
<span data-ttu-id="82c6c-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82c6c-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="82c6c-128">-SettingName</span></span>
<span data-ttu-id="82c6c-129">콘텐츠가 적용되는 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="82c6c-130">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="82c6c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82c6c-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="82c6c-131">FirstLogonCommands</span></span>
- <span data-ttu-id="82c6c-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="82c6c-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c6c-133">-VM</span><span class="sxs-lookup"><span data-stu-id="82c6c-133">-VM</span></span>
<span data-ttu-id="82c6c-134">이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="82c6c-135">가상 머신 개체를 얻습니다. [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="82c6c-136">[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="82c6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c6c-137">CommonParameters</span></span>
<span data-ttu-id="82c6c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82c6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c6c-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82c6c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c6c-140">입력</span><span class="sxs-lookup"><span data-stu-id="82c6c-140">INPUTS</span></span>

### <span data-ttu-id="82c6c-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82c6c-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="82c6c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="82c6c-142">System.String</span></span>

### <span data-ttu-id="82c6c-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="82c6c-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="82c6c-144">출력</span><span class="sxs-lookup"><span data-stu-id="82c6c-144">OUTPUTS</span></span>

### <span data-ttu-id="82c6c-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82c6c-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="82c6c-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82c6c-146">NOTES</span></span>

## <span data-ttu-id="82c6c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82c6c-147">RELATED LINKS</span></span>

[<span data-ttu-id="82c6c-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="82c6c-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="82c6c-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="82c6c-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="82c6c-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="82c6c-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
