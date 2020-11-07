---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 6582b8d0a141522e6ac8bb4dad23f1da5e31000d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882678"
---
# <span data-ttu-id="30e61-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="30e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e61-102">SYNOPSIS</span></span>
<span data-ttu-id="30e61-103">Vmss 또는 VMSS 내의 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e61-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30e61-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30e61-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30e61-105">DESCRIPTION</span></span>
<span data-ttu-id="30e61-106">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="30e61-107">이 cmdlet은 *InstanceId* 매개 변수를 사용 하 여 vmss 내부의 특정 가상 컴퓨터를 다시 시작 하는 데도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="30e61-108">예제의</span><span class="sxs-lookup"><span data-stu-id="30e61-108">EXAMPLES</span></span>

### <span data-ttu-id="30e61-109">예제 1: VMSS 다시 시작</span><span class="sxs-lookup"><span data-stu-id="30e61-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="30e61-110">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS001 라는 VMSS를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="30e61-111">예제 2: VMSS 내에서 특정 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="30e61-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="30e61-112">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 인 VMSS001 이라는 인스턴스 ID가 1 인 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="30e61-113">변수</span><span class="sxs-lookup"><span data-stu-id="30e61-113">PARAMETERS</span></span>

### <span data-ttu-id="30e61-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30e61-114">-AsJob</span></span>
<span data-ttu-id="30e61-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="30e61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e61-116">-DefaultProfile</span></span>
<span data-ttu-id="30e61-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e61-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="30e61-118">-InstanceId</span></span>
<span data-ttu-id="30e61-119">다시 시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30e61-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e61-120">-ResourceGroupName</span></span>
<span data-ttu-id="30e61-121">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="30e61-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="30e61-122">-VMScaleSetName</span></span>
<span data-ttu-id="30e61-123">이 cmdlet이 다시 시작 하는 VMSS의 이름을 종류에 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30e61-124">-확인</span><span class="sxs-lookup"><span data-stu-id="30e61-124">-Confirm</span></span>
<span data-ttu-id="30e61-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e61-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e61-126">-WhatIf</span></span>
<span data-ttu-id="30e61-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30e61-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e61-129">CommonParameters</span></span>
<span data-ttu-id="30e61-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e61-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e61-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e61-132">입력</span><span class="sxs-lookup"><span data-stu-id="30e61-132">INPUTS</span></span>

### <span data-ttu-id="30e61-133">않아야</span><span class="sxs-lookup"><span data-stu-id="30e61-133">None</span></span>
<span data-ttu-id="30e61-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30e61-135">출력</span><span class="sxs-lookup"><span data-stu-id="30e61-135">OUTPUTS</span></span>

###  
<span data-ttu-id="30e61-136">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30e61-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="30e61-137">상속자</span><span class="sxs-lookup"><span data-stu-id="30e61-137">NOTES</span></span>

## <span data-ttu-id="30e61-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30e61-138">RELATED LINKS</span></span>

[<span data-ttu-id="30e61-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="30e61-140">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="30e61-141">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="30e61-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="30e61-143">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="30e61-144">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="30e61-145">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="30e61-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


