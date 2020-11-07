---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876980"
---
# <span data-ttu-id="d3df1-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d3df1-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="d3df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3df1-102">SYNOPSIS</span></span>
<span data-ttu-id="d3df1-103">Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="d3df1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3df1-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3df1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3df1-105">DESCRIPTION</span></span>
<span data-ttu-id="d3df1-106">**AzAvailabilitySet** Cmdlet은 Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="d3df1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3df1-107">EXAMPLES</span></span>

### <span data-ttu-id="d3df1-108">예제 1: 가용성 집합 제거</span><span class="sxs-lookup"><span data-stu-id="d3df1-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d3df1-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d3df1-110">변수</span><span class="sxs-lookup"><span data-stu-id="d3df1-110">PARAMETERS</span></span>

### <span data-ttu-id="d3df1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3df1-111">-AsJob</span></span>
<span data-ttu-id="d3df1-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d3df1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3df1-113">-DefaultProfile</span></span>
<span data-ttu-id="d3df1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3df1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d3df1-115">-Force</span></span>
<span data-ttu-id="d3df1-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3df1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d3df1-117">-Name</span></span>
<span data-ttu-id="d3df1-118">가용성 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-118">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3df1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3df1-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3df1-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3df1-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d3df1-121">-Confirm</span></span>
<span data-ttu-id="d3df1-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3df1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3df1-123">-WhatIf</span></span>
<span data-ttu-id="d3df1-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d3df1-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3df1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3df1-126">CommonParameters</span></span>
<span data-ttu-id="d3df1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3df1-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3df1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3df1-129">입력</span><span class="sxs-lookup"><span data-stu-id="d3df1-129">INPUTS</span></span>

### <span data-ttu-id="d3df1-130">않아야</span><span class="sxs-lookup"><span data-stu-id="d3df1-130">None</span></span>
<span data-ttu-id="d3df1-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d3df1-132">출력</span><span class="sxs-lookup"><span data-stu-id="d3df1-132">OUTPUTS</span></span>

### <span data-ttu-id="d3df1-133">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="d3df1-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d3df1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d3df1-134">NOTES</span></span>

## <span data-ttu-id="d3df1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3df1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3df1-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d3df1-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d3df1-137">새로운 AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d3df1-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


