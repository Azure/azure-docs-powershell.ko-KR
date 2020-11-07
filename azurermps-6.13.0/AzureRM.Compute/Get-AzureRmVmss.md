---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703907"
---
# <span data-ttu-id="3d4de-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="3d4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d4de-102">SYNOPSIS</span></span>
<span data-ttu-id="3d4de-103">VMSS의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d4de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d4de-104">SYNTAX</span></span>

### <span data-ttu-id="3d4de-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d4de-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d4de-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="3d4de-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d4de-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="3d4de-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d4de-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d4de-108">DESCRIPTION</span></span>
<span data-ttu-id="3d4de-109">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)의 모델 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3d4de-110">모델 보기는 사용자가 가상 컴퓨터 크기 조정 집합의 속성을 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="3d4de-111">인스턴스 뷰는 가상 머신 배율 집합의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="3d4de-112">가상 컴퓨터 배율 집합의 인스턴스 보기만 가져오려면 *instanceview* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="3d4de-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3d4de-113">EXAMPLES</span></span>

### <span data-ttu-id="3d4de-114">예제 1: VMSS의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="3d4de-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="3d4de-115">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="3d4de-116">Command는 *instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터 배율 집합의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="3d4de-117">변수</span><span class="sxs-lookup"><span data-stu-id="3d4de-117">PARAMETERS</span></span>

### <span data-ttu-id="3d4de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d4de-118">-DefaultProfile</span></span>
<span data-ttu-id="3d4de-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d4de-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="3d4de-120">-InstanceView</span></span>
<span data-ttu-id="3d4de-121">이 cmdlet이 가상 컴퓨터 배율 집합의 인스턴스 보기만 가져오고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="3d4de-122">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="3d4de-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="3d4de-123">이 cmdlet에 가상 머신 크기 집합의 os 업그레이드 기록이 나열 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d4de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d4de-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d4de-125">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-125">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="3d4de-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3d4de-126">-VMScaleSetName</span></span>
<span data-ttu-id="3d4de-127">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-127">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d4de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d4de-128">CommonParameters</span></span>
<span data-ttu-id="3d4de-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d4de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d4de-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d4de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d4de-131">입력</span><span class="sxs-lookup"><span data-stu-id="3d4de-131">INPUTS</span></span>

### <span data-ttu-id="3d4de-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d4de-132">System.String</span></span>

## <span data-ttu-id="3d4de-133">출력</span><span class="sxs-lookup"><span data-stu-id="3d4de-133">OUTPUTS</span></span>

### <span data-ttu-id="3d4de-134">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="3d4de-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3d4de-135">상속자</span><span class="sxs-lookup"><span data-stu-id="3d4de-135">NOTES</span></span>

## <span data-ttu-id="3d4de-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d4de-136">RELATED LINKS</span></span>

[<span data-ttu-id="3d4de-137">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3d4de-138">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="3d4de-139">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="3d4de-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="3d4de-141">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3d4de-142">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3d4de-143">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d4de-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


