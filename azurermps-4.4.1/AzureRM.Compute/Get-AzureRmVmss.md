---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533112"
---
# <span data-ttu-id="9b4fd-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="9b4fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4fd-103">VMSS의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b4fd-104">SYNTAX</span></span>

### <span data-ttu-id="9b4fd-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b4fd-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b4fd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9b4fd-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b4fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="9b4fd-108">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)의 모델 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9b4fd-109">모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="9b4fd-110">인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="9b4fd-111">가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="9b4fd-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9b4fd-112">EXAMPLES</span></span>

### <span data-ttu-id="9b4fd-113">예제 1: VMSS의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b4fd-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9b4fd-114">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9b4fd-115">Command는 *Instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="9b4fd-116">변수</span><span class="sxs-lookup"><span data-stu-id="9b4fd-116">PARAMETERS</span></span>

### <span data-ttu-id="9b4fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4fd-117">-DefaultProfile</span></span>
<span data-ttu-id="9b4fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b4fd-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9b4fd-119">-InstanceView</span></span>
<span data-ttu-id="9b4fd-120">이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="9b4fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b4fd-122">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="9b4fd-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9b4fd-123">-VMScaleSetName</span></span>
<span data-ttu-id="9b4fd-124">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="9b4fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4fd-125">CommonParameters</span></span>
<span data-ttu-id="9b4fd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4fd-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4fd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4fd-128">입력</span><span class="sxs-lookup"><span data-stu-id="9b4fd-128">INPUTS</span></span>

## <span data-ttu-id="9b4fd-129">출력</span><span class="sxs-lookup"><span data-stu-id="9b4fd-129">OUTPUTS</span></span>

### <span data-ttu-id="9b4fd-130">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4fd-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9b4fd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9b4fd-131">NOTES</span></span>

## <span data-ttu-id="9b4fd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b4fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b4fd-133">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-134">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-135">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-137">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-138">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="9b4fd-139">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9b4fd-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


