---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526943"
---
# <span data-ttu-id="17b26-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17b26-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="17b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17b26-102">SYNOPSIS</span></span>
<span data-ttu-id="17b26-103">Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17b26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17b26-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17b26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17b26-105">DESCRIPTION</span></span>
<span data-ttu-id="17b26-106">**AzureRmAvailabilitySet** Cmdlet은 Azure에서 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="17b26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="17b26-107">EXAMPLES</span></span>

### <span data-ttu-id="17b26-108">예제 1: 가용성 집합 제거</span><span class="sxs-lookup"><span data-stu-id="17b26-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="17b26-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="17b26-110">변수</span><span class="sxs-lookup"><span data-stu-id="17b26-110">PARAMETERS</span></span>

### <span data-ttu-id="17b26-111">-Force</span><span class="sxs-lookup"><span data-stu-id="17b26-111">-Force</span></span>
<span data-ttu-id="17b26-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17b26-113">-이름</span><span class="sxs-lookup"><span data-stu-id="17b26-113">-Name</span></span>
<span data-ttu-id="17b26-114">가용성 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-114">The availability set name.</span></span>

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

### <span data-ttu-id="17b26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17b26-115">-ResourceGroupName</span></span>
<span data-ttu-id="17b26-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="17b26-117">-확인</span><span class="sxs-lookup"><span data-stu-id="17b26-117">-Confirm</span></span>
<span data-ttu-id="17b26-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17b26-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17b26-119">-WhatIf</span></span>
<span data-ttu-id="17b26-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="17b26-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17b26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b26-122">CommonParameters</span></span>
<span data-ttu-id="17b26-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b26-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b26-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b26-125">입력</span><span class="sxs-lookup"><span data-stu-id="17b26-125">INPUTS</span></span>

### <span data-ttu-id="17b26-126">않아야</span><span class="sxs-lookup"><span data-stu-id="17b26-126">None</span></span>
<span data-ttu-id="17b26-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17b26-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17b26-128">출력</span><span class="sxs-lookup"><span data-stu-id="17b26-128">OUTPUTS</span></span>

## <span data-ttu-id="17b26-129">상속자</span><span class="sxs-lookup"><span data-stu-id="17b26-129">NOTES</span></span>

## <span data-ttu-id="17b26-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17b26-130">RELATED LINKS</span></span>

[<span data-ttu-id="17b26-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17b26-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="17b26-132">새로운 AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="17b26-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


