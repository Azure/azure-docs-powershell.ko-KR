---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881598"
---
# <span data-ttu-id="611f1-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="611f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611f1-102">SYNOPSIS</span></span>
<span data-ttu-id="611f1-103">지정 된 VMSS에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="611f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="611f1-104">SYNTAX</span></span>

### <span data-ttu-id="611f1-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="611f1-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="611f1-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="611f1-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="611f1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="611f1-107">DESCRIPTION</span></span>
<span data-ttu-id="611f1-108">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="611f1-109">이 cmdlet이 지 원하는 유일한 작업은 이미지로 서,</span><span class="sxs-lookup"><span data-stu-id="611f1-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="611f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="611f1-110">EXAMPLES</span></span>

### <span data-ttu-id="611f1-111">예제 1: VMSS를 이미지로</span><span class="sxs-lookup"><span data-stu-id="611f1-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="611f1-112">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 ContosoVMSS 이라는 VMSS를 다시 이미지로 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="611f1-113">변수</span><span class="sxs-lookup"><span data-stu-id="611f1-113">PARAMETERS</span></span>

### <span data-ttu-id="611f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="611f1-114">-AsJob</span></span>
<span data-ttu-id="611f1-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="611f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611f1-116">-DefaultProfile</span></span>
<span data-ttu-id="611f1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="611f1-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="611f1-118">-InstanceId</span></span>
<span data-ttu-id="611f1-119">가상 컴퓨터의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="611f1-120">-이미지로</span><span class="sxs-lookup"><span data-stu-id="611f1-120">-Reimage</span></span>
<span data-ttu-id="611f1-121">Cmdlet이 VMSS를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611f1-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="611f1-122">-ReimageAll</span></span>
<span data-ttu-id="611f1-123">Cmdlet이 VMSS의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="611f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="611f1-125">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="611f1-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="611f1-126">-VMScaleSetName</span></span>
<span data-ttu-id="611f1-127">이 cmdlet이 동작을 설정 하는 VMSS의 이름을 종류에 따라 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="611f1-128">-확인</span><span class="sxs-lookup"><span data-stu-id="611f1-128">-Confirm</span></span>
<span data-ttu-id="611f1-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="611f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="611f1-130">-WhatIf</span></span>
<span data-ttu-id="611f1-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="611f1-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="611f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611f1-133">CommonParameters</span></span>
<span data-ttu-id="611f1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611f1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611f1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611f1-136">입력</span><span class="sxs-lookup"><span data-stu-id="611f1-136">INPUTS</span></span>

### <span data-ttu-id="611f1-137">않아야</span><span class="sxs-lookup"><span data-stu-id="611f1-137">None</span></span>
<span data-ttu-id="611f1-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="611f1-139">출력</span><span class="sxs-lookup"><span data-stu-id="611f1-139">OUTPUTS</span></span>

### <span data-ttu-id="611f1-140">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611f1-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="611f1-141">상속자</span><span class="sxs-lookup"><span data-stu-id="611f1-141">NOTES</span></span>

## <span data-ttu-id="611f1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="611f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="611f1-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="611f1-144">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="611f1-145">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="611f1-146">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="611f1-147">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="611f1-148">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="611f1-149">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="611f1-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


