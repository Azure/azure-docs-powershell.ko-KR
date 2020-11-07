---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvm
schema: 2.0.0
ms.openlocfilehash: bac1bf365ff1135366f2612bfbe5ba313e2300b8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883150"
---
# <span data-ttu-id="06e7f-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="06e7f-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="06e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="06e7f-103">VMSS 가상 컴퓨터의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06e7f-104">SYNTAX</span></span>

### <span data-ttu-id="06e7f-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="06e7f-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06e7f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="06e7f-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06e7f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06e7f-107">DESCRIPTION</span></span>
<span data-ttu-id="06e7f-108">**AzureRmVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터의 모델 보기와 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="06e7f-109">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="06e7f-110">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="06e7f-111">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="06e7f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="06e7f-112">EXAMPLES</span></span>

### <span data-ttu-id="06e7f-113">예제 1: VMSS 가상 컴퓨터의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="06e7f-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="06e7f-114">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="06e7f-115">Command는 *Instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="06e7f-116">예제 2: VMSS 가상 컴퓨터의 모델 뷰 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="06e7f-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="06e7f-117">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="06e7f-118">명령은 모델 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="06e7f-119">예제 3: VMSS 가상 컴퓨터의 인스턴스 보기 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="06e7f-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="06e7f-120">이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="06e7f-121">이 명령은 *Instanceview* 스위치 매개 변수를 지정 하므로 cmdlet은 가상 컴퓨터의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="06e7f-122">명령에서는 인스턴스 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="06e7f-123">변수</span><span class="sxs-lookup"><span data-stu-id="06e7f-123">PARAMETERS</span></span>

### <span data-ttu-id="06e7f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e7f-124">-DefaultProfile</span></span>
<span data-ttu-id="06e7f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06e7f-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="06e7f-126">-InstanceId</span></span>
<span data-ttu-id="06e7f-127">모델 보기를 가져올 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-127">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e7f-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="06e7f-128">-InstanceView</span></span>
<span data-ttu-id="06e7f-129">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e7f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e7f-130">-ResourceGroupName</span></span>
<span data-ttu-id="06e7f-131">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e7f-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="06e7f-132">-VMScaleSetName</span></span>
<span data-ttu-id="06e7f-133">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-133">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e7f-134">CommonParameters</span></span>
<span data-ttu-id="06e7f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e7f-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e7f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e7f-137">입력</span><span class="sxs-lookup"><span data-stu-id="06e7f-137">INPUTS</span></span>

### <span data-ttu-id="06e7f-138">않아야</span><span class="sxs-lookup"><span data-stu-id="06e7f-138">None</span></span>
<span data-ttu-id="06e7f-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06e7f-140">출력</span><span class="sxs-lookup"><span data-stu-id="06e7f-140">OUTPUTS</span></span>

### <span data-ttu-id="06e7f-141">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06e7f-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="06e7f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="06e7f-142">NOTES</span></span>

## <span data-ttu-id="06e7f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06e7f-143">RELATED LINKS</span></span>

[<span data-ttu-id="06e7f-144">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="06e7f-144">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="06e7f-145">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="06e7f-145">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


