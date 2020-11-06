---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527332"
---
# <span data-ttu-id="4258e-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4258e-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="4258e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4258e-102">SYNOPSIS</span></span>
<span data-ttu-id="4258e-103">Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4258e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4258e-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4258e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4258e-105">DESCRIPTION</span></span>
<span data-ttu-id="4258e-106">**AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="4258e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4258e-107">EXAMPLES</span></span>

### <span data-ttu-id="4258e-108">예제 1: Redis Cache를 제거 하 고 결과 반환</span><span class="sxs-lookup"><span data-stu-id="4258e-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="4258e-109">이 명령은 Redis 캐시를 제거 하 고 작업의 성공 여부를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="4258e-110">예제 2: Redis Cache 제거 및 결과 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="4258e-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="4258e-111">이 명령은 Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="4258e-112">*PassThru* 매개 변수를 지정 하지 않았으므로 연산 결과가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="4258e-113">변수</span><span class="sxs-lookup"><span data-stu-id="4258e-113">PARAMETERS</span></span>

### <span data-ttu-id="4258e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4258e-114">-Force</span></span>
<span data-ttu-id="4258e-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4258e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4258e-116">-Name</span></span>
<span data-ttu-id="4258e-117">제거할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-117">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4258e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4258e-118">-PassThru</span></span>
<span data-ttu-id="4258e-119">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4258e-120">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4258e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4258e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4258e-122">제거할 Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-122">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4258e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4258e-123">-Confirm</span></span>
<span data-ttu-id="4258e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4258e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4258e-125">-WhatIf</span></span>
<span data-ttu-id="4258e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4258e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4258e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4258e-128">-DefaultProfile</span></span>
<span data-ttu-id="4258e-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4258e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4258e-130">CommonParameters</span></span>
<span data-ttu-id="4258e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4258e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4258e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4258e-133">입력</span><span class="sxs-lookup"><span data-stu-id="4258e-133">INPUTS</span></span>

### <span data-ttu-id="4258e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="4258e-134">None</span></span>
<span data-ttu-id="4258e-135">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="4258e-136">출력</span><span class="sxs-lookup"><span data-stu-id="4258e-136">OUTPUTS</span></span>

### <span data-ttu-id="4258e-137">나타내는</span><span class="sxs-lookup"><span data-stu-id="4258e-137">Boolean</span></span>
<span data-ttu-id="4258e-138">예외가 발생 하지 않는 경우 $True를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4258e-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="4258e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4258e-139">NOTES</span></span>

## <span data-ttu-id="4258e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4258e-140">RELATED LINKS</span></span>

[<span data-ttu-id="4258e-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4258e-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="4258e-142">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4258e-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="4258e-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="4258e-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


