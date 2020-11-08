---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4bf5ec5ccdbe79f5557cb2f400fbcc0b9baf5e5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883138"
---
# <span data-ttu-id="35e1d-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="35e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="35e1d-103">Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35e1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35e1d-104">SYNTAX</span></span>

### <span data-ttu-id="35e1d-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="35e1d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35e1d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="35e1d-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e1d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35e1d-107">DESCRIPTION</span></span>
<span data-ttu-id="35e1d-108">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="35e1d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35e1d-109">EXAMPLES</span></span>

### <span data-ttu-id="35e1d-110">예제 1: 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="35e1d-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="35e1d-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="35e1d-112">변수</span><span class="sxs-lookup"><span data-stu-id="35e1d-112">PARAMETERS</span></span>

### <span data-ttu-id="35e1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35e1d-113">-AsJob</span></span>
<span data-ttu-id="35e1d-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e1d-115">-DefaultProfile</span></span>
<span data-ttu-id="35e1d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35e1d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35e1d-117">-Force</span></span>
<span data-ttu-id="35e1d-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-119">-Id</span><span class="sxs-lookup"><span data-stu-id="35e1d-119">-Id</span></span>
<span data-ttu-id="35e1d-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="35e1d-121">-Name</span></span>
<span data-ttu-id="35e1d-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="35e1d-124">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="35e1d-125">-StayProvisioned</span></span>
<span data-ttu-id="35e1d-126">Cmdlet은 VMSS 내의 모든 가상 컴퓨터를 중지 하지만 할당을 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="35e1d-127">중지 된 가상 컴퓨터에 대해 계정이 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-127">The account is charged for the stopped virtual machines.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="35e1d-128">-Confirm</span></span>
<span data-ttu-id="35e1d-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e1d-130">-WhatIf</span></span>
<span data-ttu-id="35e1d-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35e1d-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e1d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e1d-133">CommonParameters</span></span>
<span data-ttu-id="35e1d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e1d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35e1d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e1d-136">입력</span><span class="sxs-lookup"><span data-stu-id="35e1d-136">INPUTS</span></span>

### <span data-ttu-id="35e1d-137">않아야</span><span class="sxs-lookup"><span data-stu-id="35e1d-137">None</span></span>
<span data-ttu-id="35e1d-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35e1d-139">출력</span><span class="sxs-lookup"><span data-stu-id="35e1d-139">OUTPUTS</span></span>

### <span data-ttu-id="35e1d-140">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="35e1d-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="35e1d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="35e1d-141">NOTES</span></span>

## <span data-ttu-id="35e1d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35e1d-142">RELATED LINKS</span></span>

[<span data-ttu-id="35e1d-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="35e1d-144">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="35e1d-145">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="35e1d-146">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="35e1d-147">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="35e1d-148">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35e1d-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

