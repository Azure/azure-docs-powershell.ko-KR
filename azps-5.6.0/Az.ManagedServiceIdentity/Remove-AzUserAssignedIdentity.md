---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 83280df19363285ab23ca1e27441a491a783b03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962912"
---
# <span data-ttu-id="5b503-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5b503-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="5b503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b503-102">SYNOPSIS</span></span>
<span data-ttu-id="5b503-103">사용자 할당 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="5b503-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b503-104">SYNTAX</span></span>

### <span data-ttu-id="5b503-105">ResourceGroupAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b503-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b503-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b503-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b503-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b503-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b503-108">설명</span><span class="sxs-lookup"><span data-stu-id="5b503-108">DESCRIPTION</span></span>
<span data-ttu-id="5b503-109">**Remove-AzUserAssignedIdentity는** 지정된 사용자 할당 ID를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="5b503-110">예제</span><span class="sxs-lookup"><span data-stu-id="5b503-110">EXAMPLES</span></span>

### <span data-ttu-id="5b503-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b503-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="5b503-112">이 예제 cmdlet은 리소스 그룹 **PSRG에서 ID ID1을** **삭제합니다.**</span><span class="sxs-lookup"><span data-stu-id="5b503-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="5b503-113">True</span><span class="sxs-lookup"><span data-stu-id="5b503-113">True</span></span>

## <span data-ttu-id="5b503-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b503-114">PARAMETERS</span></span>

### <span data-ttu-id="5b503-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b503-115">-AsJob</span></span>
<span data-ttu-id="5b503-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b503-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b503-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b503-117">-DefaultProfile</span></span>
<span data-ttu-id="5b503-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b503-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b503-119">-Force</span></span>
<span data-ttu-id="5b503-120">{{채우기 힘 설명}}</span><span class="sxs-lookup"><span data-stu-id="5b503-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="5b503-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b503-121">-InputObject</span></span>
<span data-ttu-id="5b503-122">ID 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-122">The Identity object.</span></span>

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

### <span data-ttu-id="5b503-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b503-123">-Name</span></span>
<span data-ttu-id="5b503-124">ID 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-124">The Identity name.</span></span>

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

### <span data-ttu-id="5b503-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b503-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b503-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-126">The resource group name.</span></span>

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

### <span data-ttu-id="5b503-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b503-127">-ResourceId</span></span>
<span data-ttu-id="5b503-128">ID의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="5b503-129">-확인</span><span class="sxs-lookup"><span data-stu-id="5b503-129">-Confirm</span></span>
<span data-ttu-id="5b503-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b503-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b503-131">-WhatIf</span></span>
<span data-ttu-id="5b503-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b503-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b503-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b503-134">CommonParameters</span></span>
<span data-ttu-id="5b503-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b503-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b503-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b503-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b503-137">입력</span><span class="sxs-lookup"><span data-stu-id="5b503-137">INPUTS</span></span>

### <span data-ttu-id="5b503-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5b503-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="5b503-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5b503-139">System.String</span></span>

## <span data-ttu-id="5b503-140">출력</span><span class="sxs-lookup"><span data-stu-id="5b503-140">OUTPUTS</span></span>

### <span data-ttu-id="5b503-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b503-141">System.Boolean</span></span>

## <span data-ttu-id="5b503-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b503-142">NOTES</span></span>

## <span data-ttu-id="5b503-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b503-143">RELATED LINKS</span></span>
