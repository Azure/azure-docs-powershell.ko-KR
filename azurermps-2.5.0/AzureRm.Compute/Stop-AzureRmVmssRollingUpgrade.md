---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvmssrollingupgrade
schema: 2.0.0
ms.openlocfilehash: 8893f5fc8f6bf798635fdfd5e9a16bc4179815e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883122"
---
# <span data-ttu-id="7c7ad-101">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="7c7ad-101">Stop-AzureRmVmssRollingUpgrade</span></span>

## <span data-ttu-id="7c7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7ad-103">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c7ad-104">SYNTAX</span></span>

### <span data-ttu-id="7c7ad-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c7ad-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c7ad-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7c7ad-106">FriendMethod</span></span>
```
Stop-AzureRmVmssRollingUpgrade [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c7ad-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c7ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7c7ad-108">현재 가상 컴퓨터 배율 집합 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-108">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="7c7ad-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c7ad-109">EXAMPLES</span></span>

### <span data-ttu-id="7c7ad-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c7ad-110">Example 1</span></span>
```
PS C:\> Stop-AzureRmVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="7c7ad-111">이 명령은 리소스 그룹 "Group001"의 VM scale 집합 "VMSS001"에서 진행 중인 롤링 업그레이드를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-111">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="7c7ad-112">변수</span><span class="sxs-lookup"><span data-stu-id="7c7ad-112">PARAMETERS</span></span>

### <span data-ttu-id="7c7ad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c7ad-113">-AsJob</span></span>
<span data-ttu-id="7c7ad-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c7ad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c7ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7ad-115">-DefaultProfile</span></span>
<span data-ttu-id="7c7ad-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c7ad-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7c7ad-117">-Force</span></span>
<span data-ttu-id="7c7ad-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c7ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c7ad-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c7ad-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7c7ad-121">-VMScaleSetName</span></span>
<span data-ttu-id="7c7ad-122">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-122">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="7c7ad-123">-확인</span><span class="sxs-lookup"><span data-stu-id="7c7ad-123">-Confirm</span></span>
<span data-ttu-id="7c7ad-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c7ad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c7ad-125">-WhatIf</span></span>
<span data-ttu-id="7c7ad-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c7ad-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c7ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7ad-128">CommonParameters</span></span>
<span data-ttu-id="7c7ad-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7ad-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7ad-131">입력</span><span class="sxs-lookup"><span data-stu-id="7c7ad-131">INPUTS</span></span>

### <span data-ttu-id="7c7ad-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c7ad-132">System.String</span></span>

## <span data-ttu-id="7c7ad-133">출력</span><span class="sxs-lookup"><span data-stu-id="7c7ad-133">OUTPUTS</span></span>

### <span data-ttu-id="7c7ad-134">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7c7ad-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7c7ad-135">NOTES</span></span>

## <span data-ttu-id="7c7ad-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c7ad-136">RELATED LINKS</span></span>
