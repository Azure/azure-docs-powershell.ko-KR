---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 7220304c4dbc234a3513d2dfc35e6d71180159e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003088"
---
# <span data-ttu-id="a72d9-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a72d9-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a72d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a72d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a72d9-103">JIT 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="a72d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a72d9-104">SYNTAX</span></span>

### <span data-ttu-id="a72d9-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="a72d9-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a72d9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72d9-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a72d9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a72d9-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a72d9-108">설명</span><span class="sxs-lookup"><span data-stu-id="a72d9-108">DESCRIPTION</span></span>
<span data-ttu-id="a72d9-109">Just In-Time 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="a72d9-110">이 작업 후 사용자는 삭제된 정책 내에서 구성된 VM에서 임시 네트워크 연결을 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="a72d9-111">예제</span><span class="sxs-lookup"><span data-stu-id="a72d9-111">EXAMPLES</span></span>

### <span data-ttu-id="a72d9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a72d9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="a72d9-113">Just In-Time 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="a72d9-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a72d9-114">PARAMETERS</span></span>

### <span data-ttu-id="a72d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72d9-115">-DefaultProfile</span></span>
<span data-ttu-id="a72d9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a72d9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a72d9-117">-InputObject</span></span>
<span data-ttu-id="a72d9-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a72d9-119">-Location</span></span>
<span data-ttu-id="a72d9-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72d9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a72d9-121">-Name</span></span>
<span data-ttu-id="a72d9-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72d9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a72d9-123">-PassThru</span></span>
<span data-ttu-id="a72d9-124">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a72d9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a72d9-125">-ResourceGroupName</span></span>
<span data-ttu-id="a72d9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72d9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a72d9-127">-ResourceId</span></span>
<span data-ttu-id="a72d9-128">jit Network Access Policy 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a72d9-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a72d9-129">-Confirm</span></span>
<span data-ttu-id="a72d9-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a72d9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a72d9-131">-WhatIf</span></span>
<span data-ttu-id="a72d9-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a72d9-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a72d9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72d9-134">CommonParameters</span></span>
<span data-ttu-id="a72d9-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a72d9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72d9-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a72d9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72d9-137">입력</span><span class="sxs-lookup"><span data-stu-id="a72d9-137">INPUTS</span></span>

### <span data-ttu-id="a72d9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a72d9-138">System.String</span></span>

### <span data-ttu-id="a72d9-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a72d9-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a72d9-140">출력</span><span class="sxs-lookup"><span data-stu-id="a72d9-140">OUTPUTS</span></span>

### <span data-ttu-id="a72d9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a72d9-141">System.Boolean</span></span>

## <span data-ttu-id="a72d9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a72d9-142">NOTES</span></span>

## <span data-ttu-id="a72d9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a72d9-143">RELATED LINKS</span></span>
