---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041568"
---
# <span data-ttu-id="8836a-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8836a-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="8836a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8836a-102">SYNOPSIS</span></span>
<span data-ttu-id="8836a-103">VMSS 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="8836a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8836a-104">SYNTAX</span></span>

### <span data-ttu-id="8836a-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="8836a-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8836a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8836a-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8836a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8836a-107">DESCRIPTION</span></span>
<span data-ttu-id="8836a-108">**AzVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터의 모델 보기와 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="8836a-109">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="8836a-110">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="8836a-111">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="8836a-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8836a-112">EXAMPLES</span></span>

### <span data-ttu-id="8836a-113">예제 1: VMSS 가상 컴퓨터의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8836a-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="8836a-114">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="8836a-115">Command는 *Instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="8836a-116">예제 2: VMSS 가상 컴퓨터의 모델 뷰 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8836a-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="8836a-117">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="8836a-118">명령은 모델 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="8836a-119">예제 3: VMSS 가상 컴퓨터의 인스턴스 보기 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="8836a-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="8836a-120">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="8836a-121">이 명령은 *Instanceview* 스위치 매개 변수를 지정 하므로 cmdlet은 가상 컴퓨터의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="8836a-122">명령에서는 인스턴스 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="8836a-123">변수</span><span class="sxs-lookup"><span data-stu-id="8836a-123">PARAMETERS</span></span>

### <span data-ttu-id="8836a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8836a-124">-DefaultProfile</span></span>
<span data-ttu-id="8836a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8836a-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8836a-126">-InstanceId</span></span>
<span data-ttu-id="8836a-127">모델 보기를 가져올 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8836a-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="8836a-128">-InstanceView</span></span>
<span data-ttu-id="8836a-129">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8836a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8836a-130">-ResourceGroupName</span></span>
<span data-ttu-id="8836a-131">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8836a-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8836a-132">-VMScaleSetName</span></span>
<span data-ttu-id="8836a-133">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8836a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8836a-134">CommonParameters</span></span>
<span data-ttu-id="8836a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8836a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8836a-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8836a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8836a-137">입력</span><span class="sxs-lookup"><span data-stu-id="8836a-137">INPUTS</span></span>

### <span data-ttu-id="8836a-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8836a-138">System.String</span></span>

## <span data-ttu-id="8836a-139">출력</span><span class="sxs-lookup"><span data-stu-id="8836a-139">OUTPUTS</span></span>

### <span data-ttu-id="8836a-140">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="8836a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8836a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8836a-141">NOTES</span></span>

## <span data-ttu-id="8836a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8836a-142">RELATED LINKS</span></span>

[<span data-ttu-id="8836a-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8836a-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="8836a-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8836a-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


