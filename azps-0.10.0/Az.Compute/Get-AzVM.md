---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877080"
---
# <span data-ttu-id="fa3e1-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-101">Get-AzVM</span></span>

## <span data-ttu-id="fa3e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3e1-103">가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="fa3e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa3e1-104">SYNTAX</span></span>

### <span data-ttu-id="fa3e1-105">ListAllVirtualMachinesParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa3e1-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa3e1-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="fa3e1-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa3e1-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="fa3e1-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa3e1-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="fa3e1-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa3e1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fa3e1-109">DESCRIPTION</span></span>
<span data-ttu-id="fa3e1-110">**AzVM** Cmdlet은 Azure 가상 컴퓨터의 모델 뷰 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="fa3e1-111">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="fa3e1-112">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="fa3e1-113">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="fa3e1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="fa3e1-114">EXAMPLES</span></span>

### <span data-ttu-id="fa3e1-115">예제 1: 모델 및 인스턴스 보기 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="fa3e1-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="fa3e1-116">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 모델 보기 및 인스턴스 보기 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="fa3e1-117">예제 2: 인스턴스 뷰 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="fa3e1-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="fa3e1-118">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="fa3e1-119">이 명령은 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="fa3e1-120">따라서이 명령은 인스턴스 보기 속성만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="fa3e1-121">예제 3: 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="fa3e1-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="fa3e1-122">이 명령은 ResourceGroup11 이라는 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="fa3e1-123">예제 4: 구독에서 모든 가상 컴퓨터 가져오기</span><span class="sxs-lookup"><span data-stu-id="fa3e1-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="fa3e1-124">이 명령은 구독에 있는 모든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="fa3e1-125">변수</span><span class="sxs-lookup"><span data-stu-id="fa3e1-125">PARAMETERS</span></span>

### <span data-ttu-id="fa3e1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3e1-126">-DefaultProfile</span></span>
<span data-ttu-id="fa3e1-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa3e1-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="fa3e1-128">-DisplayHint</span></span>
<span data-ttu-id="fa3e1-129">가상 컴퓨터 개체를 표시 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="fa3e1-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-130">Valid values are:</span></span>

<span data-ttu-id="fa3e1-131">--Compact: 최상위 수준 속성만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="fa3e1-132">--확장: 모든 수준의 모든 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e1-133">-이름</span><span class="sxs-lookup"><span data-stu-id="fa3e1-133">-Name</span></span>
<span data-ttu-id="fa3e1-134">가져올 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e1-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="fa3e1-135">-NextLink</span></span>
<span data-ttu-id="fa3e1-136">다음 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa3e1-137">-ResourceGroupName</span></span>
<span data-ttu-id="fa3e1-138">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e1-139">-상태</span><span class="sxs-lookup"><span data-stu-id="fa3e1-139">-Status</span></span>
<span data-ttu-id="fa3e1-140">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa3e1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3e1-141">CommonParameters</span></span>
<span data-ttu-id="fa3e1-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3e1-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa3e1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3e1-144">입력</span><span class="sxs-lookup"><span data-stu-id="fa3e1-144">INPUTS</span></span>

### <span data-ttu-id="fa3e1-145">않아야</span><span class="sxs-lookup"><span data-stu-id="fa3e1-145">None</span></span>
<span data-ttu-id="fa3e1-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa3e1-147">출력</span><span class="sxs-lookup"><span data-stu-id="fa3e1-147">OUTPUTS</span></span>

### <span data-ttu-id="fa3e1-148">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fa3e1-149">Microsoft. a. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="fa3e1-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="fa3e1-150">상속자</span><span class="sxs-lookup"><span data-stu-id="fa3e1-150">NOTES</span></span>

## <span data-ttu-id="fa3e1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa3e1-151">RELATED LINKS</span></span>

[<span data-ttu-id="fa3e1-152">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="fa3e1-153">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="fa3e1-154">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="fa3e1-155">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="fa3e1-156">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="fa3e1-157">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="fa3e1-157">Update-AzVM</span></span>](./Update-AzVM.md)


