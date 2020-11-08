---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: cc8292940a252844c0aeabe820eec2e62055c954
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882325"
---
# <span data-ttu-id="7a9bb-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a9bb-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="7a9bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a9bb-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9bb-103">Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a9bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a9bb-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a9bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a9bb-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9bb-106">**AzureRmAvailabilitySet** Cmdlet은 Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="7a9bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a9bb-107">EXAMPLES</span></span>

### <span data-ttu-id="7a9bb-108">예제 1: 가용성 집합 제거</span><span class="sxs-lookup"><span data-stu-id="7a9bb-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7a9bb-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7a9bb-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a9bb-110">PARAMETERS</span></span>

### <span data-ttu-id="7a9bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a9bb-111">-AsJob</span></span>
<span data-ttu-id="7a9bb-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7a9bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9bb-113">-DefaultProfile</span></span>
<span data-ttu-id="7a9bb-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a9bb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a9bb-115">-Force</span></span>
<span data-ttu-id="7a9bb-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a9bb-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7a9bb-117">-Name</span></span>
<span data-ttu-id="7a9bb-118">가용성 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-118">The availability set name.</span></span>

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

### <span data-ttu-id="7a9bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a9bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a9bb-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a9bb-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7a9bb-121">-Confirm</span></span>
<span data-ttu-id="7a9bb-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a9bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a9bb-123">-WhatIf</span></span>
<span data-ttu-id="7a9bb-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7a9bb-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a9bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9bb-126">CommonParameters</span></span>
<span data-ttu-id="7a9bb-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9bb-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9bb-129">입력</span><span class="sxs-lookup"><span data-stu-id="7a9bb-129">INPUTS</span></span>

### <span data-ttu-id="7a9bb-130">않아야</span><span class="sxs-lookup"><span data-stu-id="7a9bb-130">None</span></span>
<span data-ttu-id="7a9bb-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a9bb-132">출력</span><span class="sxs-lookup"><span data-stu-id="7a9bb-132">OUTPUTS</span></span>

### <span data-ttu-id="7a9bb-133">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7a9bb-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7a9bb-134">NOTES</span></span>

## <span data-ttu-id="7a9bb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a9bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="7a9bb-136">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a9bb-136">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="7a9bb-137">새로운 AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7a9bb-137">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

