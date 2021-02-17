---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206120"
---
# <span data-ttu-id="cee81-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cee81-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="cee81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cee81-102">SYNOPSIS</span></span>
<span data-ttu-id="cee81-103">Redis Cache를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="cee81-104">구문</span><span class="sxs-lookup"><span data-stu-id="cee81-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cee81-105">설명</span><span class="sxs-lookup"><span data-stu-id="cee81-105">DESCRIPTION</span></span>
<span data-ttu-id="cee81-106">**Remove-AzRedisCache** cmdlet은 Azure Redis Cache를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="cee81-107">예제</span><span class="sxs-lookup"><span data-stu-id="cee81-107">EXAMPLES</span></span>

### <span data-ttu-id="cee81-108">예제 1: Redis Cache 제거 및 결과 반환</span><span class="sxs-lookup"><span data-stu-id="cee81-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="cee81-109">이 명령은 Redis Cache를 제거하고 작업이 성공한지 여부를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="cee81-110">예제 2: Redis Cache를 제거하고 결과를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="cee81-111">이 명령은 Redis Cache를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="cee81-112">*PassThru* 매개 변수가 지정되지 않은 경우 작업의 결과가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="cee81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cee81-113">PARAMETERS</span></span>

### <span data-ttu-id="cee81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee81-114">-DefaultProfile</span></span>
<span data-ttu-id="cee81-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee81-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cee81-116">-Force</span></span>
<span data-ttu-id="cee81-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cee81-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cee81-118">-Name</span></span>
<span data-ttu-id="cee81-119">제거할 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="cee81-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cee81-120">-PassThru</span></span>
<span data-ttu-id="cee81-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cee81-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cee81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee81-123">-ResourceGroupName</span></span>
<span data-ttu-id="cee81-124">제거할 Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="cee81-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cee81-125">-Confirm</span></span>
<span data-ttu-id="cee81-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cee81-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cee81-127">-WhatIf</span></span>
<span data-ttu-id="cee81-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cee81-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cee81-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cee81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee81-130">CommonParameters</span></span>
<span data-ttu-id="cee81-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cee81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee81-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cee81-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee81-133">입력</span><span class="sxs-lookup"><span data-stu-id="cee81-133">INPUTS</span></span>

### <span data-ttu-id="cee81-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cee81-134">System.String</span></span>

## <span data-ttu-id="cee81-135">출력</span><span class="sxs-lookup"><span data-stu-id="cee81-135">OUTPUTS</span></span>

### <span data-ttu-id="cee81-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cee81-136">System.Boolean</span></span>

## <span data-ttu-id="cee81-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cee81-137">NOTES</span></span>

## <span data-ttu-id="cee81-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cee81-138">RELATED LINKS</span></span>

[<span data-ttu-id="cee81-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cee81-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="cee81-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cee81-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="cee81-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cee81-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


