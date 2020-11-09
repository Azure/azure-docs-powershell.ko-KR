---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307379"
---
# <span data-ttu-id="d3ca2-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d3ca2-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="d3ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ca2-103">무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d3ca2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3ca2-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ca2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ca2-106">**추가-AzVMAdditionalUnattendContent** cmdlet은 정보를 무인 Windows 설치 응답 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="d3ca2-107">이 cmdlet에서 unattend.xml 파일에 추가 하는 기본 64 인코딩 xml 형식의 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="d3ca2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d3ca2-108">EXAMPLES</span></span>

### <span data-ttu-id="d3ca2-109">예제 1: unattend.xml에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="d3ca2-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="d3ca2-110">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailabilitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="d3ca2-111">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d3ca2-112">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d3ca2-113">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="d3ca2-114">세 번째 명령은 Get-Credential cmdlet을 사용 하 여 credential 개체를 만든 다음 그 결과를 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="d3ca2-115">명령이 사용자 이름 및 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="d3ca2-116">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="d3ca2-117">네 번째 명령은 **AzVMOperatingSystem** cmdlet을 사용 하 여 $VirtualMachine에 저장 된 가상 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d3ca2-118">다섯 번째 명령은 $AucContent 변수에 콘텐츠를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="d3ca2-119">내용에 암호가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-119">The content includes a password.</span></span>
<span data-ttu-id="d3ca2-120">마지막 명령은 $AucContent에 저장 된 콘텐츠를 unattend.xml 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="d3ca2-121">변수</span><span class="sxs-lookup"><span data-stu-id="d3ca2-121">PARAMETERS</span></span>

### <span data-ttu-id="d3ca2-122">-콘텐츠</span><span class="sxs-lookup"><span data-stu-id="d3ca2-122">-Content</span></span>
<span data-ttu-id="d3ca2-123">Base 64 인코딩된 XML 형식의 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="d3ca2-124">이 cmdlet은 콘텐츠를 unattend.xml 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="d3ca2-125">XML 콘텐츠는 4kb 미만 이어야 하며이 cmdlet이 삽입 하는 설정 또는 기능에 대 한 루트 요소를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="d3ca2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ca2-126">-DefaultProfile</span></span>
<span data-ttu-id="d3ca2-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ca2-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d3ca2-128">-SettingName</span></span>
<span data-ttu-id="d3ca2-129">콘텐츠가 적용 되는 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d3ca2-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3ca2-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d3ca2-131">FirstLogonCommands</span></span>
- <span data-ttu-id="d3ca2-132">자동</span><span class="sxs-lookup"><span data-stu-id="d3ca2-132">AutoLogon</span></span>

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

### <span data-ttu-id="d3ca2-133">-VM</span><span class="sxs-lookup"><span data-stu-id="d3ca2-133">-VM</span></span>
<span data-ttu-id="d3ca2-134">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d3ca2-135">가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d3ca2-136">[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="d3ca2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ca2-137">CommonParameters</span></span>
<span data-ttu-id="d3ca2-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ca2-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ca2-140">입력</span><span class="sxs-lookup"><span data-stu-id="d3ca2-140">INPUTS</span></span>

### <span data-ttu-id="d3ca2-141">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d3ca2-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3ca2-142">System.String</span></span>

### <span data-ttu-id="d3ca2-143">시스템 Null 허용 ' 1 [[23.0.0.0]. SettingNames, Microsoft Azure. 관리. t e t =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d3ca2-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d3ca2-144">출력</span><span class="sxs-lookup"><span data-stu-id="d3ca2-144">OUTPUTS</span></span>

### <span data-ttu-id="d3ca2-145">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ca2-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d3ca2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d3ca2-146">NOTES</span></span>

## <span data-ttu-id="d3ca2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3ca2-147">RELATED LINKS</span></span>

[<span data-ttu-id="d3ca2-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d3ca2-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d3ca2-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d3ca2-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d3ca2-150">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d3ca2-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
