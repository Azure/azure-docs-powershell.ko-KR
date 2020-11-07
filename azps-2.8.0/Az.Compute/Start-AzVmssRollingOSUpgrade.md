---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: c7804c71ee4cfbccf24e298d2858fa2632f7a2b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697177"
---
# <span data-ttu-id="04419-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="04419-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="04419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04419-102">SYNOPSIS</span></span>
<span data-ttu-id="04419-103">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="04419-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="04419-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04419-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04419-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04419-105">DESCRIPTION</span></span>
<span data-ttu-id="04419-106">모든 가상 컴퓨터 크기 집합 인스턴스를 사용 가능한 최신 플랫폼 이미지 OS 버전으로 이동 하기 위해 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="04419-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="04419-107">사용 가능한 최신 OS 버전을 이미 실행 중인 인스턴스는 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04419-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="04419-108">예제의</span><span class="sxs-lookup"><span data-stu-id="04419-108">EXAMPLES</span></span>

### <span data-ttu-id="04419-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="04419-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="04419-110">이 명령은 리소스 그룹 "Group001"의 VM 확장 집합 "VMSS001"의 모든 vm 인스턴스에 대 한 롤링 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="04419-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="04419-111">변수</span><span class="sxs-lookup"><span data-stu-id="04419-111">PARAMETERS</span></span>

### <span data-ttu-id="04419-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04419-112">-AsJob</span></span>
<span data-ttu-id="04419-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="04419-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04419-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04419-114">-DefaultProfile</span></span>
<span data-ttu-id="04419-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04419-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04419-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04419-116">-ResourceGroupName</span></span>
<span data-ttu-id="04419-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04419-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="04419-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="04419-118">-VMScaleSetName</span></span>
<span data-ttu-id="04419-119">VM 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04419-119">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="04419-120">-확인</span><span class="sxs-lookup"><span data-stu-id="04419-120">-Confirm</span></span>
<span data-ttu-id="04419-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04419-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04419-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04419-122">-WhatIf</span></span>
<span data-ttu-id="04419-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04419-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04419-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04419-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04419-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04419-125">CommonParameters</span></span>
<span data-ttu-id="04419-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04419-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04419-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04419-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04419-128">입력</span><span class="sxs-lookup"><span data-stu-id="04419-128">INPUTS</span></span>

### <span data-ttu-id="04419-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04419-129">System.String</span></span>

## <span data-ttu-id="04419-130">출력</span><span class="sxs-lookup"><span data-stu-id="04419-130">OUTPUTS</span></span>

### <span data-ttu-id="04419-131">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="04419-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="04419-132">상속자</span><span class="sxs-lookup"><span data-stu-id="04419-132">NOTES</span></span>

## <span data-ttu-id="04419-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04419-133">RELATED LINKS</span></span>
