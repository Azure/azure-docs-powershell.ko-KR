---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: fb35bac6f43ca444762ed1cbf8511d93eab10daf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868846"
---
# <span data-ttu-id="35b5b-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="35b5b-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="35b5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="35b5b-103">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="35b5b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35b5b-104">SYNTAX</span></span>

### <span data-ttu-id="35b5b-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="35b5b-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35b5b-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="35b5b-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35b5b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35b5b-107">DESCRIPTION</span></span>
<span data-ttu-id="35b5b-108">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="35b5b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35b5b-109">EXAMPLES</span></span>

### <span data-ttu-id="35b5b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="35b5b-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="35b5b-111">이 명령은 리소스 그룹 "Group001"의 VM scale 집합 "VMSS001"에서 진행 중인 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="35b5b-112">변수</span><span class="sxs-lookup"><span data-stu-id="35b5b-112">PARAMETERS</span></span>

### <span data-ttu-id="35b5b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35b5b-113">-AsJob</span></span>
<span data-ttu-id="35b5b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="35b5b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35b5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b5b-115">-DefaultProfile</span></span>
<span data-ttu-id="35b5b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35b5b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="35b5b-117">-Force</span></span>
<span data-ttu-id="35b5b-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35b5b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35b5b-119">-ResourceGroupName</span></span>
<span data-ttu-id="35b5b-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b5b-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="35b5b-121">-VMScaleSetName</span></span>
<span data-ttu-id="35b5b-122">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-122">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b5b-123">-확인</span><span class="sxs-lookup"><span data-stu-id="35b5b-123">-Confirm</span></span>
<span data-ttu-id="35b5b-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b5b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b5b-125">-WhatIf</span></span>
<span data-ttu-id="35b5b-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35b5b-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b5b-128">CommonParameters</span></span>
<span data-ttu-id="35b5b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b5b-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35b5b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b5b-131">입력</span><span class="sxs-lookup"><span data-stu-id="35b5b-131">INPUTS</span></span>

### <span data-ttu-id="35b5b-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35b5b-132">System.String</span></span>

## <span data-ttu-id="35b5b-133">출력</span><span class="sxs-lookup"><span data-stu-id="35b5b-133">OUTPUTS</span></span>

### <span data-ttu-id="35b5b-134">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="35b5b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="35b5b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="35b5b-135">NOTES</span></span>

## <span data-ttu-id="35b5b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35b5b-136">RELATED LINKS</span></span>
