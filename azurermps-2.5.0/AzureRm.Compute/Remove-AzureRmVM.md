---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881118"
---
# <span data-ttu-id="93429-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="93429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93429-102">SYNOPSIS</span></span>
<span data-ttu-id="93429-103">Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93429-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93429-104">SYNTAX</span></span>

### <span data-ttu-id="93429-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="93429-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93429-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="93429-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93429-107">설명은</span><span class="sxs-lookup"><span data-stu-id="93429-107">DESCRIPTION</span></span>
<span data-ttu-id="93429-108">**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="93429-109">예제의</span><span class="sxs-lookup"><span data-stu-id="93429-109">EXAMPLES</span></span>

### <span data-ttu-id="93429-110">예제 1: 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="93429-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="93429-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="93429-112">변수</span><span class="sxs-lookup"><span data-stu-id="93429-112">PARAMETERS</span></span>

### <span data-ttu-id="93429-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93429-113">-AsJob</span></span>
<span data-ttu-id="93429-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="93429-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93429-115">-DefaultProfile</span></span>
<span data-ttu-id="93429-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93429-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93429-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93429-117">-Force</span></span>
<span data-ttu-id="93429-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93429-119">-Id</span><span class="sxs-lookup"><span data-stu-id="93429-119">-Id</span></span>
<span data-ttu-id="93429-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93429-120">The resource group name.</span></span>

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

### <span data-ttu-id="93429-121">-이름</span><span class="sxs-lookup"><span data-stu-id="93429-121">-Name</span></span>
<span data-ttu-id="93429-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93429-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93429-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93429-123">-ResourceGroupName</span></span>
<span data-ttu-id="93429-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93429-125">-확인</span><span class="sxs-lookup"><span data-stu-id="93429-125">-Confirm</span></span>
<span data-ttu-id="93429-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93429-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93429-127">-WhatIf</span></span>
<span data-ttu-id="93429-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93429-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="93429-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93429-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93429-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93429-130">CommonParameters</span></span>
<span data-ttu-id="93429-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93429-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93429-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93429-133">입력</span><span class="sxs-lookup"><span data-stu-id="93429-133">INPUTS</span></span>

### <span data-ttu-id="93429-134">않아야</span><span class="sxs-lookup"><span data-stu-id="93429-134">None</span></span>
<span data-ttu-id="93429-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93429-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93429-136">출력</span><span class="sxs-lookup"><span data-stu-id="93429-136">OUTPUTS</span></span>

### <span data-ttu-id="93429-137">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="93429-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="93429-138">상속자</span><span class="sxs-lookup"><span data-stu-id="93429-138">NOTES</span></span>

## <span data-ttu-id="93429-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93429-139">RELATED LINKS</span></span>

[<span data-ttu-id="93429-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="93429-141">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="93429-142">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="93429-143">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="93429-144">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="93429-145">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="93429-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

