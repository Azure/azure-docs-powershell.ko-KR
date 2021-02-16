---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208232"
---
# <span data-ttu-id="006a9-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="006a9-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="006a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="006a9-102">SYNOPSIS</span></span>
<span data-ttu-id="006a9-103">보안 경고 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-103">Updates a security alert state.</span></span>

## <span data-ttu-id="006a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="006a9-104">SYNTAX</span></span>

### <span data-ttu-id="006a9-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="006a9-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006a9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="006a9-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006a9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="006a9-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006a9-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="006a9-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="006a9-109">설명</span><span class="sxs-lookup"><span data-stu-id="006a9-109">DESCRIPTION</span></span>
<span data-ttu-id="006a9-110">보안 경고 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-110">Sets a security alert state.</span></span>

## <span data-ttu-id="006a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="006a9-111">EXAMPLES</span></span>

### <span data-ttu-id="006a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="006a9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="006a9-113">발생된 보안 경고를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="006a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="006a9-114">PARAMETERS</span></span>

### <span data-ttu-id="006a9-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="006a9-115">-ActionType</span></span>
<span data-ttu-id="006a9-116">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006a9-117">-DefaultProfile</span></span>
<span data-ttu-id="006a9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="006a9-119">-InputObject</span></span>
<span data-ttu-id="006a9-120">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="006a9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="006a9-121">-Location</span></span>
<span data-ttu-id="006a9-122">위치.</span><span class="sxs-lookup"><span data-stu-id="006a9-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006a9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="006a9-123">-Name</span></span>
<span data-ttu-id="006a9-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006a9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="006a9-125">-PassThru</span></span>
<span data-ttu-id="006a9-126">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="006a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="006a9-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006a9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="006a9-129">-ResourceId</span></span>
<span data-ttu-id="006a9-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-130">Resource ID.</span></span>

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

### <span data-ttu-id="006a9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="006a9-131">-Confirm</span></span>
<span data-ttu-id="006a9-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006a9-133">-WhatIf</span></span>
<span data-ttu-id="006a9-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="006a9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="006a9-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006a9-136">CommonParameters</span></span>
<span data-ttu-id="006a9-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="006a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006a9-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="006a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006a9-139">입력</span><span class="sxs-lookup"><span data-stu-id="006a9-139">INPUTS</span></span>

### <span data-ttu-id="006a9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="006a9-140">System.String</span></span>

### <span data-ttu-id="006a9-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="006a9-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="006a9-142">출력</span><span class="sxs-lookup"><span data-stu-id="006a9-142">OUTPUTS</span></span>

### <span data-ttu-id="006a9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="006a9-143">System.Boolean</span></span>

## <span data-ttu-id="006a9-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="006a9-144">NOTES</span></span>

## <span data-ttu-id="006a9-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="006a9-145">RELATED LINKS</span></span>
