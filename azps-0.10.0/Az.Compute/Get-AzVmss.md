---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877039"
---
# <span data-ttu-id="0cfb7-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-101">Get-AzVmss</span></span>

## <span data-ttu-id="0cfb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cfb7-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfb7-103">VMSS의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="0cfb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cfb7-104">SYNTAX</span></span>

### <span data-ttu-id="0cfb7-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="0cfb7-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cfb7-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0cfb7-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cfb7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0cfb7-107">DESCRIPTION</span></span>
<span data-ttu-id="0cfb7-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)의 모델 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0cfb7-109">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="0cfb7-110">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="0cfb7-111">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="0cfb7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0cfb7-112">EXAMPLES</span></span>

### <span data-ttu-id="0cfb7-113">예제 1: VMSS의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0cfb7-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0cfb7-114">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="0cfb7-115">Command는 *Instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="0cfb7-116">변수</span><span class="sxs-lookup"><span data-stu-id="0cfb7-116">PARAMETERS</span></span>

### <span data-ttu-id="0cfb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfb7-117">-DefaultProfile</span></span>
<span data-ttu-id="0cfb7-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cfb7-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="0cfb7-119">-InstanceView</span></span>
<span data-ttu-id="0cfb7-120">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="0cfb7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cfb7-121">-ResourceGroupName</span></span>
<span data-ttu-id="0cfb7-122">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="0cfb7-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0cfb7-123">-VMScaleSetName</span></span>
<span data-ttu-id="0cfb7-124">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="0cfb7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfb7-125">CommonParameters</span></span>
<span data-ttu-id="0cfb7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfb7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cfb7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfb7-128">입력</span><span class="sxs-lookup"><span data-stu-id="0cfb7-128">INPUTS</span></span>

### <span data-ttu-id="0cfb7-129">않아야</span><span class="sxs-lookup"><span data-stu-id="0cfb7-129">None</span></span>
<span data-ttu-id="0cfb7-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0cfb7-131">출력</span><span class="sxs-lookup"><span data-stu-id="0cfb7-131">OUTPUTS</span></span>

### <span data-ttu-id="0cfb7-132">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfb7-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0cfb7-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0cfb7-133">NOTES</span></span>

## <span data-ttu-id="0cfb7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cfb7-134">RELATED LINKS</span></span>

[<span data-ttu-id="0cfb7-135">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="0cfb7-136">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="0cfb7-137">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="0cfb7-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="0cfb7-139">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="0cfb7-140">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="0cfb7-141">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0cfb7-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


