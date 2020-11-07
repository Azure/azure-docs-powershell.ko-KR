---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878374"
---
# <span data-ttu-id="56e8e-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="56e8e-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="56e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="56e8e-103">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="56e8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56e8e-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e8e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="56e8e-106">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="56e8e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="56e8e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="56e8e-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="56e8e-109">이 명령은 리소스 그룹 "Group001"의 VM scale 집합 "VMSS001"에서 진행 중인 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="56e8e-110">변수</span><span class="sxs-lookup"><span data-stu-id="56e8e-110">PARAMETERS</span></span>

### <span data-ttu-id="56e8e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56e8e-111">-AsJob</span></span>
<span data-ttu-id="56e8e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56e8e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56e8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e8e-113">-DefaultProfile</span></span>
<span data-ttu-id="56e8e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e8e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56e8e-115">-Force</span></span>
<span data-ttu-id="56e8e-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56e8e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e8e-117">-ResourceGroupName</span></span>
<span data-ttu-id="56e8e-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="56e8e-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56e8e-119">-VMScaleSetName</span></span>
<span data-ttu-id="56e8e-120">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="56e8e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="56e8e-121">-Confirm</span></span>
<span data-ttu-id="56e8e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e8e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e8e-123">-WhatIf</span></span>
<span data-ttu-id="56e8e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e8e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e8e-126">CommonParameters</span></span>
<span data-ttu-id="56e8e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56e8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e8e-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56e8e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e8e-129">입력</span><span class="sxs-lookup"><span data-stu-id="56e8e-129">INPUTS</span></span>

### <span data-ttu-id="56e8e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56e8e-130">System.String</span></span>

## <span data-ttu-id="56e8e-131">출력</span><span class="sxs-lookup"><span data-stu-id="56e8e-131">OUTPUTS</span></span>

### <span data-ttu-id="56e8e-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="56e8e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="56e8e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="56e8e-133">NOTES</span></span>

## <span data-ttu-id="56e8e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56e8e-134">RELATED LINKS</span></span>
