---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208288"
---
# <span data-ttu-id="21f58-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21f58-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="21f58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f58-102">SYNOPSIS</span></span>
<span data-ttu-id="21f58-103">JIT 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="21f58-104">구문</span><span class="sxs-lookup"><span data-stu-id="21f58-104">SYNTAX</span></span>

### <span data-ttu-id="21f58-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="21f58-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f58-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f58-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f58-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="21f58-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f58-108">설명</span><span class="sxs-lookup"><span data-stu-id="21f58-108">DESCRIPTION</span></span>
<span data-ttu-id="21f58-109">Just-In-Time 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="21f58-110">이 작업을 수행한 후 사용자는 삭제된 정책 내에서 구성된 VM에서 임시 네트워크 연결을 요청할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="21f58-111">예제</span><span class="sxs-lookup"><span data-stu-id="21f58-111">EXAMPLES</span></span>

### <span data-ttu-id="21f58-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="21f58-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="21f58-113">Just-In-Time 네트워크 액세스 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="21f58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21f58-114">PARAMETERS</span></span>

### <span data-ttu-id="21f58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f58-115">-DefaultProfile</span></span>
<span data-ttu-id="21f58-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f58-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21f58-117">-InputObject</span></span>
<span data-ttu-id="21f58-118">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-118">Input Object.</span></span>

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

### <span data-ttu-id="21f58-119">-Location</span><span class="sxs-lookup"><span data-stu-id="21f58-119">-Location</span></span>
<span data-ttu-id="21f58-120">위치.</span><span class="sxs-lookup"><span data-stu-id="21f58-120">Location.</span></span>

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

### <span data-ttu-id="21f58-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21f58-121">-Name</span></span>
<span data-ttu-id="21f58-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-122">Resource name.</span></span>

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

### <span data-ttu-id="21f58-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21f58-123">-PassThru</span></span>
<span data-ttu-id="21f58-124">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="21f58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f58-125">-ResourceGroupName</span></span>
<span data-ttu-id="21f58-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-126">Resource group name.</span></span>

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

### <span data-ttu-id="21f58-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f58-127">-ResourceId</span></span>
<span data-ttu-id="21f58-128">jit 네트워크 액세스 정책 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-128">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="21f58-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21f58-129">-Confirm</span></span>
<span data-ttu-id="21f58-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f58-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f58-131">-WhatIf</span></span>
<span data-ttu-id="21f58-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="21f58-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21f58-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f58-134">CommonParameters</span></span>
<span data-ttu-id="21f58-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21f58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f58-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21f58-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f58-137">입력</span><span class="sxs-lookup"><span data-stu-id="21f58-137">INPUTS</span></span>

### <span data-ttu-id="21f58-138">System.String</span><span class="sxs-lookup"><span data-stu-id="21f58-138">System.String</span></span>

### <span data-ttu-id="21f58-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="21f58-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="21f58-140">출력</span><span class="sxs-lookup"><span data-stu-id="21f58-140">OUTPUTS</span></span>

### <span data-ttu-id="21f58-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21f58-141">System.Boolean</span></span>

## <span data-ttu-id="21f58-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21f58-142">NOTES</span></span>

## <span data-ttu-id="21f58-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21f58-143">RELATED LINKS</span></span>
