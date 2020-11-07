---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 1e9895b78bc61155f7cabfc63e6fb5e4cfbcd30d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699539"
---
# <span data-ttu-id="e00b0-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00b0-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="e00b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e00b0-102">SYNOPSIS</span></span>
<span data-ttu-id="e00b0-103">Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="e00b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e00b0-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e00b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e00b0-105">DESCRIPTION</span></span>
<span data-ttu-id="e00b0-106">**AzRedisCache** Cmdlet은 Azure Redis Cache를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="e00b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e00b0-107">EXAMPLES</span></span>

### <span data-ttu-id="e00b0-108">예제 1: Redis Cache를 제거 하 고 결과 반환</span><span class="sxs-lookup"><span data-stu-id="e00b0-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="e00b0-109">이 명령은 Redis 캐시를 제거 하 고 작업의 성공 여부를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="e00b0-110">예제 2: Redis Cache 제거 및 결과 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e00b0-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="e00b0-111">이 명령은 Redis 캐시를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="e00b0-112">*PassThru* 매개 변수를 지정 하지 않았으므로 연산 결과가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="e00b0-113">변수</span><span class="sxs-lookup"><span data-stu-id="e00b0-113">PARAMETERS</span></span>

### <span data-ttu-id="e00b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00b0-114">-DefaultProfile</span></span>
<span data-ttu-id="e00b0-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e00b0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e00b0-116">-Force</span></span>
<span data-ttu-id="e00b0-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e00b0-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e00b0-118">-Name</span></span>
<span data-ttu-id="e00b0-119">제거할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="e00b0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e00b0-120">-PassThru</span></span>
<span data-ttu-id="e00b0-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e00b0-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e00b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e00b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="e00b0-124">제거할 Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e00b0-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e00b0-125">-Confirm</span></span>
<span data-ttu-id="e00b0-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e00b0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e00b0-127">-WhatIf</span></span>
<span data-ttu-id="e00b0-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e00b0-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e00b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00b0-130">CommonParameters</span></span>
<span data-ttu-id="e00b0-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e00b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00b0-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e00b0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00b0-133">입력</span><span class="sxs-lookup"><span data-stu-id="e00b0-133">INPUTS</span></span>

### <span data-ttu-id="e00b0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e00b0-134">System.String</span></span>

## <span data-ttu-id="e00b0-135">출력</span><span class="sxs-lookup"><span data-stu-id="e00b0-135">OUTPUTS</span></span>

### <span data-ttu-id="e00b0-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e00b0-136">System.Boolean</span></span>

## <span data-ttu-id="e00b0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e00b0-137">NOTES</span></span>

## <span data-ttu-id="e00b0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e00b0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e00b0-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00b0-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="e00b0-140">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00b0-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="e00b0-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="e00b0-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


