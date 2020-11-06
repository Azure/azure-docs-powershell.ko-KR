---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531105"
---
# <span data-ttu-id="83b8b-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="83b8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="83b8b-103">ARM (Azure Resource Manager) 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-103">Gets the properties of an Azure Resource Manager (ARM) virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83b8b-104">SYNTAX</span></span>

### <span data-ttu-id="83b8b-105">ListAllVirtualMachinesParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="83b8b-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83b8b-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="83b8b-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83b8b-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="83b8b-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83b8b-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="83b8b-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83b8b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="83b8b-109">DESCRIPTION</span></span>
<span data-ttu-id="83b8b-110">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터의 모델 뷰 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="83b8b-111">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="83b8b-112">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="83b8b-113">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="83b8b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="83b8b-114">EXAMPLES</span></span>

### <span data-ttu-id="83b8b-115">예제 1: 모델 및 인스턴스 보기 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="83b8b-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="83b8b-116">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 모델 보기 및 인스턴스 보기 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="83b8b-117">예제 2: 인스턴스 뷰 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="83b8b-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="83b8b-118">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="83b8b-119">이 명령은 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="83b8b-120">따라서이 명령은 인스턴스 보기 속성만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="83b8b-121">예제 3: 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="83b8b-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="83b8b-122">이 명령은 ResourceGroup11 이라는 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="83b8b-123">예제 4: 구독에서 모든 가상 컴퓨터 가져오기</span><span class="sxs-lookup"><span data-stu-id="83b8b-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="83b8b-124">이 명령은 구독에 있는 모든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="83b8b-125">변수</span><span class="sxs-lookup"><span data-stu-id="83b8b-125">PARAMETERS</span></span>

### <span data-ttu-id="83b8b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b8b-126">-DefaultProfile</span></span>
<span data-ttu-id="83b8b-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83b8b-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="83b8b-128">-DisplayHint</span></span>
<span data-ttu-id="83b8b-129">가상 컴퓨터 개체를 표시 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="83b8b-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-130">Valid values are:</span></span>

<span data-ttu-id="83b8b-131">--Compact: 최상위 수준 속성만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="83b8b-132">--확장: 모든 수준의 모든 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="83b8b-133">-이름</span><span class="sxs-lookup"><span data-stu-id="83b8b-133">-Name</span></span>
<span data-ttu-id="83b8b-134">가져올 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="83b8b-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="83b8b-135">-NextLink</span></span>
<span data-ttu-id="83b8b-136">다음 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="83b8b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b8b-137">-ResourceGroupName</span></span>
<span data-ttu-id="83b8b-138">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="83b8b-139">-상태</span><span class="sxs-lookup"><span data-stu-id="83b8b-139">-Status</span></span>
<span data-ttu-id="83b8b-140">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="83b8b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b8b-141">CommonParameters</span></span>
<span data-ttu-id="83b8b-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b8b-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b8b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b8b-144">입력</span><span class="sxs-lookup"><span data-stu-id="83b8b-144">INPUTS</span></span>

### <span data-ttu-id="83b8b-145">않아야</span><span class="sxs-lookup"><span data-stu-id="83b8b-145">None</span></span>
<span data-ttu-id="83b8b-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83b8b-147">출력</span><span class="sxs-lookup"><span data-stu-id="83b8b-147">OUTPUTS</span></span>

### <span data-ttu-id="83b8b-148">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b8b-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="83b8b-149">Microsoft. a. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="83b8b-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="83b8b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="83b8b-150">NOTES</span></span>

## <span data-ttu-id="83b8b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83b8b-151">RELATED LINKS</span></span>

[<span data-ttu-id="83b8b-152">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="83b8b-153">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="83b8b-154">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="83b8b-155">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="83b8b-156">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="83b8b-157">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83b8b-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


