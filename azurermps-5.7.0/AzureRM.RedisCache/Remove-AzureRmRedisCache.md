---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529753"
---
# <span data-ttu-id="16b88-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="16b88-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="16b88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b88-102">SYNOPSIS</span></span>
<span data-ttu-id="16b88-103">Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16b88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16b88-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16b88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16b88-105">DESCRIPTION</span></span>
<span data-ttu-id="16b88-106">**AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="16b88-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16b88-107">EXAMPLES</span></span>

### <span data-ttu-id="16b88-108">예제 1: Redis Cache를 제거 하 고 결과 반환</span><span class="sxs-lookup"><span data-stu-id="16b88-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="16b88-109">이 명령은 Redis 캐시를 제거 하 고 작업의 성공 여부를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="16b88-110">예제 2: Redis Cache 제거 및 결과 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="16b88-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="16b88-111">이 명령은 Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="16b88-112">*PassThru* 매개 변수를 지정 하지 않았으므로 연산 결과가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="16b88-113">변수</span><span class="sxs-lookup"><span data-stu-id="16b88-113">PARAMETERS</span></span>

### <span data-ttu-id="16b88-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b88-114">-DefaultProfile</span></span>
<span data-ttu-id="16b88-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16b88-116">-Force</span><span class="sxs-lookup"><span data-stu-id="16b88-116">-Force</span></span>
<span data-ttu-id="16b88-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16b88-118">-이름</span><span class="sxs-lookup"><span data-stu-id="16b88-118">-Name</span></span>
<span data-ttu-id="16b88-119">제거할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-119">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b88-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16b88-120">-PassThru</span></span>
<span data-ttu-id="16b88-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16b88-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16b88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16b88-123">-ResourceGroupName</span></span>
<span data-ttu-id="16b88-124">제거할 Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16b88-125">-확인</span><span class="sxs-lookup"><span data-stu-id="16b88-125">-Confirm</span></span>
<span data-ttu-id="16b88-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b88-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16b88-127">-WhatIf</span></span>
<span data-ttu-id="16b88-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16b88-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b88-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b88-130">CommonParameters</span></span>
<span data-ttu-id="16b88-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b88-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b88-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b88-133">입력</span><span class="sxs-lookup"><span data-stu-id="16b88-133">INPUTS</span></span>

### <span data-ttu-id="16b88-134">않아야</span><span class="sxs-lookup"><span data-stu-id="16b88-134">None</span></span>
<span data-ttu-id="16b88-135">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="16b88-136">출력</span><span class="sxs-lookup"><span data-stu-id="16b88-136">OUTPUTS</span></span>

### <span data-ttu-id="16b88-137">나타내는</span><span class="sxs-lookup"><span data-stu-id="16b88-137">Boolean</span></span>
<span data-ttu-id="16b88-138">예외가 발생 하지 않는 경우 $True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16b88-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="16b88-139">상속자</span><span class="sxs-lookup"><span data-stu-id="16b88-139">NOTES</span></span>

## <span data-ttu-id="16b88-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16b88-140">RELATED LINKS</span></span>

[<span data-ttu-id="16b88-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="16b88-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="16b88-142">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="16b88-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="16b88-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="16b88-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


