---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204641"
---
# <span data-ttu-id="81e07-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="81e07-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="81e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81e07-102">SYNOPSIS</span></span>
<span data-ttu-id="81e07-103">가상 컴퓨터의 패치 상태를 평가 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="81e07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81e07-104">SYNTAX</span></span>

### <span data-ttu-id="81e07-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="81e07-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e07-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e07-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e07-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e07-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e07-108">설명은</span><span class="sxs-lookup"><span data-stu-id="81e07-108">DESCRIPTION</span></span>
<span data-ttu-id="81e07-109">VM의 패치 상태를 평가 하 고 설치에 사용할 수 있는 모든 검색 된 패치를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="81e07-110">예제의</span><span class="sxs-lookup"><span data-stu-id="81e07-110">EXAMPLES</span></span>

### <span data-ttu-id="81e07-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="81e07-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="81e07-112">변수</span><span class="sxs-lookup"><span data-stu-id="81e07-112">PARAMETERS</span></span>

### <span data-ttu-id="81e07-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81e07-113">-AsJob</span></span>
<span data-ttu-id="81e07-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="81e07-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81e07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e07-115">-DefaultProfile</span></span>
<span data-ttu-id="81e07-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e07-117">-ResourceGroupName</span></span>
<span data-ttu-id="81e07-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e07-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e07-119">-ResourceId</span></span>
<span data-ttu-id="81e07-120">가상 컴퓨터의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e07-121">-VM</span><span class="sxs-lookup"><span data-stu-id="81e07-121">-VM</span></span>
<span data-ttu-id="81e07-122">PowerShell 가상 컴퓨터 개체</span><span class="sxs-lookup"><span data-stu-id="81e07-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e07-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="81e07-123">-VMName</span></span>
<span data-ttu-id="81e07-124">가상 머신 이름</span><span class="sxs-lookup"><span data-stu-id="81e07-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e07-125">-확인</span><span class="sxs-lookup"><span data-stu-id="81e07-125">-Confirm</span></span>
<span data-ttu-id="81e07-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e07-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e07-127">-WhatIf</span></span>
<span data-ttu-id="81e07-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81e07-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e07-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e07-130">CommonParameters</span></span>
<span data-ttu-id="81e07-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e07-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e07-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81e07-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e07-133">입력</span><span class="sxs-lookup"><span data-stu-id="81e07-133">INPUTS</span></span>

### <span data-ttu-id="81e07-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="81e07-134">System.String</span></span>

## <span data-ttu-id="81e07-135">출력</span><span class="sxs-lookup"><span data-stu-id="81e07-135">OUTPUTS</span></span>

### <span data-ttu-id="81e07-136">PSVirtualMachinePatchAssessmentResult의. m a.</span><span class="sxs-lookup"><span data-stu-id="81e07-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="81e07-137">상속자</span><span class="sxs-lookup"><span data-stu-id="81e07-137">NOTES</span></span>

## <span data-ttu-id="81e07-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81e07-138">RELATED LINKS</span></span>
