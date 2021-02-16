---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187497"
---
# <span data-ttu-id="a65e0-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a65e0-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="a65e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a65e0-103">사용자 할당 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="a65e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="a65e0-104">SYNTAX</span></span>

### <span data-ttu-id="a65e0-105">ResourceGroupAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a65e0-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65e0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65e0-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65e0-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a65e0-108">설명</span><span class="sxs-lookup"><span data-stu-id="a65e0-108">DESCRIPTION</span></span>
<span data-ttu-id="a65e0-109">**Remove-AzUserAssignedIdentity는** 지정된 사용자 할당 ID를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="a65e0-110">예제</span><span class="sxs-lookup"><span data-stu-id="a65e0-110">EXAMPLES</span></span>

### <span data-ttu-id="a65e0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a65e0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="a65e0-112">이 예제 cmdlet은 리소스 그룹 **PSRG에서 ID ID1을** **삭제합니다.**</span><span class="sxs-lookup"><span data-stu-id="a65e0-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="a65e0-113">True</span><span class="sxs-lookup"><span data-stu-id="a65e0-113">True</span></span>

## <span data-ttu-id="a65e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a65e0-114">PARAMETERS</span></span>

### <span data-ttu-id="a65e0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a65e0-115">-AsJob</span></span>
<span data-ttu-id="a65e0-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a65e0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a65e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65e0-117">-DefaultProfile</span></span>
<span data-ttu-id="a65e0-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65e0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a65e0-119">-Force</span></span>
<span data-ttu-id="a65e0-120">{{힘 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="a65e0-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="a65e0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a65e0-121">-InputObject</span></span>
<span data-ttu-id="a65e0-122">ID 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a65e0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a65e0-123">-Name</span></span>
<span data-ttu-id="a65e0-124">ID 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a65e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="a65e0-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65e0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a65e0-127">-ResourceId</span></span>
<span data-ttu-id="a65e0-128">ID의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a65e0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a65e0-129">-Confirm</span></span>
<span data-ttu-id="a65e0-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65e0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65e0-131">-WhatIf</span></span>
<span data-ttu-id="a65e0-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a65e0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65e0-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65e0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65e0-134">CommonParameters</span></span>
<span data-ttu-id="a65e0-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a65e0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65e0-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a65e0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65e0-137">입력</span><span class="sxs-lookup"><span data-stu-id="a65e0-137">INPUTS</span></span>

### <span data-ttu-id="a65e0-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a65e0-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="a65e0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a65e0-139">System.String</span></span>

## <span data-ttu-id="a65e0-140">출력</span><span class="sxs-lookup"><span data-stu-id="a65e0-140">OUTPUTS</span></span>

### <span data-ttu-id="a65e0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a65e0-141">System.Boolean</span></span>

## <span data-ttu-id="a65e0-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a65e0-142">NOTES</span></span>

## <span data-ttu-id="a65e0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a65e0-143">RELATED LINKS</span></span>
