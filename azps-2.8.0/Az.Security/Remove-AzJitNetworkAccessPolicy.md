---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b0414b6fbbd4cdb0211b7dee1f85e172c1329c3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873185"
---
# <span data-ttu-id="02749-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="02749-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="02749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02749-102">SYNOPSIS</span></span>
<span data-ttu-id="02749-103">JIT 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="02749-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02749-104">SYNTAX</span></span>

### <span data-ttu-id="02749-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="02749-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02749-106">리소스</span><span class="sxs-lookup"><span data-stu-id="02749-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02749-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="02749-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02749-108">설명은</span><span class="sxs-lookup"><span data-stu-id="02749-108">DESCRIPTION</span></span>
<span data-ttu-id="02749-109">Just-in-time 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="02749-110">이 작업을 수행한 후에는 사용자가 삭제 된 정책 내에서 구성 된 Vm에 대해 임시 네트워크 연결을 요청할 수 없게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02749-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="02749-111">예제의</span><span class="sxs-lookup"><span data-stu-id="02749-111">EXAMPLES</span></span>

### <span data-ttu-id="02749-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="02749-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="02749-113">Just-in-time 네트워크 액세스 정책을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="02749-114">변수</span><span class="sxs-lookup"><span data-stu-id="02749-114">PARAMETERS</span></span>

### <span data-ttu-id="02749-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02749-115">-DefaultProfile</span></span>
<span data-ttu-id="02749-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02749-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02749-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02749-117">-InputObject</span></span>
<span data-ttu-id="02749-118">입력 개체</span><span class="sxs-lookup"><span data-stu-id="02749-118">Input Object.</span></span>

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

### <span data-ttu-id="02749-119">-위치</span><span class="sxs-lookup"><span data-stu-id="02749-119">-Location</span></span>
<span data-ttu-id="02749-120">Location.</span><span class="sxs-lookup"><span data-stu-id="02749-120">Location.</span></span>

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

### <span data-ttu-id="02749-121">-이름</span><span class="sxs-lookup"><span data-stu-id="02749-121">-Name</span></span>
<span data-ttu-id="02749-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02749-122">Resource name.</span></span>

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

### <span data-ttu-id="02749-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02749-123">-PassThru</span></span>
<span data-ttu-id="02749-124">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="02749-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02749-125">-ResourceGroupName</span></span>
<span data-ttu-id="02749-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02749-126">Resource group name.</span></span>

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

### <span data-ttu-id="02749-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02749-127">-ResourceId</span></span>
<span data-ttu-id="02749-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02749-128">Resource ID.</span></span>

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

### <span data-ttu-id="02749-129">-확인</span><span class="sxs-lookup"><span data-stu-id="02749-129">-Confirm</span></span>
<span data-ttu-id="02749-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02749-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02749-131">-WhatIf</span></span>
<span data-ttu-id="02749-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02749-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02749-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02749-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02749-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02749-134">CommonParameters</span></span>
<span data-ttu-id="02749-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02749-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02749-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02749-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02749-137">입력</span><span class="sxs-lookup"><span data-stu-id="02749-137">INPUTS</span></span>

### <span data-ttu-id="02749-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02749-138">System.String</span></span>

### <span data-ttu-id="02749-139">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="02749-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="02749-140">출력</span><span class="sxs-lookup"><span data-stu-id="02749-140">OUTPUTS</span></span>

### <span data-ttu-id="02749-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="02749-141">System.Boolean</span></span>

## <span data-ttu-id="02749-142">상속자</span><span class="sxs-lookup"><span data-stu-id="02749-142">NOTES</span></span>

## <span data-ttu-id="02749-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02749-143">RELATED LINKS</span></span>
