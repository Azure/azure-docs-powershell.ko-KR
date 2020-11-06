---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535656"
---
# <span data-ttu-id="67c77-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="67c77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67c77-102">SYNOPSIS</span></span>
<span data-ttu-id="67c77-103">캐시 노드를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67c77-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67c77-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67c77-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67c77-105">DESCRIPTION</span></span>
<span data-ttu-id="67c77-106">**AzureRmRedisCache** Cmdlet은 Azure Redis Cache 인스턴스의 노드를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="67c77-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67c77-107">EXAMPLES</span></span>

### <span data-ttu-id="67c77-108">예제 1: 두 노드 모두 다시 시작</span><span class="sxs-lookup"><span data-stu-id="67c77-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="67c77-109">이 명령은 RedisCache06 이라는 캐시에 대해 두 노드를 모두 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="67c77-110">변수</span><span class="sxs-lookup"><span data-stu-id="67c77-110">PARAMETERS</span></span>

### <span data-ttu-id="67c77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c77-111">-DefaultProfile</span></span>
<span data-ttu-id="67c77-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c77-113">-Force</span><span class="sxs-lookup"><span data-stu-id="67c77-113">-Force</span></span>
<span data-ttu-id="67c77-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67c77-115">-이름</span><span class="sxs-lookup"><span data-stu-id="67c77-115">-Name</span></span>
<span data-ttu-id="67c77-116">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="67c77-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67c77-117">-PassThru</span></span>
<span data-ttu-id="67c77-118">이 cmdlet이 작업 성공 여부를 나타내는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="67c77-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67c77-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="67c77-120">-RebootType</span></span>
<span data-ttu-id="67c77-121">다시 시작할 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="67c77-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="67c77-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="67c77-123">PrimaryNode</span></span> 
- <span data-ttu-id="67c77-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="67c77-124">SecondaryNode</span></span> 
- <span data-ttu-id="67c77-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="67c77-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c77-126">-ResourceGroupName</span></span>
<span data-ttu-id="67c77-127">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="67c77-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="67c77-128">-ShardId</span></span>
<span data-ttu-id="67c77-129">클러스터링이 활성화 된 premium 캐시로이 cmdlet이 다시 시작 하는 샤 드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67c77-130">-확인</span><span class="sxs-lookup"><span data-stu-id="67c77-130">-Confirm</span></span>
<span data-ttu-id="67c77-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67c77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67c77-132">-WhatIf</span></span>
<span data-ttu-id="67c77-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67c77-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67c77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c77-135">CommonParameters</span></span>
<span data-ttu-id="67c77-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c77-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c77-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c77-138">입력</span><span class="sxs-lookup"><span data-stu-id="67c77-138">INPUTS</span></span>

### <span data-ttu-id="67c77-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67c77-139">System.String</span></span>

### <span data-ttu-id="67c77-140">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="67c77-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="67c77-141">출력</span><span class="sxs-lookup"><span data-stu-id="67c77-141">OUTPUTS</span></span>

### <span data-ttu-id="67c77-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="67c77-142">System.Boolean</span></span>

## <span data-ttu-id="67c77-143">상속자</span><span class="sxs-lookup"><span data-stu-id="67c77-143">NOTES</span></span>
* <span data-ttu-id="67c77-144">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="67c77-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="67c77-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67c77-145">RELATED LINKS</span></span>

[<span data-ttu-id="67c77-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="67c77-147">가져오기-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="67c77-148">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="67c77-149">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="67c77-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="67c77-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


