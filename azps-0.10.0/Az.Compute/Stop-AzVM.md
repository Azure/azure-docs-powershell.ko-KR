---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875994"
---
# <span data-ttu-id="7d24b-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-101">Stop-AzVM</span></span>

## <span data-ttu-id="7d24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d24b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d24b-103">Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7d24b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d24b-104">SYNTAX</span></span>

### <span data-ttu-id="7d24b-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d24b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d24b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7d24b-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d24b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d24b-107">DESCRIPTION</span></span>
<span data-ttu-id="7d24b-108">**AzVM** Cmdlet은 Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7d24b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d24b-109">EXAMPLES</span></span>

### <span data-ttu-id="7d24b-110">예제 1: 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="7d24b-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7d24b-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7d24b-112">변수</span><span class="sxs-lookup"><span data-stu-id="7d24b-112">PARAMETERS</span></span>

### <span data-ttu-id="7d24b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d24b-113">-AsJob</span></span>
<span data-ttu-id="7d24b-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7d24b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d24b-115">-DefaultProfile</span></span>
<span data-ttu-id="7d24b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d24b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7d24b-117">-Force</span></span>
<span data-ttu-id="7d24b-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d24b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="7d24b-119">-Id</span></span>
<span data-ttu-id="7d24b-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-120">The resource group name.</span></span>

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

### <span data-ttu-id="7d24b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7d24b-121">-Name</span></span>
<span data-ttu-id="7d24b-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="7d24b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d24b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d24b-124">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7d24b-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="7d24b-125">-StayProvisioned</span></span>
<span data-ttu-id="7d24b-126">Cmdlet은 VMSS 내의 모든 가상 컴퓨터를 중지 하지만 할당을 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="7d24b-127">중지 된 가상 컴퓨터에 대해 계정이 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="7d24b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="7d24b-128">-Confirm</span></span>
<span data-ttu-id="7d24b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d24b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d24b-130">-WhatIf</span></span>
<span data-ttu-id="7d24b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d24b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d24b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d24b-133">CommonParameters</span></span>
<span data-ttu-id="7d24b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d24b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d24b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d24b-136">입력</span><span class="sxs-lookup"><span data-stu-id="7d24b-136">INPUTS</span></span>

### <span data-ttu-id="7d24b-137">않아야</span><span class="sxs-lookup"><span data-stu-id="7d24b-137">None</span></span>
<span data-ttu-id="7d24b-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d24b-139">출력</span><span class="sxs-lookup"><span data-stu-id="7d24b-139">OUTPUTS</span></span>

### <span data-ttu-id="7d24b-140">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d24b-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7d24b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="7d24b-141">NOTES</span></span>

## <span data-ttu-id="7d24b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d24b-142">RELATED LINKS</span></span>

[<span data-ttu-id="7d24b-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7d24b-144">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7d24b-145">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7d24b-146">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7d24b-147">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7d24b-148">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d24b-148">Update-AzVM</span></span>](./Update-AzVM.md)


