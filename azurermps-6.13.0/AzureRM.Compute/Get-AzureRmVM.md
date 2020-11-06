---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528595"
---
# <span data-ttu-id="b8deb-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="b8deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8deb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8deb-103">가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8deb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8deb-104">SYNTAX</span></span>

### <span data-ttu-id="b8deb-105">ListAllVirtualMachinesParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8deb-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8deb-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b8deb-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8deb-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="b8deb-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8deb-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="b8deb-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8deb-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="b8deb-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8deb-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b8deb-110">DESCRIPTION</span></span>
<span data-ttu-id="b8deb-111">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터의 모델 뷰 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="b8deb-112">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="b8deb-113">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="b8deb-114">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="b8deb-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b8deb-115">EXAMPLES</span></span>

### <span data-ttu-id="b8deb-116">예제 1: 모델 및 인스턴스 보기 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8deb-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="b8deb-117">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 모델 보기 및 인스턴스 보기 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b8deb-118">예제 2: 인스턴스 뷰 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8deb-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="b8deb-119">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="b8deb-120">이 명령은 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="b8deb-121">따라서이 명령은 인스턴스 보기 속성만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="b8deb-122">예제 3: 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8deb-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b8deb-123">이 명령은 ResourceGroup11 이라는 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b8deb-124">예제 4: 구독에서 모든 가상 컴퓨터 가져오기</span><span class="sxs-lookup"><span data-stu-id="b8deb-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="b8deb-125">이 명령은 구독에 있는 모든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="b8deb-126">예제 5: 해당 위치에 있는 모든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="b8deb-127">이 명령은 미국 지역에 있는 모든 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="b8deb-128">변수</span><span class="sxs-lookup"><span data-stu-id="b8deb-128">PARAMETERS</span></span>

### <span data-ttu-id="b8deb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8deb-129">-DefaultProfile</span></span>
<span data-ttu-id="b8deb-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="b8deb-131">-DisplayHint</span></span>
<span data-ttu-id="b8deb-132">가상 컴퓨터 개체를 표시 하는 방법을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="b8deb-133">유효한 값은 다음과 같습니다.--Compact: 최상위 수준 속성만 표시--확장: 모든 수준의 모든 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-134">-위치</span><span class="sxs-lookup"><span data-stu-id="b8deb-134">-Location</span></span>
<span data-ttu-id="b8deb-135">가상 컴퓨터를 나열할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-136">-이름</span><span class="sxs-lookup"><span data-stu-id="b8deb-136">-Name</span></span>
<span data-ttu-id="b8deb-137">가져올 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="b8deb-138">-NextLink</span></span>
<span data-ttu-id="b8deb-139">다음 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8deb-140">-ResourceGroupName</span></span>
<span data-ttu-id="b8deb-141">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-142">-상태</span><span class="sxs-lookup"><span data-stu-id="b8deb-142">-Status</span></span>
<span data-ttu-id="b8deb-143">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8deb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8deb-144">CommonParameters</span></span>
<span data-ttu-id="b8deb-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8deb-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8deb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8deb-147">입력</span><span class="sxs-lookup"><span data-stu-id="b8deb-147">INPUTS</span></span>

### <span data-ttu-id="b8deb-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8deb-148">System.String</span></span>

### <span data-ttu-id="b8deb-149">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="b8deb-149">System.Uri</span></span>

### <span data-ttu-id="b8deb-150">Microsoft. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="b8deb-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="b8deb-151">출력</span><span class="sxs-lookup"><span data-stu-id="b8deb-151">OUTPUTS</span></span>

### <span data-ttu-id="b8deb-152">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8deb-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b8deb-153">Microsoft. a. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="b8deb-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="b8deb-154">상속자</span><span class="sxs-lookup"><span data-stu-id="b8deb-154">NOTES</span></span>

## <span data-ttu-id="b8deb-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8deb-155">RELATED LINKS</span></span>

[<span data-ttu-id="b8deb-156">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="b8deb-157">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="b8deb-158">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="b8deb-159">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="b8deb-160">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="b8deb-161">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8deb-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


