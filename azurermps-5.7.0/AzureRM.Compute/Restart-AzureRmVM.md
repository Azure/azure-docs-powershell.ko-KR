---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
ms.openlocfilehash: f77c85b21cff7db124f2d190997c5907835f0cf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529885"
---
# <span data-ttu-id="58509-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="58509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58509-102">SYNOPSIS</span></span>
<span data-ttu-id="58509-103">Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58509-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58509-104">SYNTAX</span></span>

### <span data-ttu-id="58509-105">RestartResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="58509-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58509-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58509-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58509-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58509-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58509-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58509-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58509-109">설명은</span><span class="sxs-lookup"><span data-stu-id="58509-109">DESCRIPTION</span></span>
<span data-ttu-id="58509-110">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="58509-111">예제의</span><span class="sxs-lookup"><span data-stu-id="58509-111">EXAMPLES</span></span>

### <span data-ttu-id="58509-112">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="58509-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="58509-113">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="58509-114">변수</span><span class="sxs-lookup"><span data-stu-id="58509-114">PARAMETERS</span></span>

### <span data-ttu-id="58509-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58509-115">-AsJob</span></span>
<span data-ttu-id="58509-116">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="58509-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58509-117">-DefaultProfile</span></span>
<span data-ttu-id="58509-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58509-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58509-119">-Id</span><span class="sxs-lookup"><span data-stu-id="58509-119">-Id</span></span>
<span data-ttu-id="58509-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58509-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58509-121">-이름</span><span class="sxs-lookup"><span data-stu-id="58509-121">-Name</span></span>
<span data-ttu-id="58509-122">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58509-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="58509-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="58509-123">-PerformMaintenance</span></span>
<span data-ttu-id="58509-124">가상 컴퓨터의 유지 관리를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58509-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58509-125">-ResourceGroupName</span></span>
<span data-ttu-id="58509-126">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58509-127">-확인</span><span class="sxs-lookup"><span data-stu-id="58509-127">-Confirm</span></span>
<span data-ttu-id="58509-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58509-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58509-129">-WhatIf</span></span>
<span data-ttu-id="58509-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58509-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58509-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58509-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58509-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58509-132">CommonParameters</span></span>
<span data-ttu-id="58509-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58509-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58509-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58509-135">입력</span><span class="sxs-lookup"><span data-stu-id="58509-135">INPUTS</span></span>

### <span data-ttu-id="58509-136">않아야</span><span class="sxs-lookup"><span data-stu-id="58509-136">None</span></span>
<span data-ttu-id="58509-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58509-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58509-138">출력</span><span class="sxs-lookup"><span data-stu-id="58509-138">OUTPUTS</span></span>

### <span data-ttu-id="58509-139">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="58509-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="58509-140">상속자</span><span class="sxs-lookup"><span data-stu-id="58509-140">NOTES</span></span>

## <span data-ttu-id="58509-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58509-141">RELATED LINKS</span></span>

[<span data-ttu-id="58509-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="58509-143">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="58509-144">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="58509-145">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="58509-146">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="58509-147">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="58509-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


