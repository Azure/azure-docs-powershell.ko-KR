---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 99f022f539ff5db9bb99537bb87fce8a8567947c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868873"
---
# <span data-ttu-id="f3900-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-101">Set-AzVmss</span></span>

## <span data-ttu-id="f3900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3900-102">SYNOPSIS</span></span>
<span data-ttu-id="f3900-103">지정 된 VMSS에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="f3900-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3900-104">SYNTAX</span></span>

### <span data-ttu-id="f3900-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3900-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3900-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f3900-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3900-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="f3900-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3900-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="f3900-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3900-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f3900-109">DESCRIPTION</span></span>
<span data-ttu-id="f3900-110">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f3900-111">이 cmdlet이 지 원하는 유일한 작업은 이미지로 서,</span><span class="sxs-lookup"><span data-stu-id="f3900-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="f3900-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f3900-112">EXAMPLES</span></span>

### <span data-ttu-id="f3900-113">예제 1: VMSS를 이미지로</span><span class="sxs-lookup"><span data-stu-id="f3900-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f3900-114">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 ContosoVMSS 이라는 VMSS를 다시 이미지로 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f3900-115">변수</span><span class="sxs-lookup"><span data-stu-id="f3900-115">PARAMETERS</span></span>

### <span data-ttu-id="f3900-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3900-116">-AsJob</span></span>
<span data-ttu-id="f3900-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3900-118">-DefaultProfile</span></span>
<span data-ttu-id="f3900-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f3900-120">-InstanceId</span></span>
<span data-ttu-id="f3900-121">가상 컴퓨터의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-121">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="f3900-122">-PerformMaintenance</span></span>
<span data-ttu-id="f3900-123">이 cmdlet이 VMSS에서 하나 이상의 가상 컴퓨터 유지 관리를 수행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-124">-재배포</span><span class="sxs-lookup"><span data-stu-id="f3900-124">-Redeploy</span></span>
<span data-ttu-id="f3900-125">Cmdlet이 VMSS에 하나 이상의 가상 컴퓨터를 다시 배포 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-126">-이미지로</span><span class="sxs-lookup"><span data-stu-id="f3900-126">-Reimage</span></span>
<span data-ttu-id="f3900-127">Cmdlet이 VMSS를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-128">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f3900-128">-ReimageAll</span></span>
<span data-ttu-id="f3900-129">Cmdlet이 VMSS의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="f3900-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3900-130">-ResourceGroupName</span></span>
<span data-ttu-id="f3900-131">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="f3900-132">-TempDisk</span></span>
<span data-ttu-id="f3900-133">Temp 디스크를 이미지로 인쇄할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f3900-134">-VMScaleSetName</span></span>
<span data-ttu-id="f3900-135">이 cmdlet이 동작을 설정 하는 VMSS의 이름을 종류에 따라 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-136">-확인</span><span class="sxs-lookup"><span data-stu-id="f3900-136">-Confirm</span></span>
<span data-ttu-id="f3900-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3900-138">-WhatIf</span></span>
<span data-ttu-id="f3900-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3900-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3900-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3900-141">CommonParameters</span></span>
<span data-ttu-id="f3900-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3900-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3900-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3900-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3900-144">입력</span><span class="sxs-lookup"><span data-stu-id="f3900-144">INPUTS</span></span>

### <span data-ttu-id="f3900-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3900-145">System.String</span></span>

### <span data-ttu-id="f3900-146">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f3900-146">System.String[]</span></span>

## <span data-ttu-id="f3900-147">출력</span><span class="sxs-lookup"><span data-stu-id="f3900-147">OUTPUTS</span></span>

### <span data-ttu-id="f3900-148">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="f3900-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f3900-149">상속자</span><span class="sxs-lookup"><span data-stu-id="f3900-149">NOTES</span></span>

## <span data-ttu-id="f3900-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3900-150">RELATED LINKS</span></span>

[<span data-ttu-id="f3900-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f3900-152">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f3900-153">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f3900-154">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="f3900-155">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f3900-156">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f3900-157">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f3900-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


