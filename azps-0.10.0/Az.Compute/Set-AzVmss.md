---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876852"
---
# <span data-ttu-id="d4435-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-101">Set-AzVmss</span></span>

## <span data-ttu-id="d4435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4435-102">SYNOPSIS</span></span>
<span data-ttu-id="d4435-103">지정 된 VMSS에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="d4435-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4435-104">SYNTAX</span></span>

### <span data-ttu-id="d4435-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="d4435-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4435-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="d4435-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4435-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d4435-107">DESCRIPTION</span></span>
<span data-ttu-id="d4435-108">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d4435-109">이 cmdlet이 지 원하는 유일한 작업은 이미지로 서,</span><span class="sxs-lookup"><span data-stu-id="d4435-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="d4435-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d4435-110">EXAMPLES</span></span>

### <span data-ttu-id="d4435-111">예제 1: VMSS를 이미지로</span><span class="sxs-lookup"><span data-stu-id="d4435-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="d4435-112">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 ContosoVMSS 이라는 VMSS를 다시 이미지로 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="d4435-113">변수</span><span class="sxs-lookup"><span data-stu-id="d4435-113">PARAMETERS</span></span>

### <span data-ttu-id="d4435-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4435-114">-AsJob</span></span>
<span data-ttu-id="d4435-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d4435-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4435-116">-DefaultProfile</span></span>
<span data-ttu-id="d4435-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4435-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="d4435-118">-InstanceId</span></span>
<span data-ttu-id="d4435-119">가상 컴퓨터의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="d4435-120">-이미지로</span><span class="sxs-lookup"><span data-stu-id="d4435-120">-Reimage</span></span>
<span data-ttu-id="d4435-121">Cmdlet이 VMSS를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="d4435-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="d4435-122">-ReimageAll</span></span>
<span data-ttu-id="d4435-123">Cmdlet이 VMSS의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="d4435-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4435-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4435-125">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="d4435-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4435-126">-VMScaleSetName</span></span>
<span data-ttu-id="d4435-127">이 cmdlet이 동작을 설정 하는 VMSS의 이름을 종류에 따라 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="d4435-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d4435-128">-Confirm</span></span>
<span data-ttu-id="d4435-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4435-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4435-130">-WhatIf</span></span>
<span data-ttu-id="d4435-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4435-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4435-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4435-133">CommonParameters</span></span>
<span data-ttu-id="d4435-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4435-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4435-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4435-136">입력</span><span class="sxs-lookup"><span data-stu-id="d4435-136">INPUTS</span></span>

### <span data-ttu-id="d4435-137">않아야</span><span class="sxs-lookup"><span data-stu-id="d4435-137">None</span></span>
<span data-ttu-id="d4435-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4435-139">출력</span><span class="sxs-lookup"><span data-stu-id="d4435-139">OUTPUTS</span></span>

### <span data-ttu-id="d4435-140">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4435-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d4435-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d4435-141">NOTES</span></span>

## <span data-ttu-id="d4435-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4435-142">RELATED LINKS</span></span>

[<span data-ttu-id="d4435-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="d4435-144">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="d4435-145">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="d4435-146">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="d4435-147">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="d4435-148">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="d4435-149">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d4435-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


