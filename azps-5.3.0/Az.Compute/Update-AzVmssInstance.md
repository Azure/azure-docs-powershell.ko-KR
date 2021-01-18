---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495878"
---
# <span data-ttu-id="a6a91-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="a6a91-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="a6a91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a91-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a91-103">VMSS 인스턴스의 수동 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="a6a91-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6a91-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a91-105">설명</span><span class="sxs-lookup"><span data-stu-id="a6a91-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a91-106">Update-AzVmssInstance cmdlet은 지정된 VMSS(Virtual Machine Scale Set) 인스턴스의 수동 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="a6a91-107">VMSS 확장 집합의 업그레이드 정책이 수동으로 설정된 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="a6a91-108">예제</span><span class="sxs-lookup"><span data-stu-id="a6a91-108">EXAMPLES</span></span>

### <span data-ttu-id="a6a91-109">예제 1: VMSS 인스턴스 업그레이드 시작</span><span class="sxs-lookup"><span data-stu-id="a6a91-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="a6a91-110">이 명령은 인스턴스 ID가 0인 VMScaleSet001이라는 VMSS의 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="a6a91-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6a91-111">PARAMETERS</span></span>

### <span data-ttu-id="a6a91-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6a91-112">-AsJob</span></span>
<span data-ttu-id="a6a91-113">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6a91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a91-114">-DefaultProfile</span></span>
<span data-ttu-id="a6a91-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6a91-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a6a91-116">-InstanceId</span></span>
<span data-ttu-id="a6a91-117">문자열 배열로 업그레이드할 인스턴스의 ID 또는 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a91-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a91-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6a91-119">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a6a91-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a6a91-120">-VMScaleSetName</span></span>
<span data-ttu-id="a6a91-121">이 cmdlet이 업그레이드하는 VMSS 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="a6a91-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6a91-122">-Confirm</span></span>
<span data-ttu-id="a6a91-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a91-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a91-124">-WhatIf</span></span>
<span data-ttu-id="a6a91-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6a91-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a91-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a91-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a91-127">CommonParameters</span></span>
<span data-ttu-id="a6a91-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a91-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a91-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6a91-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a91-130">입력</span><span class="sxs-lookup"><span data-stu-id="a6a91-130">INPUTS</span></span>

### <span data-ttu-id="a6a91-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a6a91-131">System.String</span></span>

### <span data-ttu-id="a6a91-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a6a91-132">System.String[]</span></span>

## <span data-ttu-id="a6a91-133">출력</span><span class="sxs-lookup"><span data-stu-id="a6a91-133">OUTPUTS</span></span>

### <span data-ttu-id="a6a91-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a6a91-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a6a91-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6a91-135">NOTES</span></span>

## <span data-ttu-id="a6a91-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a91-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6a91-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a6a91-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


