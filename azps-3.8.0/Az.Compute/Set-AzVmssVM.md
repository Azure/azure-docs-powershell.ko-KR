---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 32e04fb16d0e3360abb22177e453d5d629dbb098
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044607"
---
# <span data-ttu-id="8a818-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8a818-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="8a818-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a818-102">SYNOPSIS</span></span>
<span data-ttu-id="8a818-103">VMSS 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="8a818-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a818-104">SYNTAX</span></span>

### <span data-ttu-id="8a818-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a818-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a818-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="8a818-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a818-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8a818-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a818-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="8a818-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a818-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8a818-109">DESCRIPTION</span></span>
<span data-ttu-id="8a818-110">**AzVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 인스턴스의 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8a818-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8a818-111">EXAMPLES</span></span>

## <span data-ttu-id="8a818-112">변수</span><span class="sxs-lookup"><span data-stu-id="8a818-112">PARAMETERS</span></span>

### <span data-ttu-id="8a818-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a818-113">-AsJob</span></span>
<span data-ttu-id="8a818-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8a818-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a818-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a818-115">-DefaultProfile</span></span>
<span data-ttu-id="8a818-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a818-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="8a818-117">-InstanceId</span></span>
<span data-ttu-id="8a818-118">이 cmdlet에서 상태를 수정 하는 VMSS 인스턴스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a818-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="8a818-119">-PerformMaintenance</span></span>
<span data-ttu-id="8a818-120">이 cmdlet이 VMSS의 가상 컴퓨터에서 유지 관리를 수행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="8a818-121">-재배포</span><span class="sxs-lookup"><span data-stu-id="8a818-121">-Redeploy</span></span>
<span data-ttu-id="8a818-122">이 cmdlet이 VMSS에서 가상 컴퓨터를 다시 배포 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

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

### <span data-ttu-id="8a818-123">-이미지로</span><span class="sxs-lookup"><span data-stu-id="8a818-123">-Reimage</span></span>
<span data-ttu-id="8a818-124">이 cmdlet이 VMSS 인스턴스를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

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

### <span data-ttu-id="8a818-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="8a818-125">-ReimageAll</span></span>
<span data-ttu-id="8a818-126">Cmdlet이 VMSS 인스턴스의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

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

### <span data-ttu-id="8a818-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a818-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a818-128">VMSS 인스턴스가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="8a818-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8a818-129">-VMScaleSetName</span></span>
<span data-ttu-id="8a818-130">이 cmdlet이 수정 하는 VMSS 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8a818-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8a818-131">-Confirm</span></span>
<span data-ttu-id="8a818-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a818-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a818-133">-WhatIf</span></span>
<span data-ttu-id="8a818-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a818-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a818-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a818-136">CommonParameters</span></span>
<span data-ttu-id="8a818-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a818-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a818-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a818-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a818-139">입력</span><span class="sxs-lookup"><span data-stu-id="8a818-139">INPUTS</span></span>

### <span data-ttu-id="8a818-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a818-140">System.String</span></span>

## <span data-ttu-id="8a818-141">출력</span><span class="sxs-lookup"><span data-stu-id="8a818-141">OUTPUTS</span></span>

### <span data-ttu-id="8a818-142">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="8a818-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8a818-143">상속자</span><span class="sxs-lookup"><span data-stu-id="8a818-143">NOTES</span></span>

## <span data-ttu-id="8a818-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a818-144">RELATED LINKS</span></span>

[<span data-ttu-id="8a818-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="8a818-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)