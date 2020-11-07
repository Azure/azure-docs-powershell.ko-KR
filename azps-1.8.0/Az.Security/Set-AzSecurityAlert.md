---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699232"
---
# <span data-ttu-id="1a789-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="1a789-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="1a789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a789-102">SYNOPSIS</span></span>
<span data-ttu-id="1a789-103">보안 알림 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-103">Updates a security alert state.</span></span>

## <span data-ttu-id="1a789-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a789-104">SYNTAX</span></span>

### <span data-ttu-id="1a789-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a789-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a789-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="1a789-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a789-107">리소스</span><span class="sxs-lookup"><span data-stu-id="1a789-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a789-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="1a789-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a789-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1a789-109">DESCRIPTION</span></span>
<span data-ttu-id="1a789-110">보안 경고 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-110">Sets a security alert state.</span></span>

## <span data-ttu-id="1a789-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1a789-111">EXAMPLES</span></span>

### <span data-ttu-id="1a789-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a789-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="1a789-113">발생 한 보안 경고를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="1a789-114">변수</span><span class="sxs-lookup"><span data-stu-id="1a789-114">PARAMETERS</span></span>

### <span data-ttu-id="1a789-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="1a789-115">-ActionType</span></span>
<span data-ttu-id="1a789-116">작업 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-116">Action Type.</span></span>

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

### <span data-ttu-id="1a789-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a789-117">-DefaultProfile</span></span>
<span data-ttu-id="1a789-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a789-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a789-119">-InputObject</span></span>
<span data-ttu-id="1a789-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="1a789-120">Input Object.</span></span>

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

### <span data-ttu-id="1a789-121">-위치</span><span class="sxs-lookup"><span data-stu-id="1a789-121">-Location</span></span>
<span data-ttu-id="1a789-122">Location.</span><span class="sxs-lookup"><span data-stu-id="1a789-122">Location.</span></span>

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

### <span data-ttu-id="1a789-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1a789-123">-Name</span></span>
<span data-ttu-id="1a789-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-124">Resource name.</span></span>

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

### <span data-ttu-id="1a789-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a789-125">-PassThru</span></span>
<span data-ttu-id="1a789-126">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="1a789-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a789-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a789-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-128">Resource group name.</span></span>

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

### <span data-ttu-id="1a789-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a789-129">-ResourceId</span></span>
<span data-ttu-id="1a789-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-130">Resource ID.</span></span>

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

### <span data-ttu-id="1a789-131">-확인</span><span class="sxs-lookup"><span data-stu-id="1a789-131">-Confirm</span></span>
<span data-ttu-id="1a789-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a789-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a789-133">-WhatIf</span></span>
<span data-ttu-id="1a789-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a789-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a789-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a789-136">CommonParameters</span></span>
<span data-ttu-id="1a789-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a789-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a789-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a789-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a789-139">입력</span><span class="sxs-lookup"><span data-stu-id="1a789-139">INPUTS</span></span>

### <span data-ttu-id="1a789-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a789-140">System.String</span></span>

### <span data-ttu-id="1a789-141">Microsoft. Azure. 경고용. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="1a789-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="1a789-142">출력</span><span class="sxs-lookup"><span data-stu-id="1a789-142">OUTPUTS</span></span>

### <span data-ttu-id="1a789-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1a789-143">System.Boolean</span></span>

## <span data-ttu-id="1a789-144">상속자</span><span class="sxs-lookup"><span data-stu-id="1a789-144">NOTES</span></span>

## <span data-ttu-id="1a789-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a789-145">RELATED LINKS</span></span>
