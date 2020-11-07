---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876924"
---
# <span data-ttu-id="33a5b-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-101">Restart-AzVmss</span></span>

## <span data-ttu-id="33a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="33a5b-103">Vmss 또는 VMSS 내의 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="33a5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33a5b-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a5b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="33a5b-106">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="33a5b-107">이 cmdlet은 *InstanceId* 매개 변수를 사용 하 여 vmss 내부의 특정 가상 컴퓨터를 다시 시작 하는 데도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="33a5b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="33a5b-108">EXAMPLES</span></span>

### <span data-ttu-id="33a5b-109">예제 1: VMSS 다시 시작</span><span class="sxs-lookup"><span data-stu-id="33a5b-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="33a5b-110">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS001 라는 VMSS를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="33a5b-111">예제 2: VMSS 내에서 특정 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="33a5b-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="33a5b-112">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 인 VMSS001 이라는 인스턴스 ID가 1 인 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="33a5b-113">변수</span><span class="sxs-lookup"><span data-stu-id="33a5b-113">PARAMETERS</span></span>

### <span data-ttu-id="33a5b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33a5b-114">-AsJob</span></span>
<span data-ttu-id="33a5b-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="33a5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a5b-116">-DefaultProfile</span></span>
<span data-ttu-id="33a5b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a5b-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="33a5b-118">-InstanceId</span></span>
<span data-ttu-id="33a5b-119">다시 시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="33a5b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33a5b-120">-ResourceGroupName</span></span>
<span data-ttu-id="33a5b-121">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="33a5b-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="33a5b-122">-VMScaleSetName</span></span>
<span data-ttu-id="33a5b-123">이 cmdlet이 다시 시작 하는 VMSS의 이름을 종류에 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="33a5b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="33a5b-124">-Confirm</span></span>
<span data-ttu-id="33a5b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33a5b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a5b-126">-WhatIf</span></span>
<span data-ttu-id="33a5b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33a5b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33a5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a5b-129">CommonParameters</span></span>
<span data-ttu-id="33a5b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a5b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a5b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a5b-132">입력</span><span class="sxs-lookup"><span data-stu-id="33a5b-132">INPUTS</span></span>

### <span data-ttu-id="33a5b-133">않아야</span><span class="sxs-lookup"><span data-stu-id="33a5b-133">None</span></span>
<span data-ttu-id="33a5b-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33a5b-135">출력</span><span class="sxs-lookup"><span data-stu-id="33a5b-135">OUTPUTS</span></span>

###  
<span data-ttu-id="33a5b-136">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33a5b-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="33a5b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="33a5b-137">NOTES</span></span>

## <span data-ttu-id="33a5b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33a5b-138">RELATED LINKS</span></span>

[<span data-ttu-id="33a5b-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="33a5b-140">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="33a5b-141">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="33a5b-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="33a5b-143">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="33a5b-144">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="33a5b-145">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="33a5b-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


