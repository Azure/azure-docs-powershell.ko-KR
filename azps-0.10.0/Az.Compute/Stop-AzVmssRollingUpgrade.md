---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 915dd31b522fdbc7955494c0f76d69ee5a4b8376
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875989"
---
# <span data-ttu-id="cc03e-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cc03e-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="cc03e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc03e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc03e-103">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cc03e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc03e-104">SYNTAX</span></span>

### <span data-ttu-id="cc03e-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="cc03e-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc03e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cc03e-106">FriendMethod</span></span>
```
Stop-AzVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc03e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cc03e-107">DESCRIPTION</span></span>
<span data-ttu-id="cc03e-108">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="cc03e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cc03e-109">EXAMPLES</span></span>

### <span data-ttu-id="cc03e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc03e-110">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cc03e-111">이 명령은 리소스 그룹 "Group001"의 VM scale 집합 "VMSS001"에서 진행 중인 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="cc03e-112">변수</span><span class="sxs-lookup"><span data-stu-id="cc03e-112">PARAMETERS</span></span>

### <span data-ttu-id="cc03e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc03e-113">-AsJob</span></span>
<span data-ttu-id="cc03e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cc03e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc03e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc03e-115">-DefaultProfile</span></span>
<span data-ttu-id="cc03e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc03e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc03e-117">-Force</span></span>
<span data-ttu-id="cc03e-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc03e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc03e-119">-ResourceGroupName</span></span>
<span data-ttu-id="cc03e-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc03e-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cc03e-121">-VMScaleSetName</span></span>
<span data-ttu-id="cc03e-122">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-122">The name of the VM scale set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc03e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="cc03e-123">-Confirm</span></span>
<span data-ttu-id="cc03e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc03e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc03e-125">-WhatIf</span></span>
<span data-ttu-id="cc03e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc03e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc03e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc03e-128">CommonParameters</span></span>
<span data-ttu-id="cc03e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc03e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc03e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc03e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc03e-131">입력</span><span class="sxs-lookup"><span data-stu-id="cc03e-131">INPUTS</span></span>

### <span data-ttu-id="cc03e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc03e-132">System.String</span></span>

## <span data-ttu-id="cc03e-133">출력</span><span class="sxs-lookup"><span data-stu-id="cc03e-133">OUTPUTS</span></span>

### <span data-ttu-id="cc03e-134">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="cc03e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cc03e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="cc03e-135">NOTES</span></span>

## <span data-ttu-id="cc03e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc03e-136">RELATED LINKS</span></span>

