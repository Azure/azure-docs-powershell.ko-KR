---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206160"
---
# <span data-ttu-id="25b84-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="25b84-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="25b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b84-102">SYNOPSIS</span></span>
<span data-ttu-id="25b84-103">Redis Cache의 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="25b84-104">구문</span><span class="sxs-lookup"><span data-stu-id="25b84-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b84-105">설명</span><span class="sxs-lookup"><span data-stu-id="25b84-105">DESCRIPTION</span></span>
<span data-ttu-id="25b84-106">**New-AzRedisCacheKey** cmdlet은 Azure Redis Cache의 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="25b84-107">예제</span><span class="sxs-lookup"><span data-stu-id="25b84-107">EXAMPLES</span></span>

### <span data-ttu-id="25b84-108">예제 1: 기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="25b84-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="25b84-109">이 명령은 Redis Cache의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="25b84-110">예제 2: 보조 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="25b84-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="25b84-111">이 명령은 Redis Cache의 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="25b84-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b84-112">PARAMETERS</span></span>

### <span data-ttu-id="25b84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b84-113">-DefaultProfile</span></span>
<span data-ttu-id="25b84-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="25b84-115">-Force</span></span>
<span data-ttu-id="25b84-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25b84-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="25b84-117">-KeyType</span></span>
<span data-ttu-id="25b84-118">기본 또는 보조 액세스 키를 다시 생성할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="25b84-119">유효한 값은 기본, 보조입니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b84-120">-Name</span><span class="sxs-lookup"><span data-stu-id="25b84-120">-Name</span></span>
<span data-ttu-id="25b84-121">Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="25b84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b84-122">-ResourceGroupName</span></span>
<span data-ttu-id="25b84-123">Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="25b84-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25b84-124">-Confirm</span></span>
<span data-ttu-id="25b84-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b84-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b84-126">-WhatIf</span></span>
<span data-ttu-id="25b84-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25b84-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b84-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b84-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b84-129">CommonParameters</span></span>
<span data-ttu-id="25b84-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25b84-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b84-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25b84-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b84-132">입력</span><span class="sxs-lookup"><span data-stu-id="25b84-132">INPUTS</span></span>

### <span data-ttu-id="25b84-133">System.String</span><span class="sxs-lookup"><span data-stu-id="25b84-133">System.String</span></span>

## <span data-ttu-id="25b84-134">출력</span><span class="sxs-lookup"><span data-stu-id="25b84-134">OUTPUTS</span></span>

### <span data-ttu-id="25b84-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="25b84-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="25b84-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25b84-136">NOTES</span></span>

## <span data-ttu-id="25b84-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25b84-137">RELATED LINKS</span></span>

[<span data-ttu-id="25b84-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="25b84-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)


