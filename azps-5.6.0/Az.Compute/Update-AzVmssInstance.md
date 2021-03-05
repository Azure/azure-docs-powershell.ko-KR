---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: ed0ad08d94cbc67832b6a0dbb85882bd18692d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992847"
---
# <span data-ttu-id="706df-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="706df-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="706df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706df-102">SYNOPSIS</span></span>
<span data-ttu-id="706df-103">VMSS 인스턴스의 수동 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="706df-104">구문</span><span class="sxs-lookup"><span data-stu-id="706df-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="706df-105">설명</span><span class="sxs-lookup"><span data-stu-id="706df-105">DESCRIPTION</span></span>
<span data-ttu-id="706df-106">Update-AzVmssInstance cmdlet은 지정된 VMSS(Virtual Machine Scale Set) 인스턴스의 수동 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="706df-107">VMSS 확장 집합의 업그레이드 정책이 수동으로 설정되어 있는 경우 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="706df-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="706df-108">예제</span><span class="sxs-lookup"><span data-stu-id="706df-108">EXAMPLES</span></span>

### <span data-ttu-id="706df-109">예제 1: VMSS 인스턴스 업그레이드 시작</span><span class="sxs-lookup"><span data-stu-id="706df-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="706df-110">이 명령은 인스턴스 ID가 0인 VMScaleSet001이라는 VMSS의 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="706df-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="706df-111">PARAMETERS</span></span>

### <span data-ttu-id="706df-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="706df-112">-AsJob</span></span>
<span data-ttu-id="706df-113">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="706df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706df-114">-DefaultProfile</span></span>
<span data-ttu-id="706df-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="706df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="706df-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="706df-116">-InstanceId</span></span>
<span data-ttu-id="706df-117">업그레이드할 인스턴스의 ID 또는 ID를 문자열 배열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

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

### <span data-ttu-id="706df-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706df-118">-ResourceGroupName</span></span>
<span data-ttu-id="706df-119">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="706df-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="706df-120">-VMScaleSetName</span></span>
<span data-ttu-id="706df-121">이 cmdlet이 업그레이드하는 VMSS 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="706df-122">-확인</span><span class="sxs-lookup"><span data-stu-id="706df-122">-Confirm</span></span>
<span data-ttu-id="706df-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="706df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="706df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706df-124">-WhatIf</span></span>
<span data-ttu-id="706df-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="706df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="706df-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="706df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="706df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706df-127">CommonParameters</span></span>
<span data-ttu-id="706df-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="706df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706df-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="706df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706df-130">입력</span><span class="sxs-lookup"><span data-stu-id="706df-130">INPUTS</span></span>

### <span data-ttu-id="706df-131">System.String</span><span class="sxs-lookup"><span data-stu-id="706df-131">System.String</span></span>

### <span data-ttu-id="706df-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="706df-132">System.String[]</span></span>

## <span data-ttu-id="706df-133">출력</span><span class="sxs-lookup"><span data-stu-id="706df-133">OUTPUTS</span></span>

### <span data-ttu-id="706df-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="706df-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="706df-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="706df-135">NOTES</span></span>

## <span data-ttu-id="706df-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="706df-136">RELATED LINKS</span></span>

[<span data-ttu-id="706df-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="706df-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


